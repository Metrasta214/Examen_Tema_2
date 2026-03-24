# 🎮 Shooter 3D - Three.js

Demo interactiva de un videojuego tipo shooter en tercera persona desarrollado con **Three.js**, que incluye físicas, animaciones, inteligencia básica de enemigos y sistema de combate en tiempo real.

---

## 🚀 Características

- 🔫 Sistema de disparo con raycasting
- 🤖 Enemigos con IA básica (persecución + ataque)
- 🧍 Personaje con múltiples animaciones:
  - Idle
  - Run
  - Walk
  - Jump
  - Dying
- 🌍 Escenario 3D con colisiones (Octree)
- ⚙️ Sistema de físicas con gravedad
- ❤️ HUD de vida del jugador
- 👾 Contador de enemigos
- 🎯 Crosshair y hit markers
- 💥 Efectos visuales (disparo, daño, impacto)
- 🔊 Sonido procedural de disparo
- ⚡ Optimización:
  - Cache de assets
  - Pool de objetos (balas e impactos)
  - Compilación previa de shaders
  - Carga controlada de recursos

---

## 🎮 Controles

| Acción       | Tecla / Input |
| ------------ | ------------- |
| Mover        | WASD          |
| Mirar        | Mouse         |
| Saltar       | SPACE         |
| Disparar     | Click         |
| Recibir daño | K             |

---

## 🧠 Tecnologías utilizadas

- **Three.js** → Renderizado 3D
- **GLTFLoader** → Carga de modelos
- **Octree** → Colisiones eficientes
- **Capsule Physics** → Física del jugador y enemigos
- **Web Audio API** → Sonido de disparos

---

## 🏗️ Arquitectura

El proyecto está estructurado en módulos lógicos:

- `Player` → Movimiento, físicas y animaciones
- `Enemies` → IA, combate y comportamiento
- `World` → Escenario, colisiones y objetos
- `Rendering` → Cámara, luces y optimización
- `UI/HUD` → Interfaz del jugador

---

## ⚡ Optimizaciones implementadas

- `THREE.Cache.enabled` → Reutilización de recursos
- `renderer.compile()` → Evita lag inicial
- Object pooling → Reduce creación/destrucción de objetos
- Reducción de sombras y resolución
- Texturas "precalentadas" (warm-up)
