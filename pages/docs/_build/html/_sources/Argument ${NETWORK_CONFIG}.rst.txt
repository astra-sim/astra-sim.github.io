Argument ${NETWORK_CONFIG}
==========================

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
