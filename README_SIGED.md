# 📦 SIGED - Sistema de Gestión Empresarial de Inventario

## 🧾 Descripción General

**SIGED** es una aplicación web de gestión empresarial diseñada para administrar productos, cantidades y precios de forma simple y eficiente.  
Este proyecto utiliza un backend en **Node.js con Express** y una interfaz web estática conectada por **Fetch API**.

---

## 🚀 Características Principales

- CRUD completo (Crear, Leer, Actualizar y Eliminar productos).  
- Visualización de los productos en una tabla HTML dinámica.  
- Conexión al backend mediante Fetch API.  
- Validación básica de datos en el frontend.  
- Posibilidad de integración con MongoDB (en versiones futuras).  

---

## 🧩 Tecnologías Utilizadas

### 🔙 Backend
- Node.js  
- Express  
- CORS  
- Morgan  
- Body-Parser  
- (Opcional) Mongoose para persistencia de datos  

### 🌐 Frontend
- HTML  
- CSS (Tailwind recomendado)  
- JavaScript Vanilla (con Fetch API)

---

## 🗂️ Estructura del Proyecto

```
SIGED/
├── backend/
│   ├── routes/
│   │   └── products.js
│   ├── controllers/
│   │   └── productsController.js
│   ├── models/
│   │   └── productModel.js
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── frontend/
│   ├── index.html
│   ├── app.js
│   ├── styles.css
│   └── README.md
│
└── README.md
```

---

## ⚙️ Instalación y Ejecución

### 1️⃣ Clonar el Repositorio
```bash
git clone https://github.com/usuario/siged.git
cd siged/backend
```

### 2️⃣ Instalar Dependencias
```bash
npm install
```

### 3️⃣ Configurar Variables de Entorno
Crea un archivo `.env` con el siguiente contenido:
```env
PORT=3001
MONGO_URI=mongodb://localhost:27017/mi_base_de_datos
```

### 4️⃣ Ejecutar el Servidor
```bash
npm run dev
```

El servidor quedará activo en:
```
http://localhost:3001
```

### 5️⃣ Probar en el Frontend
Abre el archivo:
```
frontend/index.html
```
y asegúrate de que el archivo `app.js` apunte al mismo puerto del backend:
```js
const API = "http://localhost:3001/api/products";
```

---

## 📊 Endpoints API

| Método | Ruta | Descripción |
|:------:|:------|:-------------|
| GET | `/api/products` | Obtiene todos los productos |
| POST | `/api/products` | Crea un nuevo producto |
| PUT | `/api/products/:id` | Actualiza un producto existente |
| DELETE | `/api/products/:id` | Elimina un producto |

---

## 🧠 Diferencia entre HashMap y Array / Lista

Actualmente, los productos se almacenan en una **lista (array)** en memoria, lo que permite recorrerlos de forma secuencial.  
Sin embargo, **un HashMap (u objeto en JavaScript)** utiliza **claves únicas** para acceder directamente a los elementos, logrando una búsqueda **mucho más rápida (O(1))** frente al recorrido completo del array **(O(n))**.

**Ejemplo simple:**
```js
// Guardado actual (array)
let productos = [{id: 1, nombre: "Mouse", precio: 25}];

// Guardado con HashMap
let productosMap = {
  "1": {nombre: "Mouse", precio: 25}
};

// Acceso rápido
console.log(productosMap["1"]); // {nombre: "Mouse", precio: 25}
```

---

## 🧪 Ejemplo de Uso

1. Abre el formulario de agregar producto.  
2. Ingresa los datos del producto (ID, nombre, cantidad, precio).  
3. El producto se mostrará automáticamente en la tabla.  
4. Los productos se cargan desde el backend al iniciar la página.

---

## 🧰 Scripts Disponibles

| Script | Descripción |
|:-------|:-------------|
| `npm start` | Ejecuta el servidor en modo normal |
| `npm run dev` | Ejecuta el servidor con Nodemon para desarrollo |

---

## 📜 Licencia

Este proyecto está bajo la licencia **MIT**.  
Eres libre de modificarlo y distribuirlo citando la fuente original.

---

## 👩‍💻 Equipo de Desarrollo

| Nombre | Rol | Institución |
|:--------|:------|:-------------|
| **Cristian Echeverry González** | Desarrollador Backend & Documentación | Universidad de Antioquia |
| **Rebeca Bedoya** | Diseño Frontend & Pruebas | Universidad de Antioquia |
| **Yuliana Corrales Castaño** | Integración & Gestión de Proyecto | Universidad de Antioquia |

---

📅 **Versión:** 1.0  
📍 **Fecha de Entrega:** Octubre 2025  
