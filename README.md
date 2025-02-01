# UserStateDetection

Libreface is a tool for facial emotion recognition and can be used on OpenSense. It enables real-time capture and analysis of facial expressions and other social signals.

## OpenSense

[OpenSense](https://github.com/ihp-lab/OpenSense) is a platform for multimodal real-time acquisition and analysis of social signals. It allows precisely synchronized capture and processing of human behavioral signals. OpenSense is built on Microsoft's [Platform for Situated Intelligence](https://github.com/microsoft/psi) and supports various sensor modules and machine learning tools. Developers can easily integrate new components. An intuitive graphical user interface simplifies the creation of application pipelines. OpenSense is freely available for academic research.

## LibreFace as an OpenSense Component

[LibreFace](https://github.com/ihp-lab/LibreFace) has been integrated as an OpenSense component allowing it to be used alongside other OpenSense elements in a zero-code setup for real-time or non-real-time inference. The source code of this component is available in the OpenSense repository. By default, execution requires CUDA support, but with this repo you don't need CUDA support because it runs on CPU.

## Prerequisites

Before installing LibreFace, ensure that the following dependencies are installed:

- Windows 10 or higher
- Python: [Download here](https://www.python.org/downloads/)
- .NET 8: [Download here](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- Microsoft Kinect SDK 2: [Download here](https://www.microsoft.com/en-us/download/details.aspx?id=44561)

## Installation & Setup

You can download this repository as a ZIP file or clone it using the following command (if you want to clone it, make sure git is installed :[Download here](https://git-scm.com/downloads))

```sh
 git clone https://github.com/BirulZ/UserStateDetection
```



### Preparation

1. Navigate to the directory where the repository was cloned.
2. Copy the `mediapipe` folder to `C:\Windows\System32`.
3. If your webcam is not yet connected, do so now.

### Starting the Application

1. Go back to the cloned repository and run `OpenSense.WPF.exe` **as an administrator**.
2. A window will open. Click on **Pipeline Editor**.
3. In the Pipeline Editor:
   - Click **File -> Open**.
   - Navigate to `UserStateDetection/PipeLineInjector`.
   - Select the file `20230825__LibreFace__Injector__AzureKinect.pipe.json`.
4. Under **Components**:
   - Go to **Media Capture** and select your camera in the **Settings**.
   - Set the **Resolution** to **1920x1080** or lower.
   - Go to **MediaPipe** and select the **Graph** file `face_landmark_front_cpu.pbtxt` in the **Settings**.
     - File path: `C:\Windows\System32\mediapipe\modules\face_landmark`.

### Running the Application

1. Select **Runner** in the ribbon menu at the top.
2. Click **Run/Stop** to start processing.

---

