# Part I. Description of Overall Test Plan
- Our approach overall is to get the robot to move, forward or backwards, towards a good sound and then away from a bad sound. We will start by getting the robot to respond to sound in general. After this is accomplished we will get the robot to appropriately identify if the sound is good or bad depending on the decibels we deem appropriate. The final stage would be getting the robot to notify the proper party if the sound is good or bad using LED lights and move accordingly.
# Part II. Test Case Descriptions
* Motor activation
  *  Purpose: Ensures the arduino robot can move
  * Description: Short arduino program activates motors to move robot forwards and backwards to test motor sensitivity, speed, turning, etc.
  * Inputs: speed/rotations, which motor is activated
  * Expected result: robot moves forwards or backwards
  * Normal
  * Whitebox 
  * Functional
  * Unit 
  * Results: robot moves forwards or backwards
* Response to sound
  * Purpose: Ensures microphone not only works but that the robot can hear it 
  * Description: A sound is played and the arduino will activate the robots motors to indicate that it senses the sound
  * Inputs: Audio 
  * Expected result: robot moves once it hears a sound and stops when the sound stops
  * Boundary case: sound is played at different volumes and distances to determine how loud it must be for the microphones to detect it
  * Blackbox 
  * Function 
  * Unit
  * Results: robot moves once it hears a sound and stops when the sound stops
* Approach sound
  * Purpose: Ensures the robot can move toward any sound it hears 
  * Description: Robot detects sound and then activates motors to move toward detected sound
  * Inputs: Audio
  * Expected result: Robot detects sound and moves toward it
  * Boundary case: Sound is played from different angles so that robot must rotate and then start moving
  * Blackbox 
  * Performance
  * Unit 
  * Results: Robot detects sound and moves toward it
* Retreat from sound
  * Purpose: Ensures robot is able to move away from any sound it hears
  * Description: Robot detects sound and then activates motors to move away from detected sound
  * Inputs: Audio
  * Expected result: Robot detects sound and moves away from it
  * Boundary case: Sound is played from different angles so that robot must rotate and then start moving
  * Blackbox
  * Performance
  * Unit 
  * Results:  Robot detects sound and moves away from it
* Identify sound
  * Purpose: Ensures Arduino can differentiate between specific sounds (gunshots, running water)
  * Description: Specific sound is played and arduino outputs to the console what sound it is hearing
  * Inputs: Gunshot recording, waterfall recording
  * Expected output: “Gunshot” or “Water”
  * Boundary case: sound is played that is neither gunshot or water. Robot should give a null output.
  * Blackbox
  * Function
  * Integration
  * Results: “Gunshot” or “Water”
* Sound Response
  * Purpose: Ensures Arduino knows when to move away from or towards a sound
  * Description: Arduino differentiates between whether it should move toward or away from sound based on what the sound is identified as being
  * Inputs used: Gunshot/Water audio
  * Expected Results: Arduino moves away if it's a gunshot and moves toward if water
  * Boundary case: Sound is played from different angles so that robot must rotate and then start moving
  * Blackbox
  * Performance 
  * Integration
  * Results: Robot moves away if it's a gunshot and moves toward if water
* Good Notice
  * Purpose: Ensures Arduino can use LED lights when the sound is determined to be good
  * Description: Arduino notifies parties if sound is good via LED 
  * Inputs used: water sound
  * Expected Results: lights up once when the sound is good, and nothing if the sound is unknown
  * Boundary case: Sound is played from different angles so that the robot must rotate and then start moving
  * Blackbox
  * Performance
  * Integration
  * Results: lights up once when the sound is good, and nothing if the sound is unknown
* Bad Notice 
  * Purpose: Ensures Arduino can use LED lights when the sound is determined to be bad
  * Description: Arduino notifies parties if sound is bad // morse code/LED &| sound etc
  * Inputs used: gunshot sound
  * Expected Results: Arduino LED blinks when the sound is dangerous, and nothing if sound is bad
  * Boundary case: Sound is played from different angles so that the robot must rotate and then start moving.
  * Blackbox
  * Performance
  * Integration
  * Results: robot LED blinks when the sound is dangerous, and nothing if sound is bad
* Good Sound
  * Purpose: Ensures one of the goals of our project is reached 
  * Description: Arduino follows a sound for as long as the sound is above 0db
  * Inputs used: water sound
  * Expected Results: Arduino LED will light up once and move towards sound
  * Boundary case: Sound is played from different angles so that robot must rotate and then start moving
  * Blackbox
  * Performance
  * Integration
  * Results: robot LED will light up once and move towards sound
* Bad Sound
  * Purpose: Ensures the other goal of our project is reached 
  * Description: Arduino retreats from a sound for as long as the sound is above 0db
  * Inputs used: gunshot sound
  * Expected Results: Arduino LED will blink multiple times while retreating from sound
  * Boundary case: Sound is played from different angles so that robot must rotate and then start moving
  * Blackbox
  * Performance
  * Integration
  * Results: robot LED will blink multiple times while retreating from sound
