#TO CHECK THE WATER LEVEL IF WATER ID DETECTED USING TEMPERATURE SENSOR

#define SENSOR_PIN 34   // ADC pin connected to your sensor

// Set a threshold – above this means water detected
#define WATER_THRESHOLD 1000  

void setup() {
  Serial.begin(115200);
}

void loop() {
  int sensorValue = analogRead(SENSOR_PIN);  // Read raw value (0–4095)

  Serial.print("Raw Sensor Value: ");
  Serial.println(sensorValue);

  // Check if water is present
  if (sensorValue > WATER_THRESHOLD) {
    Serial.println("💧 Water Detected!");
  } else {
    Serial.println("No Water.");
  }

  delay(1000);
}
