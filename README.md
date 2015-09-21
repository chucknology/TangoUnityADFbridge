# TangoUnityADFbridge
Unity plugin for importing and exporting Project Tango Area Description Files.

You can use this library until this functionality is included with the Project Tango Unity SDK.
Place the .jar file in your /Android/Plugins folder in your Unity project.

```
// Import ADF
var androidJC = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
var jo = androidJC.GetStatic<AndroidJavaObject>("currentActivity");
var jc = new AndroidJavaClass("net.chucknology.tango.adftool.UnityPlugin");
jc.CallStatic("ImportAreaDescriptionFile", jo, filepath);
```

```
// Export ADF
var androidJC = new AndroidJavaClass("com.unity3d.player.UnityPlayer");
var jo = androidJC.GetStatic<AndroidJavaObject>("currentActivity");
var jc = new AndroidJavaClass("net.chucknology.tango.adftool.UnityPlugin");
jc.CallStatic("ExportAreaDescriptionFile", jo, uuid, filepathDirectory);
```
