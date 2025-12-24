# 🔴 Práctica 1: Parpadeo de LED en Wokwi

## 📋 Objetivo
Crear el primer programa en Arduino que haga parpadear un LED cada segundo.

---

## 🎯 Método 1: LED Integrado (MÁS RÁPIDO)

### Pasos:
1. Ir a: https://wokwi.com/projects/new/arduino-uno
2. Copiar este código en el editor
3. Click en "▶ Start Simulation"
4. Observar el LED naranja pequeño cerca del pin 13

### Código:
```cpp
// Práctica 1: Parpadeo de LED integrado
void setup() {
  pinMode(13, OUTPUT);  // Configurar pin 13 como salida
}

void loop() {
  digitalWrite(13, HIGH);  // Encender LED
  delay(1000);             // Esperar 1 segundo (1000 ms)
  digitalWrite(13, LOW);   // Apagar LED
  delay(1000);             // Esperar 1 segundo
}
```

---

## 🎨 Método 2: LED Externo (MÁS VISUAL)

### Pasos en Wokwi:

#### 1. Crear proyecto base
   - Ir a: https://wokwi.com/projects/new/arduino-uno

#### 2. Agregar componentes
   - Click en botón azul **"+"** (arriba izquierda)
   - Buscar y agregar:
     - **LED** (componente rojo)
     - **Resistor** (resistencia 220Ω)

#### 3. Hacer conexiones
   Arrastra los componentes y conecta:
   
   ```
   Pin 13 Arduino → Resistencia (220Ω) → LED (+) → GND Arduino
   ```

#### 4. Usar este código:
```cpp
// Práctica 1: Parpadeo de LED externo
const int LED_PIN = 13;

void setup() {
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(9600);
  Serial.println("Sistema iniciado");
}

void loop() {
  Serial.println("LED encendido");
  digitalWrite(LED_PIN, HIGH);
  delay(1000);
  
  Serial.println("LED apagado");
  digitalWrite(LED_PIN, LOW);
  delay(1000);
}
```

#### 5. Ver resultados
   - Monitor Serial: Mensajes de estado
   - LED visual: Parpadeo grande y claro

---


## 🎓 Retos para Estudiantes

### Reto 1: Cambiar patrón
Modificar para que haga:
- 3 parpadeos rápidos (200ms)
- 1 pausa larga (2000ms)
- Repetir

```cpp
void loop() {
  // Parpadeo 1
  digitalWrite(13, HIGH);
  delay(200);
  digitalWrite(13, LOW);
  delay(200);
  
  // Parpadeo 2
  digitalWrite(13, HIGH);
  delay(200);
  digitalWrite(13, LOW);
  delay(200);
  
  // Parpadeo 3
  digitalWrite(13, HIGH);
  delay(200);
  digitalWrite(13, LOW);
  delay(200);
  
  // Pausa larga
  delay(2000);
}
```

### Reto 3: Control por Serial
Permitir encender/apagar LED enviando comandos desde Serial Monitor:
- Enviar "1" → Encender
- Enviar "0" → Apagar

---

## 📊 Resultados de Aprendizaje

✅ Explicar qué es `setup()` y `loop()`  
✅ Diferenciar `pinMode()` de `digitalWrite()`  
✅ Entender qué son los delays  
✅ Conectar componentes básicos en Wokwi  
✅ Usar el Serial Monitor para debug  

---

## 🔗 Resumen
- **Función pinMode:** configura un pin como entrada o salida
- **Función digitalWrite:** establece un pin de salida en ALTO (HIGH) o BAJO (LOW) para controlar dispositivos
- **Función delay:** pausa la ejecución del programa por un número específico de milisegundos

---

## 💾 Compartir Proyecto

Una vez funcional:
1. Click en "Save" (arriba derecha)
2. Se genera un link único
3. Compartir ese link con el profesor
4. El profesor puede ver y ejecutar tu simulación

Ejemplo: `https://wokwi.com/projects/123456789`

---
