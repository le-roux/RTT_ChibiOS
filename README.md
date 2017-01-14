Driver to use RTT (provided by SEGGER) with ChibiOS.

To use it:
    - declare a variable of type RTTStream
    - init this variable with RTTObjectInit(). For BufferIndex, 0 is the value
            to use in most cases. If you don't have a precise reason to set it
            to another value, use 0.
    - You can now use this variable as a BaseSequentialStream one.

To use the shell with RTT:
    - In RTT_streams.h, you can find #define RTT_CLIENT. Set its value according
            to the tool you use on the host side.

WARNING: It's normal if you see twice the characters that you send to the
        device, a correction will be proposed as soon as possible.
        However, this doesn't prevent the driver to work.
