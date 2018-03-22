# DataTjej Unity AR VT18

Welcome to a repository containing a Unity and Vuforia project in cooperation between DataTjej and Thnx Innovation for educational purposes.

At the bottom of this walkthrough one will find links to resources for Unity and Vuforia, as well as a link to a goof Unity Youtube-chanel.

## Prerequisites

To run this demo and develop with Unity and Vuforia using below instructions, Unity 2017.3 or later is needed, Vuforia 7 is included with the installer for Unity and should be installed when installing Unity.

Also, an empty and newly created Unity project is the starting point of this walkthrough.

## Step-by-Step

Below is a step-by-step walkthrough to setup Unity to use Vuforia and image tracking. Please follow [DataTjej](http://datatjej.se/) and [Thnx Innovation](http://www.thnx.se) on [Facebook](https://www.facebook.com/thnxinnovation/) and [LinkedIn](https://www.linkedin.com/company/15173156/) for upcoming Unity workshops by Thnx!

### The Begining

1. Add ARCamera (GameObject -> Vuforia -> AR Camera)
2. A popup appears, accept Import Vuforia package
3. Go in to Player Settings (Edit -> Project Settings -> Player)
4. For iOS and Android
	- In Otther Settings, set Package Name
	- In XR Settings, check the box for Vuforia Augment Reality
5. For Android:
	- Set minimum API Level to 5.1 'Lollipop'
6. For iOS:
	- Set minimum API Level to 9.0
	- Set Camera Usage Description: "Camera access required for target detection and tracking."
7. Open Vuforia configuration (Window -> Vuforia Configuration, Shift + cmd/ctrl + v)
	- Set App License Key
	- Under Databases, check only Load DataTjej Database and Activate
8. Add ImageTarget (GameObject -> Vuforia -> Camera Image -> Camera Image Target)
	- Selecte added ImageTarget, and in the Inspector
	- Set Type to Predefined
	- Set Database to DataTjej
	- Set Image Target to datatjej-target
9. Add transparent image (datatjej-logo-transp.png) to Project by draging it into the Assets-folder in Unity
10. Select imported image and in the Inspector set Texture Type to Sprite (2D and UI), and Apply
11. Add sprite to ImageTarget by draging it from Assets to the ImageTarget-gameobject
12. The added sprite is big, transform it to scale (0.1, 0.1, 0.1) and move it in y-axis to 0.36
13. Use the "Play" button lokated at the top and in the middele of Unity.
	- Print the "datatjej-target-printable.pdf" on an A4-paper.
	- Hold the pritned paper in front of the camera, the DataTjej logo should appear, if not se console for details.

### Build to device
1. Open Build Settings, File -> Build Settings (cmd/ctrl + B)
2. Switch Platform to prefered platform (iOS or Android)
3. Connect device (Android or iOS), enabled development mode (might be different between devices)
4. For Android, press "Build and Run", save apk as DataTjej-Android.apk
5. For iOS, press "Build", and save project as DataTjej-iOS
6. For iOS, open built project found in DataTjej-iOS folder named Unity-iPhone.xcodeproj, add Signing Team, and hitt play
	- Hold the pritned paper in front of the camera, the DataTjej logo should appear.

### Animation
1. Open Animation window (Window -> Animation cmd/ctrl + 6)
2. Create new Animation, "rotate" (see inspector, Animator component created)
3. Add Property, Transfor, Rotation
4. Remvoe unnecessary keys for z- and x-axis
6. Select the last Key at 1 sec, move to 2 sec, and set Rotation.y to 360
7. Open Build Settings (cmd/ctrl + B)
8. In Build Settings, press "Build and Run"
9. For iOS, press "Append"

## Links
Unity: https://unity3d.com/
Vuforia: https://www.vuforia.com/
Brackeys: https://www.youtube.com/user/Brackeys
