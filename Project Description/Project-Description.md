# Team Name: BA
# Team Members: 
- Marcellina Owusu Ansah (CS)
- Anne Baldwin (CS)
# Member Emails (respectively): 
- owusuama@mail.uc.edu
- baldwiak@mail.uc.edu
# Project Topic Area: 
- Project Focus: We would like to create a new library for Arduino that is focuses on gps location based around sound (essentially a library that allows arduino robots to easily track sound)
- Abstract: Arduino is an open-source electronics platform based on easy-to-use software and hardware. Arduino boards are able to read or take in an input and turn it into an output. Our project focuses on one of it's many aspects, specifically it's GPS Echolocation property. We created a library to detect sound and classify the sound as either good/positive or bad/negative. Our approach overall is to get the robot to move, forward or backwards, towards a good sound and then away from a bad sound. There are a magnitude of reasons as to why this would be beneficial; from determining danger to acting as added on assistance for the visually impaired.  Arduino will not only be able to determine the location of danger, but they will also be able to locate beneficial environments based on sound. With the assistance of the echolocation library, we will create a new library that allows Arduino to identify a sound and determine its source by analyzing the sound of the decibels. We will start by getting the robot to respond to sound in general. After this is accomplished we will get the robot to appropriately identify if the sound is good or bad depending on the decibels we deem appropriate. The final stage would be getting the robot to notify the proper party if the sound is good or bad using LED lights and move accordingly.
- REVISION:
   * Distance between what we’re hearing and the new sound
      * If difference is below or above a certain threshold you can then say its a gunshot or not
      * Metric of distance or similarity
      * Time domain and frequency domain
      * Look up table
   * Starts by measuring decibels then compares it to what’s stored
      * Range of time -  if within range then match to sound, if not …
      * When decibel raises above a certain level then it will start in order to match to new
   * Testing
      * Sound vary and determine how much variation system can tolerate 

# Project Advisor 
- Ali Minai

