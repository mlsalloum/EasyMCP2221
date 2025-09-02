=====================================================
Easy MCP2221
=====================================================

Easy MCP2221 is a Python module to interface with Microchip MCP2221 and MCP2221A.

Connected to the USB port, this 14 pin chip part can provide a **normal computer** with the capabilities of a **basic microcontroller**.


MCP2221's peripherals:

- 4 GPIO
- 3 channel ADC
- DAC
- I2C
- UART
- Clock Output
- USB Wake-up via Interrupt Detection.

So you can practice the basics of digital electronics, microcontrollers, and robotics using nothing more than a regular computer, a breadboard, a few parts, and Python.


Quick start
-----------

Install:

.. code-block:: console

	$ pip install EasyMCP2221


First run:

.. code-block:: python

    >>> import EasyMCP2221
    >>> mcp = EasyMCP2221.Device()
    >>> print(mcp)
    {
        "Chip settings": {
            "Power management options": "enabled",
            "USB PID": "0x00DD",
            "USB VID": "0x04D8",
            "USB requested number of mA": 100
        },
        "Factory Serial": "01234567",
        "GP settings": {},
        "USB Manufacturer": "Microchip Technology Inc.",
        "USB Product": "MCP2221 USB-I2C/UART Combo",
        "USB Serial": "0000000000"
    }


GUI
---

*EasyMCP2221 Workbench* is a GUI to play with MCP2221 and MCP2221A chips based on EasyMCP2221 library.

https://github.com/electronicayciencia/EasyMCP2221-GUI


Documentation
-------------

Read the Install Guide, Examples and full API Reference here: https://easymcp2221.readthedocs.io/

Illustrative blog post with examples, pictures and schematics (spanish): `El integrado MCP2221(A) <https://www.electronicayciencia.com/2023/09/integrado-mcp2221.html>`_


Author
----------------------------------------------------

Reinoso Guzman (https://www.electronicayciencia.com).

Initially based on PyMCP2221A library by Yuta Kitagami (https://github.com/nonNoise/PyMCP2221A).

This fork was created to address a niche use-case of simultaneously communicating with two MCP2221 deivces from separate sessions, specifying by USB serial number. 
Initialisation behaviour has been changed to only search through enumerated SNs rather than connecting to devices to read flash info, which was causing conflicts. 
This means that there is a reliance on the MCP2221 devices enumerating with their serial number visible, which is disabled by default but can be enabled in the MCP2221 Utility.


License
----------------------------------------------------

The MIT License (MIT).
