# ESP32-C3

Windows First Steps on ESP-IDF
Using the ESP-IDF PowerShell (or CMD), let's use a test project to test the software with.
When you start your shell, it will place you into a directory that depends upon your install
choices. The prompt that I got was:
PS C:\Espressif\frameworks\esp-idf-v4.4>
In the text that follows, I will just show "PS C:>" as the prompt. Now change to the hello_world subdirectory:
```
PS C:> cd examples
PS C:> cd get-started
PS C:> cd hello_world
```
Choose your target device type by executing the following command:
```
PS C:> idf.py set-target esp32c3
```
This configures the build for this project to compile for your RISC-V device. Once that completes, you can build your hello_world software:
```
PS C:> idf.py build
```
The first time you build your project a lot of compiling of dependencies will occur. On successive builds however, the process only rebuilds what is needed and is much faster. If all
went well, the command should complete with the message:
Project build complete. To flash, run this command:
...
or run 'idf.py -p (PORT) flash'

If all went well, you will see that it recognizes the device and uploads the compiled software
to it. In order to see hello_world run, we monitor it with:
```
PS C:> idf.py -p COM14 monitor
```
