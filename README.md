# IMPORTANT

This example is currently broken with the most recent version of Windows 10. Until I figure out what is wrong, I recommend that you instead look at [https://github.com/Azure-Samples/cognitive-services-onnx12-customvision-sample/](https://github.com/Azure-Samples/cognitive-services-onnx12-customvision-sample/).



# Use an ONNX file exported from the Custom Vision Service with Windows ML

This example demonstrates how to take an ONNX file that was exported from the Cognitive Services Custom Vision service, and use it in a UWP application. Specifically, this example demonstrates how to use the camera on a Windows 10 device as the image source for the model.

__IMPORTANT__: This example does not work with the Windows 10 build 17738 or higher. If you are using build 17738 or higher, see [https://github.com/Azure-Samples/cognitive-services-onnx12-customvision-sample/](
https://github.com/Azure-Samples/cognitive-services-onnx12-customvision-sample/)

## Features

* Displays a preview of what the camera sees.
* Displays the tags and score returned from the model.

## Getting Started

### Prerequisites

- Windows 10 device with a camera
- [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) (Build 17110 or higher)
- [Visual Studio](https://developer.microsoft.com/windows/downloads)

### Quickstart
(Add steps to get up and running quickly)

1. `git clone https://github.com/Azure-Samples/Custom-Vision-ONNX-UWP`
2. Open the `VisionApp.sln` file using Visual Studio.
3. Use F5 to build and run the application.
4. Point the camera at a dog or cat (or a picture of one). The score below the preview shows whether the model thinks that a dog or cat is in the scene. Values closer to 1.0 mean that the model is confident that the scene contains the object. For example, Dog - 0.99. 

    Occasionally you will see a score that contains the letter E, for example 1.7E-10. This can be confusing, as it looks like a number close to 1. The E notation represents the numbers in front of the preceding value. In the case of 1.7E-10, this equals 0.0000000017. Which means that the model thinks that the image probably isn't looking at the object.

    In a production application, you wouldn't show the raw numbers, but would probably convert to a percentage or a simple yes/no value.
