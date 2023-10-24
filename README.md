# 4-legged-Dancing-Robot-
4-legged Dancing Robot using Arduino and Android Studios 
# Arduino Code
//Description:

The simple four-legged robot is a small-scale robotic platform designed to showcase basic robotic principles and provide an accessible introduction to robotics and electronics. Built around the Arduino Uno microcontroller, this robot features four legs, each actuated by a servo motor, allowing it to perform a range of basic movements and tasks. While it may not be as advanced as more complex robots, it serves as an excellent starting point for beginners in robotics and programming.

Key Components:

Arduino Uno: The central control unit of the robot, responsible for processing commands and controlling servo motors.

Servo Motors (4): Each leg of the robot is equipped with a servo motor, allowing for precise control over leg movements.

Functionalities:

Basic Locomotion: The robot can perform essential locomotion tasks such as walking forward, backward, turning, and stopping. These movements are achieved by coordinating the servo motor movements.

Manual Control: Through a user interface, typically implemented using Bluetooth or a simple remote control, users can command the robot to move in different directions or perform predefined actions.

Learning Platform: The robot serves as an educational tool for individuals interested in robotics and electronics. It provides hands-on experience in building, programming, and controlling a basic robot.

Applications:

Education: The primary purpose of this robot is to be an educational tool. It can be used in schools, workshops, or DIY projects to teach students and beginners the fundamentals of robotics, programming, and electronics.

STEM Learning: The robot is ideal for STEM (Science, Technology, Engineering, and Mathematics) programs and competitions, inspiring young minds to explore the world of robotics and engineering.

Prototyping: It can be used as a prototyping platform for experimenting with different sensors, components, and control algorithms. Developers can use it as a basis for more advanced robotics projects.

Entertainment: The simple four-legged robot can be a fun and entertaining project for hobbyists and robot enthusiasts. It can be programmed to perform tricks, dance, or respond to commands.

Research: While not suitable for complex research tasks, it can serve as a basic platform for experimenting with movement algorithms, sensor integration, and basic AI concepts.

Overall, the simple four-legged robot with an Arduino Uno is an entry-level robotics project with educational and prototyping value. It introduces beginners to the world of robotics and lays the foundation for more advanced robot-building endeavors.




User
Detailed Description of the Code:

    Libraries and Servo Initialization: The code begins by including the Servo library and initializing five Servo objects, which are used to control servo motors.

    Pin Definitions: It defines the pins for the ultrasonic sensor's trigger and echo pins and initializes a boolean variable obstacleDetected to keep track of whether an obstacle has been detected.

    Setup Function: In the setup() function, the code attaches the Servo objects to specific pins, sets the trigger pin as an output, and the echo pin as an input. It also initializes serial communication for Bluetooth communication.

    Loop Function: The loop() function is the main program loop that continuously checks for incoming serial commands from a connected device (like a smartphone or computer).

    Command Processing: Depending on the received command (e.g., 'F' for forward, 'B' for backward, etc.), the code calls corresponding functions to control the servo motors.

    Performing Dance Moves: The code includes a performRandomDanceMoves() function that generates random dance moves by calling the movement functions (forward, backward, left, right) for a set duration, creating a dancing effect.

    Movement Functions: There are various functions (accelerateForward(), accelerateBackward(), accelerateLeft(), accelerateRight(), FWaccelerate(), BWaccelerate(), M1(), and M2()) that control the movement of the robot by manipulating the servo motor angles.

    Obstacle Detection: The code implements obstacle detection using an ultrasonic sensor. The obstacleDetection() function rotates the sensor to scan for obstacles and calls detectObstacle() to check if there's an obstacle within a specified distance.

    Detect Obstacle Function: The detectObstacle() function triggers the ultrasonic sensor, measures the distance to the obstacle, and compares it with a threshold value. If an obstacle is detected, it stops the robot and sets the obstacleDetected flag to true.

Potential Applications:

