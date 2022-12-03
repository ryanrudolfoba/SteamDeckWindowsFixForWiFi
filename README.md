# Steam Deck WiFi Fix for Windows

## About
This repository contains the instructions on how to fix the WiFi issue for Steam Deck running Windows.

Steam Deck running Windows 10 / Windows 11 has the dreaded issue of "ping spikes / ping latency / ping lag" when running on battery / unplugged. This makes online game unplayable when running on battery.

The issue is non-existent if Steam Deck is plugged in to charger. I've tried several power management settings, changing WiFi settings and several driver versions but this doesnt seem to fix the issue.

However after several testing I was able to find the optimal combination that works OK for my environment. I am now able to play and enjoy online games.


## Requirement
1. Realtek 8822CE Unlocked Drivers - [more info here](https://www.techpowerup.com/forums/threads/realtek-8822ce-modded-wireless-drivers-with-enabled-advanced-features.283920/)

## Downloading and Intalling the Unlocked Drivers
1. Download the archive containing the unlocked drivers [here](https://www.techpowerup.com/forums/threads/realtek-8822ce-modded-wireless-drivers-with-enabled-advanced-features.283920/) (click the link on post#2).
![image](https://user-images.githubusercontent.com/98122529/205451596-4e4d533d-6000-480a-abca-db3f0dccb8bb.png)

2. Extract the archive.
![image](https://user-images.githubusercontent.com/98122529/205451672-c5250ec8-00ad-4771-bb54-b6eadeda4700.png)

3. Go to Device Manager. Expand Network Adapters then double click Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC.
![image](https://user-images.githubusercontent.com/98122529/205451702-42416cb4-ce91-46fd-84ff-7d2b6c1f3f29.png)

4. Go to the Driver tab, then click Update Driver.
![image](https://user-images.githubusercontent.com/98122529/205451753-10da05bf-162a-40d6-b553-3915770d7b13.png)

5. Select Browse my computer for drivers.
![image](https://user-images.githubusercontent.com/98122529/205451782-7966cc04-21ee-4aa6-baea-4cc3c412a8e7.png)

6. Navigate to where the drivers were extracted and press Next
![image](https://user-images.githubusercontent.com/98122529/205451810-16def79c-0fa3-42e5-b39f-db1001ed751d.png)

7. Wait unitl driver install is finished.
![image](https://user-images.githubusercontent.com/98122529/205451824-08e80f37-1266-42f3-ab78-f76d420b5eb7.png)

8. Once the install is done it will show up as RTK Killer Wi-Fi 5 8822CE Xtreme 802.11ac PCI-E
![image](https://user-images.githubusercontent.com/98122529/205451898-8096d0ca-b365-4238-b08f-9b0f05e89aba.png)
![image](https://user-images.githubusercontent.com/98122529/205451909-e57b9415-8068-44ca-b118-49cae914617f.png)

If it doesnt install, then driver signing need to be temporarily disabled in Windows. Look at the section labelled Disable Driver Signing.

## Changing WiFi Driver Settings
1. Go to Device Manager. Expand Network Adapters then double click RTK Killer Wi-Fi 5 8822CE Xtreme 802.11ac PCI-E. If it  shows up as Realtek 8822CE Wireless LAN 802.11ac PCI-E NIC then the unlocked drivers are not yet installed. Follow the steps Downloading and Installing the Unlocked Drivers
![image](https://user-images.githubusercontent.com/98122529/205452113-0802dca7-5f0a-44a8-8b71-7feebe68cc60.png)

2. Click the Advanced tab and modify the settings
![image](https://user-images.githubusercontent.com/98122529/205452280-d7138e6f-7c06-4104-b1f4-7cd581e6c805.png)

802.11n channel width for 2.4GHz - 20MHz (this will decrease throughput / download speeds, leaving this to Auto doesnt affect throughput / download speeds)

802.11n channel width for 5.2GHz - 20MHz (this will decrease throughput / download speeds, leaving this to Auto doesnt affect throughput / download speeds)

Classroom Mode - Enabled (this might be the only option you need to change. However toggling this to ENABLED the Steam Deck won't be able to connect to 2.4GHz networks.)

Roaming Aggresiveness - Disabled (this setting reduced ping spikes / lag when Steam Deck is on a different floor than the WiFi AP. I dont have roaming on my WiFI AP. If you do use roaming, you might want to toggle this to least aggressive

Transmit Power - Medium

Wireless Mode - 802.11ac

3. Press OK to apply the settings.

## Before and After
The image on the left is a simple ping test using stock drivers.

The image on the right is a simple ping test after using the unlocked drivers and changing the WiFi settings.
Both tests are performed in the same spot - Steam Deck is on 2nd floor while WiFi AP is in a different floor.

Signal strenght is at 100% for both test, but using the stock drivers there are random ping spikes.

![image](https://user-images.githubusercontent.com/98122529/205453768-301b9e22-57ef-4574-bd78-a002a61bb9ac.png)


