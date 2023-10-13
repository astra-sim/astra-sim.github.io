Running ASTRA-sim
=================

Once ASTRA-sim is built, the executable ${BINARY} is located at:

.. code-block:: console

  # For the analytical network backend
  $ {ASTRA_SIM}/build/astra_analytical/build/AnalyticalAstra/bin/AnalyticalAstra

Conduct experiments by passing the required aruguments:

.. code-block:: console

  $ ${BINARY} \
    --workload-configuration=${WORKLOAD_CONFIG} \
    --system-configuration=${SYSTEM_CONFIG} \
    --network-configuration=${NETWORK_CONFIG} \
    --memory-configuration=${ASTRA_SIM}/inputs/memory/analytical/no_memory_expansion.json

.. note::
  Additional arguments may be required based on the type of network backend.

Argument ${WORKLOAD_CONFIG}
---------------------------

.. code-block:: console

  --workload-configuration: path to the prefix of execution trace files 

The naming rule for execution traces follows the format {path_prefix}.{npu_id}.eg. 

.. note::
  Execution traces can be created using Chakra tools. You have the option of using either execution trace generator (et_generator) or execution trace converter (et_converter). 

Argument ${SYSTEM_CONFIG}
-------------------------

.. code-block:: console

  --system-configuration: path to the system configuration file

Example system configurations can be found at:

.. code-block:: console

  ${ASTRA_SIM}/inputs/system/

* **scheduling-policy**: (LIFO/FIFO) 
  
  The order we proritize collectives according based on their time of arrival. LIFO means that most recently created collectives have higher priority. While FIFO is the reverse.
  
* **intra-dimension-scheduling**: (FIFO/SCF)

  The order we proritize collective chunks inside each dimension. FIFO means that the least recently created collectives have higher priority. SCF means that the smallest chunk have higher priority.
  
* **inter-dimension-scheduling**: (baseline/themis)

  The order we proritize collective chunks across multiple dimensions. baseline means that the scheduling always uses a constant schedule for all chunks. themis means that the scheduling issues chunks to the dimension with least load.
  
* **endpoint-delay**: (int)

  The time NPU spends processing a message after receiving it in terms of cycles.
  
* **active-chunks-per-dimension**: (int)

  This corresponds to the Maximum number of chunks we like execute in parallel on
  each logical dimesnion of topology.
  
* **preferred-dataset-splits**: (int)

  The number of chunks we divide each collective into.
  
* **all-reduce-implementation**: (Dimension0Collective_Dimension1Collective_xxx_DimensionNCollective)

  Here we can create a multiphase colective all-reduce algorithm and directly specify the collective algorithm type for each logical dimension. The available options (algorithms) are: ring, direct, doubleBinaryTree, oneRing, oneDirect.
  
  For example, "ring_doubleBinaryTree" means we create a logical topology with 2 dimensions and we perform ring algorithm on the first dimension followed by double binary tree on the second dimension for the all-reduce pattern. Hence the number of physical dimension should be equal to the number of logical dimensions. The only exceptions are oneRing/oneDirect where we assume no matter how many physical dimensions we have, we create a one big logical ring/direct(AllToAll) topology where all NPUs are connected and perfrom a one phase ring/direct algorithm.
 
.. note::  
  
  oneRing and oneDirect is not available for Garnet Backend in this version. 
  
* **reduce-scatter-implementation**:    (Dimension0CollectiveAlg_Dimension1CollectiveAlg_xxx_DimensionNCollectiveAlg)

  The same as "all-reduce-implementation:" but for reduce-scatter collective. The available options are: ring, direct, oneRing, oneDirect.
  
* **all-gather-implementation**: (Dimension0CollectiveAlg_Dimension1CollectiveAlg_xxx_DimensionNCollectiveAlg)

  The same as "all-reduce-implementation:" but for all-gather collective. The available options (algorithms) are: ring, direct, oneRing, oneDirect.
  
* **all-to-all-implementation**: (Dimension0CollectiveAlg_Dimension1CollectiveAlg_xxx_DimensionNCollectiveAlg)

  The same as "all-reduce-implementation:" but for all-to-all collective. The available options (algorithms) are: ring, direct, oneRing, oneDirect.
  
