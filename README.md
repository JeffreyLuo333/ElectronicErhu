# Electronic Erhu
<img src="images/FrontView.jpg" width="400" height="300"> <img src="images/BackView.jpg" width="400" height="300">

## Project Context
How can a machine emulate the nuances and emotions of human performance, instead of yielding uniform sounds that lack a personal touch? Furthermore, what design principles should govern these machines to ensure they accompany human musicians seamlessly and harmoniously on stage? Our exploratory journey of creating a human-machine orchestra begins with a foundational step: crafting an electronic instrument that is programmable so that it is capable of nuanced performance. This instrument will lay the groundwork for future exploration into advanced autonomous control within our forthcoming projects.

This ultimate goal is not just about technical synchronization but capturing the essence of musical empathy, enabling a seamless and emotive interplay between silicon and soul.

This repository contains files and guidelines associated with this project. Please feel free to utilize them.

## Project Objective
We've built an electronic version of the Chinese string instrument Erhu which utilizes a __physical bow__ as an input mechanism. This device produces MIDI signals as its output. These signals are then transmitted wirelessly using Bluetooth to a Digital Audio Workstation (DAW) for further editing, mixing, and synthesis.

The physical bow control lays the foundation for robotic arm manipulation, setting the stage for an investigation into how autonomous musical machines can observe and assimilate the nuances of human performers, encompassing both their physical movements and emotional expressions. This venture seeks to transcend mere technical precision, infusing machine performance with a personalized touch.

## Project details 
This section provides a detailed, step-by-step guide to constructing an electronic Erhu, outlining the entire process from start to finish.

This project is inspried by a [DIY e-Erhu project](https://oshwhub.com/Dr.Zhang/edrum_copy_copy). The microprocessor utilized in the initial project has reached its end-of-life (EOL), necessitating updates to the circuit design to accommodate a newer version of the processor. Furthermore, the software requires additional refinement to generate MIDI outputs that more precisely capture aspects such as pitch, timbre, dynamics, and the articulation of notes.

### Architecture

This project entails crafting an electronic erhu utilizing the ESP32 module, enabling it to establish a Bluetooth connection with the "GarageBand" app on an iPhone to produce music.
The main control module uses ESP32, and its core components are 16 mechanical keyboard keys and an EC11 encoder.

<img src="images/SystemView1.png" width="400" height="300"> <img src="images/SystemView0.png" width="400" height="300">

Here are the links for additional resources and learning materials:
- [MCP ESP32](https://www.espressif.com/en/products/socs/esp32)
- [Bluetooth LE MIDI Specification](https://www.midi.org/specifications-old/item/bluetooth-le-midi)
- [Free Circuit Board Design & Process](https://lceda.cn/editor) for modifing the PCB design.
- [Espressif IoT Development Framework](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/#installation) for modifying ESP32 software.
- [ESP32 Download Tool](https://www.espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=13) for downloading firmware to the target board. 

### Hardware Design & Instructions to Build an E-Erhu: 
[DIY electornic erhu project](https://oshwhub.com/Dr.Zhang/edrum_copy_copy) provides comprehensive information on hardware design and step-by-step instructions for constructing an E-Erhu.
Here are my additional notes:
- Soldering Component 16 can be a bit challenging. You may find it helpful to use a scope to ensure precise soldering.

    <img src="images/Component16.jpg" width="200" height="200">
    <img src="images/ScopeView.jpg" width="200" height="200">

- It's worth mentioning that a standard encoder produces a clicking sound and vibrations when rotated. To resolve this matter, the encoder needs to be disassembled using appropriate tools, and its components should be removed one by one. Locate the innermost spring piece and use tweezers to depress these two spring components. Subsequently, reassemble all the components in the correct sequence and seal the encoder. Removing this spring enhances the encoder's rotational smoothness.

### Firmware:
The [Original Software Source Code](https://github.com/ospanic/eerhu) can be found at: https://github.com/ospanic/eerhu. I have also cloned it to the "eerhu" folder. Additionally, Eerhu_V0.1.bin is a precompiled target image that can be downloaded to the target board using the [ESP32 Download Tool](https://www.espressif.com/en/support/download/other-tools?keys=&field_type_tid%5B%5D=13).

<img src="images/Download.png" width="400" height="300">

### Integration:
To connect your electronic erhu, open the GarageBand app on your mobile phone, then tap on "Settings" -> "Advanced" -> "Bluetooth MIDI Devices." With a little practice, I hope you'll soon find joy in playing.

__Demo__

https://github.com/JeffreyLuo333/ElectronicErhu/assets/114297879/c262f2a7-2b90-4fbd-84d1-cd86bc75b108



