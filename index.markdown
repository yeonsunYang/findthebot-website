---
layout: default
---

## Abstract

Team members commonly collaborate on visual documents remotely and asynchronously. Particularly, students are frequently restricted to this setting as they often do not share work schedules or physical workspaces. As communication in this setting has delays and limits the main modality to text, members exert more effort to reference document objects and understand others' intentions. We propose <span style="color:{{site.syscolor}}">**Winder**</span>, a Figma plugin that addresses these challenges through *linked tapes*&mdash;multimodal comments of clicks and voice. Bidirectional links between the clicked-on objects and voice recordings facilitate understanding tapes: selecting objects retrieves relevant recordings, and playing recordings highlights related objects. By periodically prompting users to produce tapes, <span style="color:{{site.syscolor}}">**Winder**</span> preemptively obtains information to satisfy potential communication needs. Through a five-day study with eight teams of three, we evaluated the system's impact on teams asynchronously designing graphical user interfaces. Our findings revealed that producing linked tapes could be as lightweight as face-to-face (F2F) interactions while transmitting intentions more precisely than text. Furthermore, with preempted tapes, teammates coordinated tasks and invited members to build on each others' work.

------

## System

In <span style="color:{{site.syscolor}}">**Winder**</span>, users send *linked tapes*, which are recordings of their voice and clicks on objects on the UI design. The system generates bidirectional links between voice snippets and clicked-on objects to support navigation and understanding the receiver side.

The main components of the system's interface are (a) the top bar, (b) the list of linked tapes, and (c) the transcript space.

{: .center}
![Winder next to the design for a screen of a mobile application](/assets/img/winder_main.png){: width="90%"}

### Object Highlighting on Voice Playback

When the user plays a tape, <span style="color:{{site.syscolor}}">**Winder**</span> Winder displays the version of the document when the tape was recorded, and plays the voice audio while highlighting objects as they were clicked during recording.

{: .center}
![An image of a salad in the UI design is highlighted while a recording appears to be playing in Winder.](/assets/img/winder_highlight.png){: width="90%"}

### Inline Thumbnail Images on Voice Transcripts

{: .inline}
![A transcript of a voice recording is shown with inline thumbnail images of UI design objects.](/assets/img/winder_transcript.png){: width="50%"}

{: style="float:right"}
<span style="color:{{site.syscolor}}">**Winder**</span> provides automatic transcripts of the voice recordings (generated through speech-to-text). On the transcript, it embeds thumbnail images of the objects clicked during the recording inline with the words of the transcript.

### Object-based Search of Voice Recordings

qlwnwlqnwonp qnpwqn pwqnwp npwqnpw nqp nwpqn pqnpwnp nwpqn pwqnp wnp nqwpn pqwnw pqnpw nqp nwqpnw pqnp wqnp wnqp nqwpnwqp n

------

## Results

sdqs

------

## CHI 2021 Paper (Camera-ready)

[Link to the PDF][1]

------

{: .logos}
[![Logo of KIXLAB](/assets/img/kixlab_logo.png)](https://kixlab.org)
[![Logo of KAIST](/assets/img/kaist_logo.png)](https://kaist.ac.kr)

{: .center .acknowledgement}
This research was supported by the [KAIST](https://kaist.ac.kr) UP Program.


[1]:{{site.url}}/papers/CHI2021___Winder___CameraReady.pdf
