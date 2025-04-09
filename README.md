## What it is
This is a custom build of the popular digital audio workstation REAPER that broadcasts the loudness 
levels (in dB) of the currently-playing track over a local network using OSC. This is meant to be paired
with the [PeakVibe iPhone app](https://github.com/interactiveaudiolab/peakvibe-ios). PeakVibe captures 
the loudness levels being sent by REAPER over the local network and makes the iPhone vibrate, mapping 
each loudness value to a corresponding haptic intensity on the iPhone in realtime. Using this setup, 
the intensity of the loudness waveform is communicated by the vibration intensity of the iPhone’s 
haptic motor, letting the user feel the volume levels as one scrubs through the track without requiring 
the user to look at the waveform. This is helpful for blind and low vision (BVI) users and anyone else 
that needs to scrub quickly through audio and find peak levels without listening and without looking at the waveform.


## Building the source code

```bash
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Debug
make -j install
```
## Installing

## Running with PeakVibe 
