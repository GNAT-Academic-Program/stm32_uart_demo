


### Program to Board
- Linux, MacOS:    
```console
openocd -f /usr/share/openocd/scripts/board/stm32f429disc1.cfg -c 'program bin/stm32_uart_blocking_demo verify reset exit'
```   
- Windows:
```console
openocd -f interface/stlink.cfg -f target/stm32f4x.cfg -c 'program bin/stm32_uart_blocking_demo verify reset exit'
```


### Using UART from a Shell

- Linux:

Install minicom

```
sudo apt-get install minicom
```

Execute to find correct device: Eg. On my machine its ttyACM0
```
sudo dmesg | grep tty
```

Start minicom (replace your exact device name):
```
sudo minicom -b 115200 -o -D /dev/ttyACM0
```