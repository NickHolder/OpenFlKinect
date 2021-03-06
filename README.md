OpenFlKinect
============

Openfl / Haxe native extension for Microsoft Kinect for Windows SDK

**To build ndll library:**

haxelib run hxcpp Build.xml

**To compile samples:**

[haxelib run] openfl build project.xml windows

Copy KinectInteraction180_32.dll from %KINECT_TOOLKIT_DIR%/bin into same directory as .exe

## Usage

```Haxe

// Set options
d = new DeviceOptions();
d.depthEnabled = true;
d.depthResolution = ImageResolution.NUI_IMAGE_RESOLUTION_640x480;

// Create a Kinect references
k = new Kinect(d);
k.start();

// Add the image stream display list
addChild(k.bmDepth);

// call update each frame
addEventListener(Event.ENTER_FRAME, function(e)
{
  k.update();
});

```


## Dependencies

* Kinect for Windows SDK & Kinect for Windows Developer Toolkit http://www.microsoft.com/en-us/kinectforwindowsdev/Downloads.aspx
* Haxe and OpenFL http://www.openfl.org/documentation/setup/install-haxe/
* Visual Studio 2012 / Visual Studio 2012 Express (2010 Will not compile) http://www.microsoft.com/en-us/download/details.aspx?id=34673

## Depth Stream

![](https://lh4.googleusercontent.com/-_HtY04KcUTw/Uz2W7jbH6qI/AAAAAAAADZ4/dW_7oVNZ5y4/w303-h240-no/depth.png)



## Colour Stream

![](https://lh3.googleusercontent.com/-Glij7YoYaOg/Uz2W9FM6QNI/AAAAAAAADaM/s8deUGa8pO4/w301-h240-no/color.png)

## IR Stream

![](https://lh5.googleusercontent.com/-YhAzTU-m5bA/Uz2W9CP-1YI/AAAAAAAADaU/1dGobEL_KGw/w305-h240-no/ir.png)

## User Tracking

![](https://lh4.googleusercontent.com/-DiTZ9UtHUp0/Uz2W97FFHmI/AAAAAAAADac/_FCOEHmQmXE/w304-h240-no/user.png)

## Skeleton Stream

![](https://lh4.googleusercontent.com/-7KWziKIuymA/Uz2W9ODPzmI/AAAAAAAADaQ/M9X5AxCEQCg/w303-h240-no/skeleton.png)

## Interactions

![](https://lh5.googleusercontent.com/-tNBRedd49Dw/Uz2W7m1CIWI/AAAAAAAADZ8/tkN5iyPK1dM/w307-h240-no/interactions.png)
