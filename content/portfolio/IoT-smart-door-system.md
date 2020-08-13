+++
categories = ["web-dev"]
coders = []
date = 2020-04-25T23:00:00Z
description = "A smart door system"
github = ["https://github.com/albero94/20_mystery-men"]
image = "https://res.cloudinary.com/aalbero/image/upload/v1597260175/raspberry-pi_zfsn48.svg"
title = "Smart Door System"
type = "post"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260162/.net_core_pxrqly.png"
name = ".NET Core"
url = "https://dotnet.microsoft.com/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260164/C_Sharp_logo_yagaj2.svg"
name = "C#"
url = "https://docs.microsoft.com/en-us/dotnet/csharp/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597329684/Azure_n8ztwk.png"
name = "Azure"
url = "https://azure.microsoft.com/en-us/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597339169/Android-Logo_dsa4ot.png"
name = "Android"
url = "https://www.android.com/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597339130/kotlin_tlswfg.png"
name = "Kotlin"
url = "https://kotlinlang.org/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260175/raspberry-pi_zfsn48.svg"
name = "Raspberyy PI"
url = "https://www.raspberrypi.org/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260175/python_onqcqa.svg"
name = "Python"
url = "https://www.python.org/"

+++

### [Clik here to watch a Demo](https://drive.google.com/open?id=1d16epz6AwzkoG-WXnCZSgXjU2IlyBvqN)

## Description
We have created a smart door application that uses face recognition. The basic description of the service is, we have a cloud application that contains the list and images of people that are allowed into the house. We have a mobile application that is used as an administrator and can add and delete people from the list and operate the door lock directly. We have an IoT system with a Raspberry PI, a camera and a lock actuator that will take a picture of the person trying to get into the house, send it to the cloud service, and operate the door if there is a match in the face.

* [Face Recognition Server](https://github.com/albero94/20_mystery-men/tree/master/FaceRecognitionServer) contains the cloud service
* [Android](https://github.com/albero94/20_mystery-men/tree/master/android) contains the mobile application
* [PI](https://github.com/albero94/20_mystery-men/tree/master/pi) contains the Raspberry PI code to manage the actuators
* [Deployment](https://github.com/albero94/20_mystery-men/tree/master/deployment) contans the files to deploy the project
* A short demo video can be found .

## Deployment
If you want to use our application, you need the following components. A hosting environment to deploy the .NET server, an Azure Face API subscription (basic is free), an android device to administrate the system, a camera, a door lock, and a Raspberry PI to operate both of them.

We have included a [Deployment](https://github.com/albero94/20_mystery-men/tree/master/deployment) folder where you can find the three projects (Cloud, Web and PI).

To deploy the cloud application
* You need to copy the files in FaceRecognitionServer to the hosting provider of your choice, we have used Azure App Services
* You need to register to [Azure Face API](https://azure.microsoft.com/en-us/services/cognitive-services/face/) to get the API keys, then include them as environment variables named AZURE_FACE_SUBSCRIPTION_KEY and AZURE_FACE_ENDPOINT
* Your cloud service is ready to use

To deploy the mobile application
* Download the [APK](https://github.com/albero94/20_mystery-men/tree/master/deployment/android/FaceMatch-Door-Lock.apk) and install on an Android Device, or build the [project](https://github.com/albero94/20_mystery-men/tree/master/android) in Android Studio and run in an emulator.

To deploy the IoT component
* Download [controller.py](https://github.com/albero94/20_mystery-men/tree/master/deployment/pi/controller.py) and run on a Raspberry Pi.
* A wiring example can be found [here](https://github.com/albero94/20_mystery-men/tree/master/deployment/pi/wiring.JPG)