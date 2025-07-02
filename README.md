# Guía de Implementación de Imágenes Responsive en E-commerce

## 🎯 Misión

La misión es optimizar la galería de productos para asegurar una experiencia de usuario perfecta en dispositivos móviles, tabletas y escritorios (hasta 4K). Este proyecto aborda la optimización de imágenes con tecnologías como `srcset`, `sizes`, `picture`, y lazy loading.

---

## 🛠️ Requisitos

### 1. 📸 **Imágenes Responsive**
- Implementa `srcset` y `sizes` para cargar la resolución adecuada según el dispositivo.
- Utiliza imágenes de diferentes tamaños y formatos.

### 2. 🎨 **Art Direction**
- Utiliza el `<picture>` element para ofrecer diferentes composiciones en móvil vs escritorio.

### 3. ⚡ **Rendimiento**
- Implementa `lazy loading` para imágenes y optimiza la carga de contenido.

### 4. ♿ **Accesibilidad**
- Usa atributos `alt` descriptivos en todas las imágenes.
- Implementa `aspect-ratio` para evitar desplazamientos de layout y mejorar la estabilidad visual.

---

## 🛍️ Galería de Productos

### Productos Destacados:

- **Smartphone Pro Max 128GB**  
  Cámara de 108MP, pantalla AMOLED de 6.7” y batería de larga duración.

- **Laptop Gaming RTX 4070**  
  Procesador Intel i7, 32GB de RAM y tarjeta gráfica RTX 4070 para un rendimiento extremo.

- **Auriculares Noise Cancelling Pro**  
  Cancelación de ruido activa, sonido Hi-Res y hasta 30 horas de batería.

- **Smartwatch Health Monitor**  
  Monitoreo de salud 24/7, GPS integrado y resistencia al agua hasta 50m.

---

## 📝 Ejemplos de Implementación

### **Producto 1: Smartphone Pro Max**

```html
<picture>
  <!-- Móvil: Imagen cuadrada -->
  <source media="(max-width: 767px)" srcset="https://picsum.photos/400/400?random=1">
  <img 
    class="product-image"
    src="https://picsum.photos/600/400?random=1"
    srcset="https://picsum.photos/600/400?random=1 600w, https://picsum.photos/1200/800?random=1 1200w"
    sizes="(max-width: 768px) 100vw, 33vw"
    alt="Smartphone Pro Max mostrando pantalla de inicio"
    loading="lazy"
  >
</picture>
