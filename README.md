# Descripción Técnica del Proyecto Staractyl

## 📋 Información General
**Nombre:** Staractyl  
**Versión:** 1.0.0  
**Autor:** Prismark Proyects // PancaDev  
**Descripción:** Dashboard de gestión de panel Pterodactyl con sistema de tickets y administración de usuarios

---

## 🏗️ Arquitectura del Proyecto

Staractyl es una aplicación web **Full-Stack** que utiliza una arquitectura **cliente-servidor** separada:

### **Frontend (Cliente)**
- **Framework Principal:** React 19.2.0
- **Ubicación:** `/client`
- **Puerto:** 3000 (desarrollo)

### **Backend (Servidor)**
- **Framework:** Node.js con Express 4.18.2
- **Ubicación:** `/server`
- **Puerto:** 3001

---

## 🎨 Frontend - Tecnologías

### **Core**
- **React 19.2.0** - Biblioteca principal para la interfaz de usuario
- **React DOM 19.2.0** - Renderizado de componentes React en el navegador
- **React Scripts 5.0.1** - Herramientas de desarrollo y build de Create React App

### **Enrutamiento**
- **React Router DOM 7.9.4** - Navegación entre páginas (SPA - Single Page Application)

### **UI/UX**
- **React Color 2.19.3** - Selector de colores para personalización de rangos
- **CSS Personalizado** - Diseño con glassmorphism, efectos de blur y animaciones
- **Fuentes:** Google Fonts (Outfit, Inter)

### **Testing**
- **@testing-library/react 16.3.0** - Testing de componentes
- **@testing-library/jest-dom 6.9.1** - Matchers de Jest para DOM
- **@testing-library/user-event 13.5.0** - Simulación de eventos de usuario

### **Herramientas de Desarrollo**
- **Webpack** - Bundler (incluido en react-scripts)
- **Babel** - Transpilador de JavaScript (incluido en react-scripts)
- **ESLint** - Linter de código

---

## ⚙️ Backend - Tecnologías

### **Framework y Servidor**
- **Node.js** - Runtime de JavaScript
- **Express 4.18.2** - Framework web minimalista y flexible
- **Body-Parser 2.2.0** - Middleware para parsear cuerpos de peticiones HTTP

### **Base de Datos**
El proyecto soporta **dos tipos de bases de datos**:
- **SQLite3 5.1.6** - Base de datos embebida (opción por defecto)
- **MySQL 2.18.1** - Base de datos relacional (opción avanzada)

### **Seguridad**
- **Bcrypt 6.0.0** - Encriptación de contraseñas con hashing seguro

### **Desarrollo**
- **Concurrently 8.2.2** - Ejecuta cliente y servidor simultáneamente en desarrollo

---

## 📁 Estructura del Proyecto

```
Staractyl/
├── client/                    # Aplicación React (Frontend)
│   ├── public/               # Archivos estáticos
│   │   └── index.html       # HTML principal
│   ├── src/
│   │   ├── components/      # Componentes React
│   │   │   ├── Auth.js/css          # Autenticación
│   │   │   ├── Dashboard.js/css     # Panel principal
│   │   │   ├── Configuration.js/css # Configuración
│   │   │   ├── Tickets.js/css       # Sistema de tickets
│   │   │   ├── Soporte.js/css       # Soporte
│   │   │   ├── Setup.js/css         # Configuración inicial
│   │   │   ├── Navbar.js/css        # Navegación
│   │   │   └── ...
│   │   ├── App.js           # Componente principal
│   │   ├── index.js         # Punto de entrada
│   │   └── index.css        # Estilos globales
│   └── package.json         # Dependencias del cliente
│
├── server/                   # Servidor Node.js (Backend)
│   ├── index.js             # Servidor Express y API REST
│   ├── database.js          # Configuración de base de datos
│   ├── config.json          # Configuración del servidor
│   └── database/            # Archivos de base de datos
│
└── package.json             # Dependencias del proyecto raíz
```

---

## 🎯 Características Principales

### **Sistema de Autenticación**
- Login y registro de usuarios
- Encriptación de contraseñas con bcrypt
- Sesiones de usuario

### **Panel de Administración**
- Dashboard con estadísticas
- Gestión de usuarios
- Sistema de rangos personalizables con colores
- Configuración de Pterodactyl

### **Sistema de Tickets**
- Creación de tickets de soporte
- Chat en tiempo real para cada ticket
- Estados de tickets (abierto, cerrado, esperando respuesta, respondido)
- Filtrado y búsqueda de tickets

### **Diseño Moderno**
- **Glassmorphism** - Efectos de vidrio esmerilado con blur
- **Animaciones CSS** - Transiciones suaves y efectos hover
- **Tema Oscuro** - Paleta de colores oscura con acentos neón
- **Responsive** - Adaptable a diferentes tamaños de pantalla
- **Fondo Animado** - Estrellas animadas con CSS

### **Configuración Inicial**
- Wizard de setup multi-paso
- Selección de base de datos (SQLite/MySQL)
- Configuración de tema y idioma
- Creación de cuenta administrador

---

## 🚀 Scripts de Desarrollo

### **Comandos Principales**
```bash
# Iniciar servidor backend
npm start

# Iniciar cliente React
npm run client

# Iniciar ambos simultáneamente (desarrollo)
npm run dev

# Build de producción del cliente
cd client && npm run build
```

---

## 🔧 Configuración

### **Proxy**
El cliente React está configurado con un proxy a `http://localhost:3001` para las peticiones API, evitando problemas de CORS en desarrollo.

### **Variables de Entorno**
- **Frontend:** Puerto 3000
- **Backend:** Puerto 3001
- **Base de datos:** Configurable (SQLite por defecto)

---

## 🎨 Diseño y Estilo

### **Sistema de Diseño**
- **Variables CSS** para colores, glassmorphism y transiciones
- **Fuentes:** Outfit (principal), Inter (secundaria)
- **Paleta de Colores:**
  - Fondo: Degradado oscuro (#1B2735 → #090A0F)
  - Acento: Cyan neón (#00f2ff)
  - Texto: Blanco/Gris claro
  - Éxito: Verde (#22c55e)
  - Error: Rojo (#ff4d4d)

### **Efectos Visuales**
- Backdrop blur de 16-20px
- Sombras con transparencia
- Animaciones de fadeIn y slideIn
- Hover effects con transform y scale
- Gradientes lineales en botones

---

## 📦 Dependencias Clave

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| React | 19.2.0 | Framework UI |
| Express | 4.18.2 | Servidor web |
| React Router | 7.9.4 | Navegación SPA |
| Bcrypt | 6.0.0 | Seguridad |
| SQLite3 | 5.1.6 | Base de datos |
| MySQL | 2.18.1 | Base de datos alternativa |
| React Color | 2.19.3 | Selector de colores |

---

## 🔐 Seguridad

- Contraseñas hasheadas con bcrypt (salt rounds configurables)
- Validación de inputs en cliente y servidor
- Protección contra inyección SQL (prepared statements)
- Sesiones de usuario seguras

---

## 📝 Notas Adicionales

- **SPA (Single Page Application):** La aplicación no recarga la página al navegar
- **API RESTful:** Comunicación cliente-servidor mediante endpoints REST
- **Modular:** Componentes React reutilizables y bien organizados
- **Escalable:** Arquitectura preparada para crecer y añadir funcionalidades