The code you provided seems to be the control logic for a robot that uses servo motors for movement and an ultrasonic sensor for obstacle detection. Here are some potential applications for this type of robot:

    Educational Robotics: This code can be used to teach robotics and programming concepts to students. It's a great way to demonstrate how servo motors and sensors can be used to control a robot's movements and avoid obstacles.

    Prototyping and Testing: Robotics enthusiasts and engineers can use this code as a starting point for prototyping and testing robot designs. It allows for quick experimentation with different movement patterns and obstacle avoidance strategies.

    Robotic Art and Entertainment: Robots that can perform dance moves or interact with audiences in creative ways are used in art installations and entertainment shows. This code could be a foundation for creating such robots.

    Home Automation: With some modifications, this robot could be adapted for home automation tasks like remote surveillance, where it can move around a space and detect intruders or anomalies.

    Research and Exploration: Robots with obstacle avoidance capabilities are used in research and exploration scenarios, such as exploring hazardous environments or conducting experiments in remote locations.

    Hobbyist Projects: Robotics hobbyists can use this code as a basis for building their own custom robots, adding additional features and sensors to suit their specific needs and interests.

It's important to note that the code you provided serves as a control system for the robot's movements and obstacle detection. The specific application will depend on how the robot is built and any additional hardware or sensors integrated into it.
User
even wite about using andriod studios 
ChatGPT

Certainly, if you want to control your robot using an Android app developed in Android Studio, you'll need to establish communication between the Android app and the robot. Here's a general overview of how you can achieve this:
Using Android Studio for Robot Control:

    Design the Android App Interface: In Android Studio, design the user interface (UI) of your Android app. You can use buttons, sliders, or any other UI elements to send commands to the robot. For example, you might have buttons for "Forward," "Backward," "Left," "Right," "Stop," and "Scan for Obstacles."

    Establish Bluetooth Communication: To send commands from your Android app to the robot, you'll typically use Bluetooth communication. You need to pair your Android device with the Bluetooth module on your robot. Android Studio provides APIs for Bluetooth communication. You can use the BluetoothAdapter class to manage the device's Bluetooth functionality and the BluetoothSocket class to establish a connection.

    Send Commands: When a button or UI element in your Android app is clicked or interacted with, send a corresponding command over the Bluetooth connection. For example, if the "Forward" button is pressed, send the command 'F' to the robot. Similarly, send 'B' for backward, 'L' for left, 'R' for right, and so on.

    Receive Feedback: Depending on your robot's capabilities, you can also receive feedback from the robot and display it on your Android app. For instance, if your robot has sensors, it can send sensor data (e.g., distance measurements) back to the Android app, which can then be displayed on the screen.

    Implement Error Handling: Implement error handling in your Android app to deal with issues such as a lost Bluetooth connection or failed command execution. You can display error messages to the user or attempt to reconnect to the robot automatically.

    User Interface for Obstacle Detection: If your robot has obstacle detection capabilities, you can create a separate screen or UI element in your Android app to display real-time data from the robot's sensors, allowing the user to visualize obstacles.

    Testing and Debugging: Thoroughly test your Android app and robot to ensure that commands are transmitted accurately, and the robot responds as expected. Use Android Studio's debugging tools to identify and fix any issues.

    Deployment: Once your Android app is ready, you can deploy it to your Android device, such as a smartphone or tablet.

Benefits of Using Android Studio:

Using Android Studio for robot control offers several advantages:

    User-Friendly Interface: Android Studio allows you to create a user-friendly and visually appealing interface for controlling the robot, making it accessible to a wide range of users.

    Wireless Control: Bluetooth communication enables wireless control of the robot, making it convenient and eliminating the need for physical connections.

    Feedback and Visualization: You can use the Android app to receive real-time feedback from the robot, which can be displayed graphically, allowing users to make informed decisions while controlling the robot.

    Expandability: Android Studio provides a powerful development environment, making it easy to expand your app's functionality over time. You can add features like voice control, mapping, or automation.

    Integration with Other Android Features: You can leverage other features of Android devices, such as GPS, camera, and voice recognition, to enhance your robot control app's capabilities.

