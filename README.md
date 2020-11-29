# PAL/GAL dumps

This repository contains recreated source code for some PALs (Programmable Array Logic) and GALs (Generic Array Logic) that I have encountered while reverse-engineering retro computer hardware.

PALs and GALs are programmable logic chips that can take the place of many discrete logic components. They can be thought of as the predecessor of modern FPGAs (Field Programmable Gate Array).

Many computers and peripherals from the 80s and 90s used these chips. When cloning or repairing old hardware, it is helpful to have the original code used to program the chip, so that it can be replaced with a modern substitute. However, most PALs and GALs have a security fuse, so it is generally impossible to read back the code once it is written.

For many chips that use simple combinatorial logic, it is possible to work around this simply sending all possible inputs to the chip and recording the results. Software can then be used to turn the truth table back into logic equations. However, some chips use feedback or flip-flops which are difficult to infer from the output. With some knowledge of the original circuit, many of these chips can still be reverse-engineered, but it takes much more effort.
