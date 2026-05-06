This is a collection of useful methods for future years of Thunderbots to use!!!

Feel free to copy the template repository for your own repository. Please use your team name (and maybe year) to keep organized.

To use the database, first create a java class on the robot (or Android Studio) with the name RobotDataBase. 
Then copy the data base from the doc or GitHub and paste it into the RobotDataBase class. 
Then create a Teleop or Autonomous, and in the teleop declare the database as: RobotDataBase robotDataBase;. 
Then during initialization initialize it by writing: robotDataBase = new RobotDataBase(this);.
To call methods from the database write: robotDataBase.methodName();.

Description of all methods:

RobotDataBase(OpMode opMode)
DO NOT CHANGE THIS!!!!!!!!!!!
This is what allows the database to be active in other classes andd files.

init()
This is code that initializes all motors, servos and devices, as well as directions and modes.

PFTUNER(double wantedValue, double currentValue, double P, double F)
This is a method to make your motors more responsive and cause less oscillilation.

rangeCheck(double value, double min, double max)
This method allows a value to be set to a min or max if it does not fall into the wanted range.

MechanumMoving(double forward, double sideways, double turn)
This is the standard movement code for a Mechanum drive base (likely what you'll be using).
Put the gamepad inputs you want in the method corresponding to the direction you want robot to move.

fieldRelativeDrive(double forward, double sideways, double turn)
This is an upgraded movement code for Mechnum that makes it based off of the field rather than the direction the robot is facing
Put the gamepad inputs you want in the method corresponding to the direction you want robot to move.

driveTelemetry()
Provides feedback of the power being applied to the drive motors.

LinearSlideMovement(double move, boolean clawOn, int clawPos, boolean wristOn, int wristPos)
Code for slide movement in two directions.
Have a move be a stick, the booleans be buttonWasPressed and Pos are set values for the servos.

fly(boolean active)
Code for a flywheel (with PFTUNER method example inside).

boolean REDAlliance
A boolean for Alliance related methods and systems.

setAlliance(boolean redInput, boolean blueInput)
Method to change above boolean.
Highly untested.
Must be put during initilization.

