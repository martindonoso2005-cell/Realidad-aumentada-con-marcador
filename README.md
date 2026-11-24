# Botella UAI en Realidad Aumentada
**Asignatura:** Diseño de Interfaces (2026) | Universidad Adolfo Ibáñez  
**Estudiante:** Martín Donoso  
**Aplicación web:** [Abrir la experiencia AR](https://martindonoso2005-cell.github.io/Realidad-aumentada-con-marcador/)

---

## Descripción
Experiencia de realidad aumentada en el navegador: al apuntar la cámara del celular o del computador al marcador, aparece sobre él un modelo 3D de la botella UAI. No hay que instalar ninguna aplicación.

## Cómo probarlo
1. Abre la [aplicación web](https://martindonoso2005-cell.github.io/Realidad-aumentada-con-marcador/) y acepta el permiso de la cámara.
2. Apunta la cámara al marcador (impreso o en otra pantalla).
3. La botella aparece sobre el marcador y lo sigue cuando lo mueves.

## Tecnología
- **A-Frame** para la escena 3D.
- **AR.js** para reconocer el marcador de patrón (`a-marker`).
- **aframe-extras** para cargar el modelo glTF.

## Contenido del repositorio
- `index.html`: la escena AR.
- `assets/asset.glb`: modelo 3D de la botella.
- `assets/marker.patt`: patrón del marcador que reconoce la cámara.
