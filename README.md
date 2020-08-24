
### 1. Depend on it  
Add this to your package's pubspec.yaml file:  
```  
import 'package:qrscan/qrscan.dart';  
```  
### iOS  
Add the the camera usage description to your Info.plist  
```xml  
<key>NSCameraUsageDescription</key>  
<string>Camera permission is required for qrcode scanning.</string>  
```  
### Android  
For Android, you must do the following before you can use the plugin:  
Add the QrCodeScannerActivity to your AndroidManifest.xml  
      `<activity android:name="com.djgeo.qrscan.g_scanner.QrCodeScannerActivity"/>`  
## Example  
 ```dart  
String qrResult = await qrscan.startScan(
    title: "掃二維碼",
    desc: '請把二維碼對準掃描區域掃碼',
    barColor: Colors.red, 
    titleColor: Colors.green, 
    qRCornerColor: Colors.blue,
    qRScannerColor: Colors.deepPurple,
    flashlightEnable: true, 
    scanAreaScale: 0.7 /// value 0.0 to 1.0
);
```
 ### Parameters
 
 **title** : Navigation bar title.
 
 **barColor** : Navigation bar color.
 
 **titleColor** : Navigation bar title color (include back icon).
 
 **qRCornerColor** : Square color.
 
 **qRScannerColor** : Scanner line color.
 
 **flashlightEnable** : Flashlight button enable flag.
 
 **scanAreaScale** : Center scan area size scale.#   c o m p o n t e n t _ q r s c a n 
 
 