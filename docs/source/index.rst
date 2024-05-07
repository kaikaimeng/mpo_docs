Welcome to mpo_api's documentation!
===================================
Python standard libraries and micro-libraries
---------------------------------------------
About stardand standard libraries, you can find here:

https://docs.micropython.org/en/latest/library/index.html

Usage for mpo
--------------
.. code-block:: python

    try:
        # This module is a built-in module
        import gds_info as gds
    except ImportError:
        # Or you can import specific module
        import dso2kp as gds
    
    dso = gds.Dso()
    dso.connect() # connect as internal port
    
    # Now you should control your DSO, add your code below.
    # ========
    dso.channel.set_on(2) # Set CH2 to ON
    dso.channel.set_off(2) # Set CH2 to OFF
    dso.awg.set_on(1, wave='SQUAre', freq=10e3) # Set AWG1 ON and waveform is SQUARE, frequency is 10e3
    dso.awg.set_off(1) # Set AWG1 OFF
    # ========
    
    # Don't forget to close the connection.
    dso.close()

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   dso2kp
   dso_acquire
   dso_awg
   dso_basic
   dso_channel
   dso_colors
   dso_const
   dso_display
   dso_dmm
   dso_draw
   dso_gonogo
   dso_gui
   dso_hardcopy
   dso_math
   dso_meas
   dso_power_supply
   dso_ref
   dso_sns
   dso_spectrum
   dso_timebase
   dso_trigger
   load
   psw

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