Overall, using Android Studio for robot control enables you to create a versatile and user-friendly interface for interacting with your robot, making it suitable for various applications, including education, hobbyist projects, and more give this info in scroll bar
//
#include <Servo.h>

Servo servoLeg1;
Servo servoLeg2;
Servo servoLeg3;
Servo servoLeg4;
Servo servoRot;

int trigPin = 11; // Trig pin of the ultrasonic sensor
int echoPin = 12; // Echo pin of the ultrasonic sensor
bool obstacleDetected = false;

void setup() {
  servoLeg1.attach(3); // Connect servoLeg1 to pin 3
  servoLeg2.attach(5); // Connect servoLeg2 to pin 5
  servoLeg3.attach(6); // Connect servoLeg3 to pin 6
  servoLeg4.attach(9); // Connect servoLeg4 to pin 9
  servoRot.attach(10); // Connect servoRot to pin 10

  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);

  // Initialize Bluetooth communication
  Serial.begin(9600);
}

void loop() {
  if (Serial.available() > 0) {
    char command = Serial.read();

    // Control servo angles based on received commands
    if (command == 'F') {
      accelerateForward();
    } else if (command == 'B') {
      accelerateBackward();
    } else if (command == 'L') {
      accelerateLeft();
    } else if (command == 'R') {
      accelerateRight();
    } else if (command == 'E') {
      FWaccelerate();
    } else if (command == 'A') {
      BWaccelerate();
    } else if (command == 'C') {
      M1();
    } else if (command == 'D') {
      M2();
    } else if (command == 'J') {
      obstacleDetection();
    } else if (command == 'V') {
      accelerateForward();
      accelerateBackward();
      accelerateLeft();
      servoRot.write(90);
      obstacleDetection();
      servoRot.write(90);
      accelerateBackward();
      servoRot.write(90);
      FWaccelerate();
      BWaccelerate();
      M1();
      M2();
    } else if (command == 'K') {
      servoRot.write(90);
    } else if (command == 'G') {
      // Start random dance moves
      performRandomDanceMoves();
    }
    else if(command == 'H' ){
      newobstacleDetection();

    }
    else if(command == 'p' ){
      null();

    }
  }
}

void performRandomDanceMoves() {
  for (int i = 0; i < 10; i++) { // Perform 10 random dance moves
    int randomMove = random(1, 8); // Generate a random move (1 to 4)

    switch (randomMove) {
      case 1:
        accelerateForward();
        break;
      case 2:
        accelerateBackward();
        break;
      case 3:
        accelerateLeft();
        break;
      case 4:
        accelerateRight();
        break;
      case 5:
      newobstacleDetection();
      break;
      case 6:
      M2();
      break;
      case 7:
      servoRot.write(90);

    }

    delay(1000); // Delay for 1 second between moves
  }
  // Stop the robot after the dance
  servoLeg1.write(90);
  servoLeg2.write(90);
  servoLeg3.write(90);
  servoLeg4.write(90);
}

void accelerateBackward() {
  // Decrease servo angles for backward acceleration
  for (int i = 180; i >= 90; i--) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(5);
  }
  for (int i = 0; i <= 90; i++) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(5);
  }
}

void accelerateForward() {
  // Increase servo angles for forward acceleration
   for (int i = 0; i <= 180; i++) {
    servoLeg1.write(i);
    servoLeg4.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    delay(2);
  }
  for (int i = 180; i >= 0; i--) {
    servoLeg3.write(i);
    servoLeg2.write(i);
    servoLeg4.write(i);
    servoLeg1.write(i);
    delay(2);
  }
}

void accelerateLeft() {
  // Implement the left-turn movement
   for (int i = 90; i >= 0; i--) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    delay(5);
  }
  for (int i =0; i <=90; i++) {
    servoLeg2.write(i);
    servoLeg1.write(i);
    delay(5);
  }
}
 
void accelerateRight() {
  // Implement the right-turn movement

  for (int i = 90; i >= 0; i--) {
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(5);
  }
  for (int i = 0; i <= 90; i++) {
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(5);
  }
}

