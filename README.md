## PeakVibe-REAPER
(formerly known as kiwi-reaper) 

This is an extension for the popular digital audio workstation REAPER that broadcasts the loudness 
levels (in dB) of the currently-playing track over a local network using OSC. This is meant to be paired
with the [PeakVibe iPhone app](https://github.com/interactiveaudiolab/peakvibe-ios). PeakVibe captures 
the loudness levels being sent by REAPER over the local network and makes the iPhone vibrate, mapping 
each loudness value to a corresponding haptic intensity on the iPhone in realtime. Using this setup, 
the intensity of the loudness waveform is communicated by the vibration intensity of the iPhone’s 
haptic motor, letting the user feel the volume levels as one scrubs through the track without requiring 
the user to look at the waveform. This is helpful for blind and low vision (BVI) users and anyone else 
that needs to scrub quickly through audio and find peak levels without listening and without looking at the waveform.

# Installation
clone
```bash
git clone https://https://github.com/interactiveaudiolab/peakvibe-reaper
cd peakvibe-reaper
```

build the source code
```bash
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Debug
make -j8 install
```

after `make -j8 install`, a REAPER extension should be installed under `~/Library/Application Support/REAPER`. 

## Running with PeakVibe 

To run PeakVibe-REAPER, simply follow the installation instructions above, then launch REAPER normally. 

To run PeakVibe-REAPER, you must have an iPhone running [PeakVibe-iOS](https://github.com/interactiveaudiolab/peakvibe-ios).  
When launching REAPER with PeakVibe-REAPER installed, the first thing that will show up is a pop-up window asking for the IP address of the iPhone running PeakVibe. Enter that IP address, and PeakVibe-REAPER should connect to the iPhone after that.

Once both PeakVibe-REAPER and PeakVibe-iOS are running, you will be able to monitor the level of the currently selected audio track with Haptic feedback on your iPhone. 


