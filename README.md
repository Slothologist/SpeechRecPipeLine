# SpeechRecPipeLine
Pipeline for speech recognition, covering everything from sound source localisation to natural language processing

## Disclaimer

This Speech recognition pipeline is in development and currently not recommended for use.
Requirements will most likely change in the near future; We will move away from jackaudio as sound framework to a more dedicated framework called esiaf (see https://github.com/Slothologist/esiaf_ros), which is currently beeing worked on.

## Principles

- All audio is transmitted between most stages via Jack audio (TODO: find a way to reliably match ssl to recognized speech)
- Additional information is transmitted using ROS
- Highly modular design to ensure maximum reusability and flexibility

## Stages

1. Recording
   - no special software available yet, can be done by jackaudio itself
   - (will in the future be done by an dedicated esiaf node)

1. Sound Source Localisation, Separation, Filtering
   - will most likely be based on ODAS, but no implementation yet

1. Segmentation
   - AudioSegmenter
      - Has its own repo over here: https://github.com/Slothologist/AudioSegmenter

1. Speech recognition
   - DeepSpeech4Ros
      - Has its own repo over here: https://github.com/Slothologist/DeepSpeech4Ros

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