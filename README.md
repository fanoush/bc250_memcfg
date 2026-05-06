# bc250_memcfg
BC-250 tool to set CMOS BIOS memory configuration from linux.
Works also with original P3.00 and P5.00 BIOS, no modded BIOS needed.

## Usage

The most useful parameter to set is probably VRAM size (`UMA_SIZE`)

you run it as root with one parameter and value like this

```
sudo ./bc250memcfg UMA_SIZE 512
setting UMA_SIZE to 512
```
and then reboot the machine.

Running without parameters prints all values for all tunable parameters.

You can also tune memory timings (like tREF) but it may affect stability and no significant gains were confirmed. For more info see https://github.com/NexGen-3D-Printing/SteamMachine/blob/main/Memory-Timings-Explained.txt

This tool writes to battery backed up CMOS RAM, to clear it clear CMOS by jumper on the board and/or by removing battery.

This tool does not require modified BIOS, it was confirmed that it works both with P3.00 and P5.00 original BIOS so no custom BIOS is needed if you just want to modify VRAM size.
