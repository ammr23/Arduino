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
### Ahora añadir una parte (+) LED, para visualizar mejor al ejecutar
---

## 🎓 Retos: resolver en clase

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

### Reto 2: Encender LED con un botón
- https://www.youtube.com/watch?v=x8rEgxWrUHg 

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
