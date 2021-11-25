# U6144_SSD1306

## C code
- Environmental configuration
```
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install make
```
```
sudo apt install gcc
```
- Download library 
```bash
git clone https://github.com/hansworse/U6143_ssd1306.git
```
- Compile the source code 
```bash
cd U6143_ssd1306/C 
```
```bash
make 
```
## Run the display
```bash 
sudo ./oled-display-stats 
```

## Setup service to start display on startup.

- Copy the oled-display-stats binary to standard path binaries location.
```bash
sudo cp /home/(User name)/U6143_ssd1306/C/oled-display-stats /usr/local/sbin
```
- Copy simple service definition to systemd service configuration location.
```bash
sudo cp /home/(User name)/U6143_ssd1306/Ubuntu/oled-display-stats.service /etc/systemd/system
```
- Enable the service
```bash 
sudo systemctl enable oled-display-stats
```
- Optionally, start the service
```bash
sudo systemctl start oled-display-stats
```
- reboot your system

