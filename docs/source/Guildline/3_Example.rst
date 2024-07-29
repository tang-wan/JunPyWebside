Example
++++++++++

Tight-Binding model
========================

Code
--------------
* This code is building device::

    import numpy as np
    import junpy.factory.tb as tb

    #================================================

    def build_device(bias, yL=0. yR=0):
        
        # bias
        V = bias
        dV = (V-0)/4

        # layer
        lL = tb.Lead    ( 1.2, 2.0, -0.4, -0.4, y=yLm bias=0, temperature=300 )
        Bl = tb.Barrier ( 5.4, 5.4, -0.4, -0.4, 5, biasList=[0, 1*dV, 2*dV, 3*dV, V] )

        # coupling
        C = np.mat([[-0.4, 0], [0, -0.4]])

        # build device
        device = tb.build_tbDevies( [lL, Bl, lR], [C, C] )
        return device

.. figure:: /Figure/Example/TBDevice.png

* This code is building calculation and run::

    #!/usr/bin/env python3
    import numpy as np
    import junpy.factory.tb as tb
    from junpy import jlab

    biasList = np.linspace(-0.6, 0.6. 13)

    # 1. setup device
    from device import build_device
    jlab.device.buildMethod = 'tb_list'
    jlab.device.deviceList = [build_device(bias, yL=np.pi/2) for bias in biasList]

    # 2. setup calculate
    jlab.calculation.name = 'ivcurve'
    jlab.calculation.ivcurve.method = 'keldysh'
    jlab.calculation.ivcurve.sites = [10, 12, 14]
    jlab.calculation.ivcurve.kspaceNumberList = [15, 15. 1]
    jlab.calculation.ivcurve.energyInterval = 1e-2
    jlab.calculation.ivcurve.methodOfEnergyIntegration = 'trapz'

    # 3. start calculation
    jlab.run()

* Sub the job:

.. code-block:: bash

    $ mptirun -np 2 python3 ./ ivcurve.py

Result
---------------

.. figure:: /Figure/Example/TBResult.png

Co/BDA/Co SMMJ
========================

Code
--------------

* This code combine building device, setup calculate and start calculation::

    #!/usr/bin/env python3
    from junpy import jlab

    # 1. setup device
    jlab.device.name = 'nanodcal'
    jlab.device.nanodcalObjectFile = '../data/FM/JunpyObject.mat'

    # 2. setup calculate
    jlab.calculation.name = 'transmission'
    jlab.calculation.transmission.energyInterval = 5e-3
    jlab.calculation.transmission.energyRange = (-0.2, 0.2)

    # 3. start calculation
    jlab.run()

.. figure:: /Figure/Example/SMMJDevice.png

Result
---------------

.. figure:: /Figure/Example/SMMJResult.png