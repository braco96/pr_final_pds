
# 🎧 Ecualizabra

**Ecualizabra** es una aplicación desarrollada en **MATLAB** que combina una interfaz gráfica interactiva con procesamiento digital de señales de audio.  
Permite visualizar, modificar y analizar señales acústicas a través de un **ecualizador de 7 bandas**, además de aplicar técnicas avanzadas para **detección y segmentación de palabras** en grabaciones de voz.

---

## 🚀 Funcionalidades principales

- 🎚️ **Ecualizador de 7 bandas** completamente funcional.  
  Permite ajustar las frecuencias de audio en tiempo real y visualizar el resultado mediante representaciones gráficas dinámicas.

- 🧠 **Análisis de energía y detección de palabras**.  
  Implementa un **algoritmo de cruces por cero** que mide la energía de una señal acústica, permitiendo detectar y separar palabras dentro de un flujo de audio.

- 🪄 **Separación y mezcla de audios**.  
  Permite importar múltiples archivos de sonido, mezclarlos y aplicarles efectos de ecualización o expansión temporal.

- 🎛️ **Interfaz gráfica avanzada**.  
  Diseñada completamente en MATLAB App Designer / GUIDE, con una disposición intuitiva de controles y gráficos para interacción directa con el usuario.

---

## 🧩 Arquitectura técnica

El sistema combina procesamiento digital de señales (DSP) con herramientas gráficas de MATLAB:

| Módulo | Descripción |
|--------|--------------|
| `GUI` | Interfaz principal que permite cargar, visualizar y modificar los audios. |
| `Ecualizador` | Módulo de filtrado con 7 bandas (Bajo, Medio-bajo, Medio, Medio-alto, Alto, Presencia, Brillo). |
| `Analizador` | Implementa el algoritmo de **cruces por cero** y cálculo de energía RMS para detección de actividad de voz (VAD). |
| `Procesador` | Funciones para mezclar audios, expandir palabras o ajustar velocidad de reproducción. |

---

## 🧠 Algoritmo de cruces por cero

El método de **cruces por cero** cuenta el número de veces que la señal de audio cambia de signo (de positivo a negativo o viceversa) dentro de una ventana temporal.  
Este valor, junto con la energía media de la ventana, permite **detectar la presencia de voz o silencio**, posibilitando separar automáticamente las palabras en una grabación continua.

---

## 🧮 Requisitos

- MATLAB R2020b o superior  
- Signal Processing Toolbox  
- Audio Toolbox (opcional, para visualización espectral)

---

## ▶️ Ejecución

1. Descomprime el proyecto en una carpeta local.  
2. Abre MATLAB y navega al directorio raíz del proyecto.  
3. Ejecuta el archivo principal (`Ecualizabra.m`, `app.mlapp` o similar).  
4. Carga un archivo de audio `.wav` desde la interfaz y ajusta las bandas del ecualizador.  

---

## 📁 Estructura del proyecto

```
Ecualizabra/
├── GUI/                   # Componentes visuales y controladores
├── funciones/             # Funciones auxiliares de DSP
├── audios/                # Ejemplos de audio de entrada
├── resultados/            # Salidas procesadas (mezclas, cortes, expansiones)
└── README.md              # Documentación del proyecto
```

---

## 🧑‍💻 Autor

Proyecto desarrollado por **braco96**  
Especializado en procesamiento de señales acústicas y diseño de interfaces MATLAB.

---

## 📄 Licencia

Este proyecto se distribuye bajo licencia **MIT**.  
Puedes modificarlo y reutilizarlo libremente citando la autoría original.

---

> *“La música y la voz son ondas; entenderlas es aprender a moldear el tiempo.”* 🎶
