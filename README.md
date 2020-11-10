
## :+1: clay.exe 






THE UNITY VUFORIA ADD-ON, WHICH IS THE FIRST STAGE FOR THE PROJECT, WAS INSTALLED AND WHEN THE REQUESTED PICTURE WAS DISPLAYED ON THE SCREEN, THE SCREEN WAS MOVED BY THE REQUESTED 3D MODEL AND RIGGING.

  - unity vuforia is established.
  - Image named www.developer.vuforia.com mgrs.jpg uploaded
  - Rigged moving 3d model was imported and its movements were adjusted.
# dr.v1 



 As [Muhammed BAYAT](https://muhammed-bayat.github.io/site/) 




### Installation

Dillinger requires [UNİTY](https://unity3d.com/get-unity/download/) 2019.4.12f1 install.

# install vuforia and License Key
### How to Add a License Key to Your Vuforia Engine App
This article describes how to add a license key to your Vuforia Unity, Android, iOS, and UWP projects. Vuforia Engine apps use a unique license key obtained from the Vuforia Engine License Manager.  We strongly recommend developers encrypt their key for enhanced security. To learn how to create a license key, refer to the Vuforia License Manager article.

## Adding a License Key to a Unity app
-After opening your Unity project, perform the following steps:

- In the Window menu, select Vuforia Configuration.
- In the Inspector window, click the Add License button. 
- The License Manager window opens in a browser.
- Click on your project name.
- The My License window opens.
- Click the license key to copy it to your clipboard.
- In the Inspector window, paste the key into the App License Key field. 

 

 
![alt text](https://library.vuforia.com/content/dam/vuforia-library/articles/unity-ui/vuforia-configuration-vuforia-inspector.PNG/_jcr_content/renditions/cq5dam.web.1280.1280.png "Logo Title Text 1")

 

For production environments...


## Adding a License Key to a Native Vuforia Engine App
Use the AppController.cpp file in the Vuforia Engine Native Samples as a starting point. Use the following to initialize your license key. The licenseKey should be defined in the namespace of your app. Obtain the license key from the License Manager on the Vuforia Developer Portal and place it as the licenseKey that is empty by default in the Native Sample:

```sh
$ namespace
{
    constexpr char licenseKey[] = "";
}

```
### The license key is used in the initiVuforiaInternal() method when calling Vuforia::setInitParatmeters(), which has a slightly different signature for each platform:


|PLATFORM               |CODE                                               |
|----------------|-------------------------------|
|IOS  |``` Vuforia::setInitParameters(mVuforiaInitFlags, licenseKey );```          |
|ANDROİD         |``` Vuforia::setInitParameters(jobject(appData), mVuforiaInitFlags, licenseKey);  ```          |
|UWP         |```Vuforia::setInitParameters(licenseKey); ```|

 


## Related Topics
 [Vuforia License Manager](https://library.vuforia.com/content/vuforia-library/en/articles/Training/Vuforia-License-Manager.html)
  [Vuforia Target Manager]( https://library.vuforia.com/content/vuforia-library/en/articles/Training/Getting-Started-with-the-Vuforia-Target-Manager.html)
