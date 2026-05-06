# bc250_memcfg
BC-250 tool to set CMOS BIOS memory configuration from linux

## Usage

The most useful parameter to set is probably VRAM size (`UMA_SIZE`)

you run it as root with one parameter and value like this

```
sudo ./bc250memcfg UMA_SIZE 512
setting UMA_SIZE to 512
```
and then reboot the machine.

You can also tune memory timings (like tREF) but it may affect stability and no significant gains were confirmed. For more info see https://github.com/NexGen-3D-Printing/SteamMachine/blob/main/Memory-Timings-Explained.txt

This tool writes to battery backed up CMOS RAM, to clear it clear CMOS by jumper on the board and/or by removing battery.