void FWaccelerate() {
  // Implement forward-left movement
  for (int i = 90; i >= 0; i--) {
    servoLeg2.write(i);
    servoLeg3.write(i);
    delay(7);
  }
  for (int i = 90; i <= 180; i++) {
    servoLeg2.write(i);
    servoLeg3.write(i);
    delay(7);
  }
}

void BWaccelerate() {
  // Implement backward-left movement
   for (int i = 180; i >= 90; i--) {
    servoLeg1.write(i);
    servoLeg4.write(i);
    delay(5);
  }
  for (int i = 0; i <= 90; i++) {
    servoLeg1.write(i);
    servoLeg4.write(i);
    delay(5);
  }
}

void M1() {
  // Implement movement 1
  for (int i = 180; i >= 0; i--) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(15);
  }
  for (int i = 0; i <= 180; i++) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(15);
  }
}

void M2() {
  for (int i = 0; i <= 160; i++) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(15);
  }
  for (int i = 180; i >= 0; i--) {
    servoLeg1.write(i);
    servoLeg2.write(i);
    servoLeg3.write(i);
    servoLeg4.write(i);
    delay(15);
  }
}

void obstacleDetection() {
  // Implement obstacle detection logic
  bool isIncreasing = true; // Flag to control sweep direction

  for (int i = 90; i <= 180; i += 20) {
    servoRot.write(i);
    delay(100);
    if (!obstacleDetected) {
      detectObstacle();
    }
  }

  isIncreasing = !isIncreasing; // Reverse direction

  for (int i = 180; i >= 0; i -= 20) {
    servoRot.write(i);
    delay(1000);
    if (!obstacleDetected) {
      detectObstacle();
    }
  }

  isIncreasing = !isIncreasing; // Reset direction
}

void detectObstacle() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(2);
  digitalWrite(trigPin, LOW);

  long duration = pulseIn(echoPin, HIGH);
  float distance_cm = duration / 58.0;

  // Set a threshold for obstacle detection (adjust as needed)
  float thresholdDistance_cm = 20.0;

  if (distance_cm < thresholdDistance_cm) {
    // Obstacle detected, stop the motors and set the obstacleDetected flag
    Serial.println("Obstacle detected at angle: " + String(servoRot.read()) + " degrees");
    servoLeg1.write(90); // Stop the motors by setting them to a neutral position
    servoLeg2.write(90);
    servoLeg3.write(90);
    servoLeg4.write(90);
    obstacleDetected = true;
  } else {
    // Obstacle not detected, reset the flag
    obstacleDetected = false;
    Serial.println("Obstacle not detected at angle: " + String(servoRot.read()) + " degrees");
  }
}
void newobstacleDetection() {
  // Rotate the servo motor from 0 to 180 degrees
  for (int i = 0; i <= 180; i+=20) {
    servoRot.write(i);
    delay(100);
    detectObstacle();
  }

  // Rotate the servo motor from 180 to 0 degrees
  for (int i = 180; i >= 0; i-=20) {
    servoRot.write(i);
    delay(1000);
    newdetectObstacle();
  }
}

void newdetectObstacle() {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  long duration = pulseIn(echoPin, HIGH);
  float distance_cm = duration / 58.0;

  // Set a threshold for obstacle detection (adjust as needed)
  float thresholdDistance_cm = 20.0;

  if (distance_cm < thresholdDistance_cm) {
    // Obstacle detected, implement appropriate action here
    // For example, stop the robot, change direction, or send a message
    Serial.println("Obstacle detected at angle: " + String(servoRot.read()) + " degrees");
    Serial.println();
    // Add code to handle the obstacle detection at this angle
  }
  else{
    Serial.println("Obstacle not detected at angle?::?: " + String(servoRot.read()) + " degrees");
    Serial.println();
    Serial.println();
  }
}
void null(){
  servoLeg1.write(0); // Connect servoLeg1 to pin 3
  servoLeg2.write(0); // Connect servoLeg2 to pin 5
  servoLeg3.write(0); // Connect servoLeg3 to pin 6
  servoLeg4.write(0); // Connect servoLeg4 to pin 9
  servoRot.write(0); 
}

