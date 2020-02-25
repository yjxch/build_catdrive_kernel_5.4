## linux kernel for catdrive  

Porting the patch from ![hanwckf](https://github.com/hanwckf/build-catdrive)  

### steps  
1. add the mac address for catdrive for your own, such as (4C:65:A8:00:00:00)  
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
