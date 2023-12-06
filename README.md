## linux kernel for catdrive  

2023.12.06 update:  
 --- add github actions  
 --- update to kernel 5.4.262  
## Build steps:
### 1. github actions build:  

1. add your token to varible GH_TOKEN in this repo
2. run github actions

### 2. local PC build :

requirement: 

`sudo apt install libncurses-dev flex bison libssl-dev git gcc-aarch64-linux-gnu fakeroot build-essential ncurses-dev xz-utils libssl-dev bc flex libelf-dev bison`

local build steps:  
1. [optional] add the mac address for catdrive for your own, such as (4C:65:A8:00:00:00)  
```
--- a/linux-5.4.21/arch/arm64/boot/dts/marvell/armada-3720-catdrive.dts
+++ b/linux-5.4.21/arch/arm64/boot/dts/marvell/armada-3720-catdrive.dts
@@ -111,6 +111,7 @@
 
 &eth0 {
        phy-mode = "sgmii";
+       mac-address = [4C 65 A8 00 00 00];
        phy = <&phy0>;
        status = "okay";
 };

```
2. mkdir output  
3. make 