****And Code for Andriod Studios using Java****
activity_main.XML1
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <Button
        android:id="@+id/connectButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn"
        android:text="Connect"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.083"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.086" />

    <Button
        android:id="@+id/disconnectButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn"
        android:onClick="onDisconnectClick"
        android:text="Disconnect"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.945"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.087" />

    <Button
        android:id="@+id/forwardButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_2"
        android:onClick="sendForwardCommand"
        android:text="Forward"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.463"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.408" />

    <Button
        android:id="@+id/backwardButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_3"
        android:onClick="sendBackwardCommand"
        android:text="Backward"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.478"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.562" />

    <Button
        android:id="@+id/leftButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_1"
        android:onClick="sendLeftCommand"
        android:text="Left"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.755"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.478" />

    <Button
        android:id="@+id/rightButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_1"
        android:onClick="sendRightCommand"
        android:text="Right"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.173"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.478" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="98dp"
        android:layout_height="106dp"
        android:src="@drawable/img2"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.059" />

    <!-- Add buttons for other commands similarly -->

    <TextView
        android:id="@+id/textView"
        android:layout_width="298dp"
        android:layout_height="54dp"
        android:layout_marginStart="182dp"
        android:layout_marginTop="44dp"
        android:layout_marginEnd="171dp"
        android:layout_marginBottom="87dp"
        android:text="ArdiRot Controller"
        android:textSize="30sp"
        app:layout_constraintBottom_toTopOf="@+id/forwardButton"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.404"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/imageView"
        app:layout_constraintVertical_bias="0.04" />

    <Button
        android:id="@+id/fun1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/rnd_btn"
        android:onClick="sendDanceMod"
        android:text="Dance Mode"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.056"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.734" />

    <Button
        android:id="@+id/fun2"
        android:layout_width="82dp"
        android:layout_height="44dp"
        android:background="@drawable/rnd_btn"
        android:onClick="sendFunc"
        android:text="func"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.522"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.736" />

    <Button
        android:id="@+id/obst"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_3"
        android:onClick="sendObst"
        android:text="Obstacle Detection"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.85" />

    <Button
        android:id="@+id/Pos"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="@drawable/btn_1"
        android:onClick="pos"
        android:text="Pos 90'"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.911"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.74" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="163dp"
        android:layout_marginTop="23dp"
        android:layout_marginEnd="157dp"
        android:layout_marginBottom="31dp"
        android:text="Next"
        android:background="@drawable/btn"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/obst" />

</androidx.constraintlayout.widget.ConstraintLayout>

MainActivity-1
package com.example.myapplication;

import android.app.Activity;
import android.bluetooth.BluetoothAdapter;
import android.bluetooth.BluetoothDevice;
import android.bluetooth.BluetoothSocket;
import android.content.Intent;
import android.content.pm.PackageManager;
import android.os.Bundle;
import android.os.Handler;
import android.view.Menu;
import android.view.View;
import android.widget.Button;
import android.widget.Toast;

import androidx.core.app.ActivityCompat;

import java.io.IOException;
import java.util.UUID;

public class MainActivity extends Activity {

    private BluetoothAdapter bluetoothAdapter;
    private BluetoothSocket bluetoothSocket;
    private boolean isConnected = false;

    private final String HC_05_ADDRESS = "98:D3:21:F8:03:84";
    private final UUID HC_05_UUID = UUID.fromString("00001101-0000-1000-8000-00805F9B34FB");
private  Button button;
    private final Handler handler = new Handler();

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
       bluetoothAdapter  = BluetoothAdapter.getDefaultAdapter();

