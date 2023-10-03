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

Argument ${SYSTEM_CONFIG}
-------------------------

.. code-block:: console

  --system-configuration: path to the system configuration file

Example system configurations can be found at:

.. code-block:: console

  ${ASTRA_SIM}/inputs/system/

Argument ${NETWORK_CONFIG}
--------------------------

.. code-block:: console

  --network-configuration: path to the network configuration file

Example network configurations can be found at 

.. code-block:: console

  ${ASTRA_SIM}/inputs/network/

.. note::
  Execution traces can be created using Chakra tools. You have the option of using either execution trace generator (et_generator) or execution trace converter (et_converter). 

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


