# SpeechRecPipeLine
Pipeline for speech recognition, covering everything from sound source localisation to natural language processing

## Principles

- All audio is transmitted between most stages via Jack audio (TODO: find a way to reliably match ssl to recognized speech)
- Additional information is transmitted using ROS
- Highly modular design to ensure maximum reusability and flexibility

## Stages

1. Recording
   - no special software available yet, can be done by jackaudio itself

1. Sound Source Localisation, Separation, Filtering
   - ODAS, needs to be adjusted

1. Segmentation
   - AudioSegmenter
      - Has its own repo over here: https://github.com/Slothologist/AudioSegmenter

1. Speech recognition
   - no software available yet

1. Natural Language Preprocessing
   - no software available yet
   
## Dependencies

### Required

- Jackaudio 
   - sudo apt install jackd2
   
- ROS
   - see http://wiki.ros.org/ROS/Installation to install ROS. I develop on Melodic, but Kinetic should be fine as well
   
- somewhat recent gcc 

### Recommended

- Catia is great for a graphical interface to configure jack
   - http://kxstudio.linuxaudio.org/Applications:Catia

### Optional

Certain parts of the pipeline can have different/ additional requirements. Be sure to check there as well!