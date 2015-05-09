# Using the Camera on iOS

## Introduction

ARToolKit for iOS offers a wide variety of options for control of the cameras on the device, and the stream coming from them.

You can choose between rear (main) and front cameras, on devices which have more than one camera, and additionally, can request different resolution image data from the cameras. Configuration of these options is performed by use of named parameters to the arVideoOpen() function (in the -start method of the ARViewController class). See [Configuring_video_capture_in_ARToolKit_Professional][1].

Camera calibration information holds the lens model needed to get ARToolKit tracking working properly. This is pre-supplied for all current supported iOS device models, including specific calibrations for different focus-distances of the iPhone 4 and 4S rear (main) camera, and front cameras on the iPhone 4 and 4S, iPod touch 4G, iPad 2, and iPad 3. With release 10 (ARToolKit version 4.5.11), loading of these camera parameters has also been simplified by addition of support to libARvideo for directly requesting the camera parameter structure. See the release 10 release notes and look at the -start method of the ARViewController class for example usage.

Other capabilities include flipping the generated video stream vertically or horizontally.

The best guide to camera usage is to examine the example applications carefully, particulary ARViewController, as it is the class which handles most of the interaction with libARvideo. Additional helpful information can be found in the header files <AR/sys/videoiPhone>, <AR/sys/CameraVideo.h> and <AR/sys/MovieVideo.h>.

[1]: /Configuring_video_capture_in_ARToolKit_Professional#AR_VIDEO_DEVICE_IPHONE