        Button connectButton = findViewById(R.id.connectButton);
        Button disconnectButton = findViewById(R.id.disconnectButton);
        button =(Button) findViewById(R.id.button);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent i=new Intent(MainActivity.this, MainActivity2.class);
                startActivity(i);
            }
        });

        connectButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (!isConnected) {
                    connectToBluetooth();
                }
            }
        });

        disconnectButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (isConnected) {
                    disconnectBluetooth();
                }
            }
        });
    }



    private void connectToBluetooth() {
        // Check if Bluetooth is enabled.
        if (!bluetoothAdapter.isEnabled()) {
            showToast("Please enable Bluetooth.");
            return;
        }

        // Check if the device has the BLUETOOTH_CONNECT permission.
        if (ActivityCompat.checkSelfPermission(getApplicationContext(), android.Manifest.permission.BLUETOOTH_CONNECT) != PackageManager.PERMISSION_GRANTED) {
            ActivityCompat.requestPermissions(this, new String[]{android.Manifest.permission.BLUETOOTH_CONNECT}, 1);
            return;
        }

        // Get the BluetoothDevice object for the HC-05 device.
        BluetoothDevice device = bluetoothAdapter.getRemoteDevice(HC_05_ADDRESS);

        // Create a new BluetoothSocket object for the HC-05 device.
        try {
            bluetoothSocket = device.createRfcommSocketToServiceRecord(HC_05_UUID);
        } catch (IOException e) {
            showToast("Failed to create BluetoothSocket: " + e.getMessage());
            return;
        }

        // Connect to the HC-05 device in a separate thread.
        new Thread(new Runnable() {
            @Override
            public void run() {
                try {
                    if (ActivityCompat.checkSelfPermission(getApplicationContext(), android.Manifest.permission.BLUETOOTH_CONNECT) != PackageManager.PERMISSION_GRANTED) {
                        // TODO: Consider calling
                        //    ActivityCompat#requestPermissions
                        // here to request the missing permissions, and then overriding
                        //   public void onRequestPermissionsResult(int requestCode, String[] permissions,
                        //                                          int[] grantResults)
                        // to handle the case where the user grants the permission. See the documentation
                        // for ActivityCompat#requestPermissions for more details.
                        return;
                    }
                    bluetoothSocket.connect();
                    isConnected = true;
                    handler.post(new Runnable() {
                        @Override
                        public void run() {
                            showToast("Connected to HC-05");
                        }
                    });
                } catch (IOException e) {
                    isConnected = false;
                    handler.post(new Runnable() {
                        @Override
                        public void run() {
                            showToast("Failed to connect to HC-05: " + e.getMessage());
                        }
                    });
                }
            }
        }).start();
    }
    public void sendForwardCommand(View view) {
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('F');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }
    }
    public void sendBackwardCommand(View view) {
        // Implement logic for sending 'B' character for backward action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('B');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }
    }

    public void sendLeftCommand(View view) {
        // Implement logic for sending 'L' character for left action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('L');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            
    }

    public void sendRightCommand(View view) {
        // Implement logic for sending 'R' character for right action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('R');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }

    }
    public void sendDanceMod(View view) {
        // Implement logic for sending 'R' character for right action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('G');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }

    }
    public void sendFunc(View view) {
        // Implement logic for sending 'R' character for right action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('V');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }

    }

    public void sendObst(View view) {
        // Implement logic for sending 'R' character for right action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('H');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }

    }

    public void pos(View view) {
        // Implement logic for sending 'R' character for right action
        if (isConnected) {
            try {
                // Send the 'F' character to the Arduino for forward action
                bluetoothSocket.getOutputStream().write('K');
            } catch (IOException e) {
                showToast("Error sending command to Arduino: " + e.getMessage());
            }
        } else {
            showToast("Not connected to HC-05. Click the Connect button first.");
        }

    }


    private void disconnectBluetooth() {
        try {
            bluetoothSocket.close();
            isConnected = false;
            showToast("Disconnected from HC-05");
        } catch (IOException e) {
            showToast("Error while disconnecting: " + e.getMessage());
        }
    }

    private void showToast(String message) {
        Toast.makeText(getApplicationContext(), message, Toast.LENGTH_SHORT).show();
    }
}

main_activity XML -2
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2">

    <ScrollView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:layout_editor_absoluteX="38dp"
        tools:layout_editor_absoluteY="331dp">


        <TextView
            android:id="@+id/projectInfoTextView"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:padding="16dp"
            android:text="Project Title:\n\n"
            android:textSize="18sp" />

    </ScrollView>
