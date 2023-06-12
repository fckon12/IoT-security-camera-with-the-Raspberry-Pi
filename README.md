# Door Security System with Raspberry Pi

![gif](https://i.imgur.com/ZgfokcZ.gif)

이 프로그램은 라이브 비디오의 프레임을 처리하고 감지된 얼굴을 알려진 얼굴 인코딩 집합과 비교합니다.

facewithvideo.py 파일 실행 ....!

일치하는 항목이 있는 경우 그 사람은 알려진 것으로 간주되며 아무 작업도 수행되지 않습니다.
일치하는 항목이 없으면 그 사람을 침입자로 간주하고 쉘 스크립트를 호출하여 침입자의 이미지가 포함된 이메일을 보냅니다.


Adam Geitgey의 안면 인식 API를 사용했습니다. 자세한 내용은 그의 [Github 저장소](https://github.com/ageitgey/face_recognition)를 참조하세요.

이 프로그램은 USB 웹캠이 있는 Raspberry Pi 3 B에서 실행되었습니다.

Requirements
Python 3.3+ or Python 2.7
macOS or Linux (Windows not officially supported, but might work)
Installation Options:
Installing on Mac or Linux
First, make sure you have dlib already installed with Python bindings:

How to install dlib from source on macOS or Ubuntu
Then, make sure you have cmake installed:

brew install cmake

Finally, install this module from pypi using pip3 (or pip2 for Python 2):

pip3 install face_recognition
Alternatively, you can try this library with Docker, see this section.

If you are having trouble with installation, you can also try out a pre-configured VM.

Installing on an Nvidia Jetson Nano board
Jetson Nano installation instructions
Please follow the instructions in the article carefully. There is current a bug in the CUDA libraries on the Jetson Nano that will cause this library to fail silently if you don't follow the instructions in the article to comment out a line in dlib and recompile it.
Installing on Raspberry Pi 2+
Raspberry Pi 2+ installation instructions
Installing on FreeBSD
pkg install graphics/py-face_recognition
Installing on Windows
While Windows isn't officially supported, helpful users have posted instructions on how to install this library:

@masoudr's Windows 10 installation guide (dlib + face_recognition)
Installing a pre-configured Virtual Machine image
Download the pre-configured VM image (for VMware Player or VirtualBox).


