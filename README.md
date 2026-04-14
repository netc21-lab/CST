# ♻️ Recicla Clone — Marketplace de Segunda Mano

Clon funcional de Resikla.pe, listo para GitHub y Netlify. Personalizable al 100% desde un solo archivo.

## 📁 Estructura

```
resikla-clone/
├── index.html              ← Página principal
├── css/main.css            ← Todos los estilos
├── js/
│   ├── config.js           ← ⭐ EDITA AQUÍ tu marca y configuración
│   └── store.js            ← Datos, carrito, auth (no editar)
├── pages/
│   ├── productos.html      ← Catálogo con filtros
│   ├── producto.html       ← Detalle de producto
│   ├── carrito.html        ← Carrito de compras
│   ├── favoritos.html      ← Lista de favoritos
│   ├── vender.html         ← Formulario para vender
│   ├── cuenta.html         ← Login, registro, mi cuenta
│   └── checkout.html       ← Proceso de pago (Yape)
└── admin/
    └── index.html          ← Panel administrador
```

## 🚀 Inicio rápido

### 1. Personalizar tu marca
Abre **`js/config.js`** y edita:

```js
const SITE = {
  name:        'NombreDeTuTienda',   // ← Cambia esto
  logoLetter:  'N',                  // ← Inicial del logo
  colorPrimary:'#16A34A',            // ← Color principal
  whatsapp:    '51987654321',        // ← Tu WhatsApp
  yapeNumber:  '987654321',          // ← Tu número Yape
  adminEmail:  'tu@correo.com',      // ← Email admin
  adminPass:   'tuPassword123',      // ← Contraseña admin
  // ... más opciones
};
```

### 2. Publicar en Netlify (gratis)
1. Sube este repositorio a GitHub
2. Ve a [netlify.com](https://netlify.com) → "Import from Git"
3. Conecta tu repositorio → Deploy ✅
4. Tu tienda estará en: `https://tu-tienda.netlify.app`

### 3. Publicar arrastrando carpeta
1. Ve a [netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra toda la carpeta `resikla-clone/`
3. ¡Listo en segundos!

## 🔑 Acceso admin

- URL: `/admin/index.html`
- Email: el que configures en `SITE.adminEmail`
- Contraseña: la que configures en `SITE.adminPass`
- Por defecto: `admin@recicla.pe` / `admin123`

## ✨ Funcionalidades

| Función | Estado |
|---------|--------|
| Catálogo con filtros y búsqueda | ✅ |
| Página de producto con detalle | ✅ |
| Carrito de compras | ✅ |
| Favoritos | ✅ |
| Registro e inicio de sesión | ✅ |
| Pago con Yape (voucher) | ✅ |
| Envío de detalle por WhatsApp | ✅ |
| Formulario para vender | ✅ |
| Panel admin completo | ✅ |
| Gestión de productos | ✅ |
| Gestión de pedidos | ✅ |
| Lista de clientes | ✅ |
| Diseño responsive (móvil) | ✅ |
| Sin dependencias externas | ✅ |
| Datos guardados en localStorage | ✅ |

## 🎨 Cambiar colores

En `js/config.js`, cambia `colorPrimary` por cualquier color hex:

```js
colorPrimary: '#E91E63',  // Rosa
colorPrimary: '#1E88E5',  // Azul  
colorPrimary: '#FF5722',  // Naranja
colorPrimary: '#9C27B0',  // Morado
```

## 💡 Notas

- Los datos se guardan en `localStorage` del navegador
- Para una base de datos real, integra con [Supabase](https://supabase.com) (gratis)
- Las imágenes subidas se guardan como base64 en el navegador
- Para imágenes en producción, usa Supabase Storage o Cloudinary

## 📱 Flujo de venta

```
Cliente → Agrega al carrito → Checkout → Yapea → Sube voucher
→ Admin ve pedido pendiente → Confirma → WhatsApp al cliente ✅
```
