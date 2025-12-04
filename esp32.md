#include <WiFi.h>
#include <WebServer.h>

// PIN vibrator
#define VIB_LEFT 4
#define VIB_RIGHT 5

WebServer server(80);

// Fungsi vibrate
void vibrateLeft() {
  digitalWrite(VIB_LEFT, HIGH);
  delay(250);
  digitalWrite(VIB_LEFT, LOW);
}

void vibrateRight() {
  digitalWrite(VIB_RIGHT, HIGH);
  delay(250);
  digitalWrite(VIB_RIGHT, LOW);
}

void handleRoot() {
  server.send(200, "text/plain", "ESP32-C3 Vibrator Ready");
}

void handleLeft() {
  vibrateLeft();
  server.send(200, "text/plain", "LEFT OK");
}

void handleRight() {
  vibrateRight();
  server.send(200, "text/plain", "RIGHT OK");
}

void setup() {
  Serial.begin(115200);

  pinMode(VIB_LEFT, OUTPUT);
  pinMode(VIB_RIGHT, OUTPUT);

  WiFi.begin("WIFI_NAME", "WIFI_PASS");
  Serial.print("Connecting...");
  while (WiFi.status() != WL_CONNECTED) {
    delay(350);
    Serial.print(".");
  }

  Serial.println();
  Serial.println("Connected!");
  Serial.println(WiFi.localIP());

  server.on("/", handleRoot);
  server.on("/left", handleLeft);
  server.on("/right", handleRight);

  server.begin();
}

void loop() {
  server.handleClient();
}