* **collective-optimization**: (baseline/localBWAware)

  baseline issues allreduce across all dimensions to handle allreduce of single chunk. While for an N-dimensional network, localBWAware issues a series of reduce-scatters on all dimensions from dim1 to dimN-1, followed by all-reduce on dimN, and then series of all-gathers starting from dimN-1 to dim1. This optimization is used to reduce the chunk size as it goes to the next network dimensions.

.. note::   
  The default clock cycle period is 1ns (1 Ghz feq). This value is defined inside Sys.hh. One can change it to any number. It will be a configurable command line parameter in the later versions.

Argument ${NETWORK_CONFIG}
--------------------------

.. code-block:: console

  --network-configuration: path to the network configuration file

Example network configurations can be found at 

.. code-block:: console

  ${ASTRA_SIM}/inputs/network/

* **topology-name**: (string) put "Hierarchical"

* **dimensions-count**: (uint) number of network dimensions

.. note:: 
  Each configurations below is represented as an array of size **dimensions-count**, indexed by the dimension level.

* **topologies-per-dim**: (string) network topology ("Ring", "FullyConnected", or "Switch")
  
* **dimension-type**: (string) dimension type ("Tile", "Package", "Node", or "Pod")

* **units-count**: (uint) number of GPUs

* **links-count**: (uint) number of links

* **link-latency**: (uint) link latency (ns)

* **link-bandwidth**: (uint) link bandwidth (GB/s or B/ns)

* **nic-latency**: (uint) nic latency (ns)

* **router-latency**: (uint) router latency (ns)

* **hbm-latency**: (uint) memory latency (ns)

* **hbm-bandwidth**: (uint) memory bandwidth (GB/s or B/ns)

* **hbm-scale**: (uint) memory scaling factor

Using Execution Trace Generator (et_generator)
----------------------------------------------

et_generator can be used to define and generate any execution traces, functioning as a test case generator. You can generate execution traces with the following commands:

.. code-block:: console

  $ cd {ASTRA_SIM}/extern/graph_frontend/chakra/et_generator
  $ cmake CMakeLists.txt && make -j$(nproc)
  $ ./et_generator --num_npus 64 --num_dims 1

To run one of the example traces (twoCompNodesDependent), execute the following command:

.. code-block:: console

  $ cd -
  $ ./build/astra_analytical/build/AnalyticalAstra/bin/AnalyticalAstra \
    --workload-configuration=./extern/graph_frontend/chakra/et_generator/twoCompNodesDependent \
    --system-configuration=./inputs/system/sample_fully_connected_sys.txt \
    --network-configuration=./inputs/network/analytical/fully_connected.json \
    --memory-configuration=./inputs/memory/analytical/no_memory_expansion.json

Upon completion, ASTRA-sim will display the number of cycles it took to run the simulation.

.. code-block:: console

  sys[0] finished, 10 cycles
  sys[1] finished, 10 cycles
  ...
  sys[62] finished, 10 cycles
  sys[63] finished, 10 cycles

Using Execution Trace Converter (et_converter)
----------------------------------------------

et_converter is a trace schema conversion tool, supporting PyTorch and FlexFlow execution traces, as well as ASTRA-sim 1.0 input files. You can convert ASTRA-sim 1.0 text input files into Chakra traces with the following commands:

.. code-block:: console

  $ cd {ASTRA_SIM}/extern/graph_frontend/chakra/
  $ python3 setup.py install --user
  $ python3 -m et_converter.et_converter \
      --input_type Text \
      --input_filename ../../../inputs/workload/ASTRA-sim-1.0/Resnet50_DataParallel.txt \
      --output_filename ../../../inputs/workload/ASTRA-sim-2.0/Resnet50_DataParallel \
      --num_npus 64 \
      --num_dims 1 \
      --num_passes 1

Run the following command:

.. code-block:: console

  $ cd -
  $ ./build/astra_analytical/build/AnalyticalAstra/bin/AnalyticalAstra \
    --workload-configuration=./inputs/workload/ASTRA-sim-2.0/Resnet50_DataParallel \
    --system-configuration=./inputs/system/sample_fully_connected_sys.txt \
    --network-configuration=./inputs/network/analytical/fully_connected.json \
    --memory-configuration=./inputs/memory/analytical/no_memory_expansion.json

Upon completion, ASTRA-sim will display the number of cycles it took to run the simulation.

.. code-block:: console

  sys[62] finished, 187442108 cycles
  sys[61] finished, 187442108 cycles
  ...
  sys[0] finished, 187442108 cycles
  sys[63] finished, 187442108 cycles