</androidx.constraintlayout.widget.ConstraintLayout>
Mainactivity Java-2
package com.example.myapplication;

import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.os.Handler;
import android.view.Menu;
import android.view.MenuItem;
import android.view.View;
import android.view.animation.AlphaAnimation;
import android.view.animation.Animation;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
        TextView projectInfoTextView = findViewById(R.id.projectInfoTextView);
        StringBuilder projectInfo = new StringBuilder();

        projectInfo.append("Project Title: Four-Legged Robot with Obstacle Detection\n\n");
        projectInfo.append("Description:\n");
        projectInfo.append("This project focuses on building a versatile four-legged robot that can move in multiple directions ");
        projectInfo.append("and detect obstacles in its path. The robot is powered by an Arduino Uno microcontroller and ");
        projectInfo.append("uses five mini servo motors for leg movement. An ultrasonic sensor is employed to detect obstacles ");
        projectInfo.append("in front of the robot, allowing it to autonomously avoid collisions.\n\n");

        projectInfo.append("Key Components:\n");
        projectInfo.append("1. Arduino Uno: The brain of the robot, responsible for processing commands and controlling servo motors.\n");
        projectInfo.append("2. Mini Servo Motors (5): These servo motors control the robot's leg movements, enabling it to walk and turn.\n");
        projectInfo.append("3. Ultrasonic Sensor: The ultrasonic sensor, with a trigger and echo pin, is used for obstacle detection.\n");
        projectInfo.append("4. External Power Supply (9V): The robot requires an external power supply to operate effectively.\n");
