# week3-homework-

Code for turning on and off earthquake with switch. 

void setup() {
  pinMode (3, OUTPUT);// connedts to modor 
  pinMode (2, INPUT); // receives signal from switch
}

void loop() {

  if (HIGH == digitalRead(2) ) {
    analogWrite(3, 255);    // turning on motor at full speed 
  } else {
    analogWrite(3, 0);    // motor off
  }
}

// I tried to get the code to cycle through my previous code but it wouldn't stop the cycle once the button was released. 

// Here is what that looked like: 

void setup() {
  pinMode (3, OUTPUT);// connedts to modor 
  pinMode (2, INPUT); // receives signal from switch
}

void loop() {

  if (HIGH == digitalRead(2) ) {
    analogWrite(3, 255);    // turning on motor at full speed 
  analogWrite(3, 255);   // turn the earthquake on (100% force)
  delay(7000);                       // wait for seven seconds
  analogWrite(3, 0);    // turn the earthquake off by making the voltage 0
  delay(1000);                       // wait for a second
  analogWrite(3, 204);   // turn the earthquake on (80% forcel)
  delay(9000);                       // wait for 9 seconds
  analogWrite(3, 0);    // turn the LED off by making the voltage LOW
  delay(3000);                       // wait for 3 seconds 
  analogWrite(3, 255);    // turns on at full force 
  delay(11000);                       // wait for 11 seconds
  analogWrite(3, 0);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second  
  analogWrite(3, 255);   // turn the earthquake on full force)
  delay(6000);                       // wait for 6 seconds
  analogWrite(3, 0);    // turn the LED off by making the voltage LOW
  delay(3000);                       // wait for 3 second
  analogWrite(3, 150);   // turn the LED on (HIGH is the voltage level)
  delay(8000);                       // wait for a second
  analogWrite(3, 0);    // turn the LED off by making the voltage LOW
  delay(6000);                       // wait for a second
  } else {
    analogWrite(3, 0);    // motor off
    
    // not sure why it will not respond to the botton being released? 
