# esp32_tools

Some scripts to aid in ESP32 development. 

The ocd_* scripts are all symlinks to ocd_flash to ease development. These simplify working with the ESP32 JTAG board.

The ota script calls my modified version of the update_firmware.py script to, you guessed it, perform OTA updates.

Provided "as is". Who knows, someone may also find them useful :)


Write one file to a specific offset on the ESP32 board:
ocd_flash <binfile> <offset>

Write all the bin files in the build directory to their correct offsets:
ocd_flash

Start an OpenOCD debug server for the current or default project:
ocd_server

Connect to a running OpenOCD debug server:
ocd_debug

Dump a corefile named "corefile.txt". This could be a corefile that has been dumped via the UART.
(I suppose I should make this take an optional name, but hey, I suck)
ocd_coredump

Debug a corefile name "corefile.txt.
ocd_dbgdump

Do an OTA update. If you don't specify a host, it will use the default configured within the script.
ota <ip address/host>

esp_ocd is an early version of the ocd_ tools.