// Add more key components as needed

        projectInfo.append("Code Overview:\n");
        projectInfo.append("Libraries and Servo Initialization: The code begins by including the Servo library and initializing five Servo objects, which are used to control servo motors.\n");
        projectInfo.append("Pin Definitions: It defines the pins for the ultrasonic sensor's trigger and echo pins and initializes a boolean variable obstacleDetected to keep track of whether an obstacle has been detected.\n");
        projectInfo.append("Setup Function: In the setup() function, the code attaches the Servo objects to specific pins, sets the trigger pin as an output, and the echo pin as an input. It also initializes serial communication for Bluetooth communication.\n");
        projectInfo.append("Loop Function: The loop() function is the main program loop that continuously checks for incoming serial commands from a connected device (like a smartphone or computer).\n");
        projectInfo.append("Command Processing: Depending on the received command (e.g., 'F' for forward, 'B' for backward, etc.), the code calls corresponding functions to control the servo motors.\n");
        projectInfo.append("Performing Dance Moves: The code includes a performRandomDanceMoves() function that generates random dance moves by calling the movement functions (forward, backward, left, right) for a set duration, creating a dancing effect.\n");
        projectInfo.append("Movement Functions: There are various functions (accelerateForward(), accelerateBackward(), accelerateLeft(), accelerateRight(), FWaccelerate(), BWaccelerate(), M1(), and M2()) that control the movement of the robot by manipulating the servo motor angles.\n");
        projectInfo.append("Obstacle Detection: The code implements obstacle detection using an ultrasonic sensor. The obstacleDetection() function rotates the sensor to scan for obstacles and calls detectObstacle() to check if there's an obstacle within a specified distance.\n");
        projectInfo.append("Detect Obstacle Function: The detectObstacle() function triggers the ultrasonic sensor, measures the distance to the obstacle, and compares it with a threshold value. If an obstacle is detected, it stops the robot and sets the obstacleDetected flag to true.\n");

        projectInfo.append("Potential Applications:\n");
        projectInfo.append("The code you provided serves as a control system for the robot's movements and obstacle detection. Here are some potential applications for this type of robot:\n");
        projectInfo.append("1. Educational Robotics: This code can be used to teach robotics and programming concepts to students. It's a great way to demonstrate how servo motors and sensors can be used to control a robot's movements and avoid obstacles.\n");
        projectInfo.append("2. Prototyping and Testing: Robotics enthusiasts and engineers can use this code as a starting point for prototyping and testing robot designs. It allows for quick experimentation with different movement patterns and obstacle avoidance strategies.\n");
        projectInfo.append("3. Robotic Art and Entertainment: Robots that can perform dance moves or interact with audiences in creative ways are used in art installations and entertainment shows. This code could be a foundation for creating such robots.\n");
        projectInfo.append("4. Home Automation: With some modifications, this robot could be adapted for home automation tasks like remote surveillance, where it can move around a space and detect intruders or anomalies.\n");
        projectInfo.append("5. Research and Exploration: Robots with obstacle avoidance capabilities are used in research and exploration scenarios, such as exploring hazardous environments or conducting experiments in remote locations.\n");
        projectInfo.append("6. Hobbyist Projects: Robotics hobbyists can use this code as a basis for building their own custom robots, adding additional features and sensors to suit their specific needs and interests.\n");

        projectInfo.append("Using Android Studio for Robot Control:\n");
        projectInfo.append("If you want to control your robot using an Android app developed in Android Studio, you'll need to establish communication between the Android app and the robot. Here's a general overview of how you can achieve this:\n");
        projectInfo.append("1. Design the Android App Interface: In Android Studio, design the user interface (UI) of your Android app. You can use buttons, sliders, or any other UI elements to send commands to the robot.\n");
        projectInfo.append("2. Establish Bluetooth Communication: To send commands from your Android app to the robot, you'll typically use Bluetooth communication. You need to pair your Android device with the Bluetooth module on your robot. Android Studio provides APIs for Bluetooth communication.\n");
        projectInfo.append("3. Send Commands: When a button or UI element in your Android app is clicked or interacted with, send a corresponding command over the Bluetooth connection. For example, if the 'Forward' button is pressed, send the command 'F' to the robot. Similarly, send 'B' for backward, 'L' for left, 'R' for right, and so on.\n");
        projectInfo.append("4. Receive Feedback: Depending on your robot's capabilities, you can also receive feedback from the robot and display it on your Android app. For instance, if your robot has sensors, it can send sensor data (e.g., distance measurements) back to the Android app, which can then be displayed on the screen.\n");
        projectInfo.append("5. Implement Error Handling: Implement error handling in your Android app to deal with issues such as a lost Bluetooth connection or failed command execution. You can display error messages to the user or attempt to reconnect to the robot automatically.\n");
        projectInfo.append("6. User Interface for Obstacle Detection: If your robot has obstacle detection capabilities, you can create a separate screen or UI element in your Android app to display real-time data from the robot's sensors, allowing the user to visualize obstacles.\n");
        projectInfo.append("7. Testing and Debugging: Thoroughly test your Android app and robot to ensure that commands are transmitted accurately, and the robot responds as expected. Use Android Studio's debugging tools to identify and fix any issues.\n");
        projectInfo.append("8. Deployment: Once your Android app is ready, you can deploy it to your Android device, such as a smartphone or tablet.\n");

        projectInfoTextView.setText(projectInfo.toString());
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.option_menu, menu);

        return true;
    }


    public boolean onOptionsItemSelected(@NonNull MenuItem item) {
        if (item.getItemId() == R.id.xyz) {
            // Show the Settings fragment
            Toast.makeText(getBaseContext(),"Refreshed",Toast.LENGTH_LONG).show();;
            return true;
        } else if (item.getItemId() == R.id.txi) {
            // Blink the screen 3 times
            finish();

            return true;
        } else {
            return super.onOptionsItemSelected(item);
        }
    }


}
Options menu 
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:id="@+id/xyz"
        android:title="Refresh"
        android:icon="@drawable/baseline_refresh_24">
    </item>
    <item android:id="@+id/zxi"
        android:title="help"
        android:icon="@drawable/baseline_help_24">

    </item>
    <item android:id="@+id/lxi"
        android:title="Others"
        android:icon="@drawable/baseline_gamepad_24">
    </item>
    <item android:id="@+id/txi"
        android:title="Exit"
        android:icon="@drawable/baseline_exit_to_app_24">
    </item>
</menu>




