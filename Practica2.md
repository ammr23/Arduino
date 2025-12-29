
# 🔴 Práctica 2: Comunicación Serial
  Arduino hablando con la computadora. 
  Se inicializa la comunicación serial en Arduino. Básicamente le dice al Arduino: "prepárate para enviar y recibir datos por el puerto USB". 
  1. Serial: Es el objeto que controla el puerto de comunicación serial (USB) del Arduino.
  2. begin(): Es la función que inicia/activa la comunicación serial.
  3. 9600: Es la velocidad de comunicación (baudios o baud rate).
     Ver el resultado en el monitor serial de wokwi.
  ### Código:
```cpp
// Arduino enviando datos por serial
void setup() {
  Serial.begin(9600); // Iniciar comunicación a 9600 baudios
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  Serial.println("LED encendido");
  delay(1000);
  
  digitalWrite(13, LOW);
  Serial.println("LED apagado");
  delay(1000);
}
```

Arduino envía temperatura simulada cada 2 segundos. Cambiar el void loop : 
```cpp
void loop() {
  float tempSimulada = random(20, 30); // Entre 20°C y 30°C
  Serial.print("Temperatura: ");
  Serial.print(tempSimulada);
  Serial.println(" °C");
  delay(2000);
}
```


