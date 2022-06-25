This is a Merge of two codes in one, the original VU Metter I2C display with 10 leds VU Metter.

The original code is named OLED_Metter
The second code was the Arduino.cc exemple of barGraph

Some ajusts are maded in ledLevel mapping as below:
  // map the result to a range from 0 to the number of LEDs:
  int ledLevel = map(sensorReading, 50, 400, 0, ledCount);

The original was:
  // map the result to a range from 0 to the number of LEDs:
  int ledLevel = map(sensorReading, 0, 1023, 0, ledCount);

For the display the sample window was changed to to the response of the needle sincronize with the leds (The original is 50ms)

const int sampleWindow = 30;          // sample window width in mS (50 mS = 20Hz)

