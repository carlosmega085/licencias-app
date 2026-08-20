# Generador Universal de Suscripciones Premium MVP

Este es un generador de licencias y suscripciones premium offline basado en la web para aplicaciones móviles y de escritorio que utilizan validación criptográfica local. Está diseñado de manera ultra-ligera como una SPA (Single Page Application) de un solo archivo HTML.

## 🚀 Características

* **Validación Criptográfica Local**: Genera firmas digitales robustas de 6 caracteres basadas en semillas dinámicas (seeds) y algoritmos de hashing ligeros.
* **Soporte Multi-App**: Configurado con presets para múltiples aplicaciones:
  * **CitaPro** (`CP`)
  * **Lumi** (`LM`)
  * **GymPro** (`GP`)
  * **Configuración Personalizada**: Permite definir prefijos de 2 letras y llaves secretas personalizadas para cualquier aplicación externa.
* **Plantilla de Mensajería para WhatsApp**: Copia automáticamente un mensaje formateado listo para enviar a los clientes por WhatsApp con las instrucciones de activación.
* **Seguridad de Acceso**: Control de inicio de sesión administrativo con almacenamiento de sesión por pestaña (`sessionStorage`) y contraseña hasheada (`citapro2026`).

## 📁 Estructura del Proyecto

* [generator.html](file:///c:/Users/Walner/PROYECTOS%20CON%20REACT%20NATIVE%20Y%20EXPO/LICENSIAMIENTO/generator.html): Archivo HTML auto-contenido que incluye la estructura, estilos CSS modernos con variables de diseño premium en modo oscuro, y lógica en JavaScript.

## ⚙️ Cómo Funciona la Firma de Códigos

El código generado sigue el formato:
`[PREFIJO]-[SEMILLA]-[DÍAS]-[FIRMA]`

1. **Prefijo**: Define qué aplicación utilizará la licencia (ej. `CP` para CitaPro).
2. **Semilla (Seed)**: Un número aleatorio de 5 dígitos generado para evitar colisiones y reutilización de firmas.
3. **Días**: La cantidad de días de suscripción otorgados (ej. `30` o `365`).
4. **Firma**: Una firma hash de 6 caracteres hexadecimales calculada combinando `Seed + "_" + Days + "_" + BusinessID + SecretKey`.

## 🛠️ Instalación y Uso

1. Simplemente clona o descarga el archivo [generator.html](file:///c:/Users/Walner/PROYECTOS%20CON%20REACT%20NATIVE%20Y%20EXPO/LICENSIAMIENTO/generator.html).
2. Haz doble clic en el archivo para abrirlo en cualquier navegador web moderno (no requiere servidor web o NodeJS).
3. Ingresa la contraseña de administrador predeterminada: `citapro2026`.
4. Rellena los datos (ID del Negocio, duración y aplicación) para generar tu licencia.
