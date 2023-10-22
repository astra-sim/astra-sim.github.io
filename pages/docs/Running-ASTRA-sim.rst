Running ASTRA-sim
=================

Once ASTRA-sim is built, the executable ${BINARY} is located at:

.. code-block:: console

  # For the analytical network backend
  $ ${ASTRA_SIM}/build/astra_analytical/build/AnalyticalAstra/bin/AnalyticalAstra

Conduct experiments by passing the required aruguments:

.. code-block:: console

  $ ${BINARY} \
    --workload-configuration=${WORKLOAD_CONFIG} \
    --system-configuration=${SYSTEM_CONFIG} \
    --network-configuration=${NETWORK_CONFIG} \
    --memory-configuration=${ASTRA_SIM}/inputs/memory/analytical/no_memory_expansion.json

.. toctree::

  Argument-WORKLOAD-CONFIG
  Argument-SYSTEM-CONFIG
  Argument-NETWORK-CONFIG

.. note::
  Additional arguments may be required based on the type of network backend.
