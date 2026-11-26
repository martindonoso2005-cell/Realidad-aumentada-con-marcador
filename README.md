# Botella UAI en Realidad Aumentada
**Asignatura:** Taller de Diseño de Interfaces (2026) | Universidad Adolfo Ibáñez  
**Ejercicio:** Unidad 3 · Módulo 02: Realidad Aumentada Web (AR.js)  
**Estudiante:** Martín Donoso  
**Aplicación web:** [Abrir la experiencia AR](https://martindonoso2005-cell.github.io/Realidad-aumentada-con-marcador/)  
**Marcador para imprimir:** [assets/marcador.png](assets/marcador.png)

---

## Descripción
Experiencia de realidad aumentada en el navegador basada en un marcador físico (*marker-based*). Al apuntar la cámara del celular o del computador al marcador, aparece la botella UAI sobre su pedestal, parada encima del marcador y siguiéndolo cuando se mueve. No hay que instalar ninguna aplicación.

## Cómo probarlo
1. Imprime el [marcador](assets/marcador.png) o ábrelo en otra pantalla. También está el botón **Ver marcador** dentro de la aplicación.
2. Abre la [aplicación web](https://martindonoso2005-cell.github.io/Realidad-aumentada-con-marcador/) y acepta el permiso de la cámara.
3. Apunta la cámara al marcador completo, incluido el borde blanco alrededor del cuadrado negro, y con buena luz.
4. La botella aparece sobre el marcador.

Para probarlo en el computador sin publicar, usa un servidor local (por ejemplo `python -m http.server 8000`): la cámara no funciona abriendo el HTML con doble clic (`file://`).

## Tecnología
- **A-Frame 1.3.0** (sobre Three.js) para la escena 3D.
- **AR.js 3.4.5** con marcador de patrón (`a-marker` + `assets/patt/marcador.patt`).
- **Modelo glTF** (`botella.glb`, exportado de KeyShot). Solo se muestran la botella de pie y su pedestal (`OBJETOS_VISIBLES` en `index.html`).

## Ajustes por URL
- `?altura=1.5`: altura de la botella con pedestal, en anchos de marcador (por defecto 1.2).
- `?debug=1`: dibuja un plano azul sobre el marcador detectado.

## Contenido del repositorio
```
index.html                 página AR
assets/marcador.png        marcador para imprimir o mostrar en pantalla
assets/patt/marcador.patt  patrón del marcador para AR.js
assets/models/botella.glb  modelo 3D de la botella (~21 MB)
```

## Cambiar el marcador
El `.patt` se genera con el [generador de marcadores de AR.js](https://ar-js-org.github.io/AR.js/three.js/examples/marker-training/examples/generator.html) subiendo solo la imagen interior del cuadrado negro.
