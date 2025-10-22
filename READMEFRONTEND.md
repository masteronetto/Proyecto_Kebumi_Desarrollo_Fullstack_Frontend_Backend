# 🎨 Proyecto Kebumy - Frontend React

## 📋 Descripción del Proyecto

**Proyecto Kebumy** es una aplicación frontend moderna desarrollada con **React** que proporciona una interfaz completa para la gestión de usuarios y productos. La aplicación implementa un sistema de autenticación, operaciones CRUD completas y está diseñada para trabajar con un backend Spring Boot a través de API REST.

## �️ Arquitectura del Proyecto

### **Patrón de Arquitectura Implementado**
- **Arquitectura por Componentes (Component-Based)**
- **Patrón Container/Presentational**
- **Custom Hooks Pattern**
- **Service Layer Pattern**
- **Protected Routes Pattern**

### **Estructura de Capas**
```
┌─────────────────────────────────────┐
│         CAPA PRESENTACIÓN           │
│        (Pages & Components)         │
├─────────────────────────────────────┤
│          CAPA LÓGICA                │
│         (Hooks & Utils)             │
├─────────────────────────────────────┤
│         CAPA SERVICIOS              │
│         (API Services)              │
├─────────────────────────────────────┤
│       CAPA CONFIGURACIÓN            │
│       (Config & Constants)          │
└─────────────────────────────────────┘
```

## 📁 Estructura del Proyecto

```
FrontendKebumy/
├── 📄 package.json                             # Dependencias y scripts del proyecto
├── 📄 vite.config.js                          # Configuración de Vite
├── 📄 eslint.config.js                        # Configuración de ESLint
├── 📄 index.html                              # HTML principal de la aplicación
├── � public/                                 # Archivos públicos estáticos
├── � src/                                    # Código fuente principal
│   ├── 📄 main.jsx                           # Punto de entrada de la aplicación
│   ├── 📄 App.jsx                            # Componente raíz con configuración de rutas
│   ├── 📄 App.css                            # Estilos del componente principal
│   ├── 📄 index.css                          # Estilos base de la aplicación
│   ├── � components/                        # Componentes reutilizables
│   │   ├── 📄 ProtectedRoute.jsx             # Protección de rutas administrativas
│   │   ├── � Navbar/                        # Barra de navegación principal
│   │   │   └── 📄 Navbar.jsx                 # Componente de navegación
│   │   ├── � Footer/                        # Pie de página
│   │   │   └── 📄 Footer.jsx                 # Componente de pie de página
│   │   ├── � Productos/                     # Gestión completa de productos
│   │   │   ├── 📄 Productos.jsx              # Listado y gestión de inventario
│   │   │   └── 📄 EditarProducto.jsx         # Modal de edición de productos
│   │   ├── � Usuarios/                      # Gestión completa de usuarios
│   │   │   ├── 📄 Usuarios.jsx               # Listado y administración de usuarios
│   │   │   ├── 📄 CrearUsuario.jsx           # Formulario de alta de usuarios
│   │   │   └── 📄 EditarUsuario.jsx          # Modal de edición de usuarios
│   │   ├── � CrearProd/                     # Formularios de creación
│   │   │   └── 📄 CrearProducto.jsx          # Formulario crear producto
│   │   ├── � BackendToggle/                 # Herramientas de desarrollo
│   │   │   └── 📄 BackendToggle.jsx          # Alternador backend real/mock
│   │   └── � DiagnosticTool/                # Diagnóstico de conexión
│   │       └── 📄 DiagnosticTool.jsx         # Herramienta de debug
│   ├── � pages/                             # Páginas principales de la aplicación
│   │   ├── � Home/                          # Página de inicio
│   │   │   └── 📄 Home.jsx                   # Página principal pública
│   │   ├── � Login/                         # Autenticación
│   │   │   └── 📄 Login.jsx                  # Formulario de login administrativo
│   │   ├── � Contacto/                      # Información de contacto
│   │   │   ├── � Contacto.jsx               # Página de contacto
│   │   │   └── 📄 Contacto.css               # Estilos específicos de contacto
│   │   ├── 📁 Inventario/                    # Gestión de inventario
│   │   │   └── 📄 Inventario.jsx             # Wrapper para gestión de productos
│   │   └── � Usuarios/                      # Panel de usuarios
│   │       └── 📄 Adminusuarios.jsx          # Wrapper para administración de usuarios
│   ├── � hooks/                             # Custom React Hooks
│   │   └── 📄 useAuth.js                     # Hook de autenticación centralizada
│   ├── � services/                          # Servicios de comunicación
│   │   └── 📄 apiService.js                  # Cliente HTTP principal para API
│   ├── � config/                            # Configuraciones del sistema
│   │   └── 📄 api.js                         # Configuración de API y datos mock
│   ├── � styles/                            # Estilos globales
│   │   └── 📄 GlobalStyles.css               # CSS global de la aplicación
│   └── � assets/                            # Recursos multimedia
│       ├── 🖼️ logoKebumy.png                 # Logo principal de la marca
│       ├── 🖼️ Polera.png                     # Imágenes de productos
│       ├── 🖼️ Poleron.png                    # Recursos gráficos
│       └── 🖼️ [más imágenes...]              # Otros recursos multimedia
```

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Propósito |
|-----------|---------|-----------|
| **React** | 19.1.1 | Framework principal de frontend |
| **React DOM** | 19.1.1 | Renderizado de componentes |
| **React Router DOM** | 7.9.3 | Enrutamiento SPA |
| **Vite** | 7.1.7 | Build tool y servidor de desarrollo |
| **Axios** | 1.12.2 | Cliente HTTP para API REST |
| **Bootstrap** | 5.3.8 | Framework CSS y componentes |
| **React Hook Form** | 7.64.0 | Manejo avanzado de formularios |
| **Yup** | 1.7.1 | Esquemas de validación |
| **ESLint** | 9.36.0 | Linter y calidad de código |

### 🌟 Características Principales Implementadas

- ✅ **Panel de Administración** completo con autenticación
- ✅ **Gestión de Productos** (CRUD completo)
- ✅ **Gestión de Usuarios** con roles y permisos
- ✅ **Control de Inventario** con alertas de stock bajo
- ✅ **Sistema de Imágenes** robusto con múltiples formatos
- ✅ **Modo Desarrollo/Producción** con backend real o datos mock
- ✅ **Diseño Responsive** adaptable a móviles
- ✅ **Interfaz Intuitiva** con tema visual coherente

## 🚀 Instalación y Ejecución

### **Prerrequisitos**
- **Node.js** versión 18 o superior
- **npm** o **yarn** como gestor de paquetes
- Backend Spring Boot corriendo en puerto 3000 (opcional - tiene modo mock)

### **Pasos para ejecutar:**

1. **Clonar el repositorio**
```bash
git clone [URL-del-repositorio]
cd FrontendKebumy
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Ejecutar en modo desarrollo**
```bash
npm run dev
```

4. **Acceder a la aplicación**
```
http://localhost:5173
```

### **Scripts Disponibles**
```bash
npm run dev      # Servidor de desarrollo con hot reload
npm run build    # Construir aplicación para producción
npm run preview  # Vista previa de la build de producción
npm run lint     # Verificar código con ESLint
```

## 🧩 Componentes y Funcionalidades

### **1. Capa de Presentación (Pages & Components)**

#### **App.jsx**
- **Propósito:** Configuración principal de rutas y layout
- **Funciones:**
  - Configuración de React Router
  - Definición de rutas públicas y protegidas
  - Integración del BackendToggle para desarrollo
  - Manejo de rutas de fallback

#### **Home.jsx** (`src/pages/Home/`)
- **Propósito:** Página de bienvenida e información principal
- **Funciones:**
  - Presentación de la marca Kebumy
  - Enlaces de navegación principales
  - Diseño responsive y atractivo

#### **Login.jsx** (`src/pages/Login/`)
- **Propósito:** Autenticación de administradores
- **Estados gestionados:**
  - `email, password, userRole`: Credenciales de acceso
  - `loading`: Estado de carga durante autenticación
  - `error`: Mensajes de error específicos
- **Funciones principales:**
  - **Autenticación:** Validar credenciales con backend
  - **Redirección:** Automática post-login a panel admin
  - **Manejo de errores:** Diagnóstico detallado de fallos
  - **Modo dual:** Soporte para backend real y mock

#### **Navbar.jsx** (`src/components/Navbar/`)
- **Propósito:** Barra de navegación principal adaptativa
- **Características:**
  - Logo de Kebumy con enlace al inicio
  - Navegación condicional basada en autenticación
  - Indicador de usuario logueado
  - Botón de cerrar sesión
- **Funciones principales:**
  - `handleLogout()`: Cierra sesión y redirige al inicio

#### **Footer.jsx** (`src/components/Footer/`)
- **Propósito:** Pie de página informativo y de contacto
- **Elementos incluidos:**
  - Información de contacto empresarial
  - Enlaces a redes sociales (Instagram, Facebook)
  - Logo y descripción de la empresa
  - Datos de contacto (email, WhatsApp)

### **2. Gestión de Productos**

#### **Productos.jsx** (`src/components/Productos/`)
- **Propósito:** Listado completo y gestión de inventario
- **Características principales:**
  - Tabla responsive con todos los productos
  - Sistema robusto de manejo de imágenes con cache
  - Filtros por categoría y estado
  - Acciones de editar/eliminar con confirmaciones
  - Indicadores visuales de stock bajo (<5 unidades)
  - Estadísticas de inventario
- **Funciones clave:**
  - `fetchProductos()`: Cargar productos desde API/mock
  - `handleDelete()`: Eliminar producto con confirmación
  - `getImageUrl()`: Sistema inteligente de resolución de imágenes
  - Manejo de imágenes locales, URLs externas y base64

#### **CrearProducto.jsx** (`src/components/CrearProd/`)
- **Propósito:** Formulario completo de creación de productos
- **Características avanzadas:**
  - Validación en tiempo real de todos los campos
  - Soporte dual para imágenes (URL externa o archivo local)
  - Preview en tiempo real de imágenes
  - Validación de formatos y tamaños de archivo
  - Conversión automática a base64 para archivos locales
- **Estados principales:**
  - `producto`: Datos completos del formulario
  - `tipoImagen`: Selector entre URL o archivo
  - `previewImagen`: Vista previa en tiempo real
  - `validandoUrl`: Estado de validación de URLs

#### **EditarProducto.jsx** (`src/components/Productos/`)
- **Propósito:** Modal de edición de productos existentes
- **Funcionalidades:**
  - Pre-llenado automático con datos existentes
  - Actualización en tiempo real
  - Validación de cambios antes de envío
  - Manejo de imágenes actualizado

### **3. Gestión de Usuarios**

#### **Usuarios.jsx** (`src/components/Usuarios/`)
- **Propósito:** Administración completa de usuarios del sistema
- **Elementos de interfaz:**
  - Widget estadístico de total de usuarios
  - Tabla completa con información detallada
  - Indicadores visuales de estado (activo/inactivo)
  - Acciones de editar/inhabilitar con confirmaciones
- **Funciones principales:**
  - `fetchUsuarios()`: Cargar lista completa desde API
  - `handleDelete()`: Inhabilitar usuario (no eliminar)
  - `handleEdit()`: Abrir modal de edición
  - `getStatusClass()`: Aplicar estilos según estado

#### **CrearUsuario.jsx** (`src/components/Usuarios/`)
- **Propósito:** Formulario de alta de nuevos usuarios administrativos
- **Validaciones implementadas:**
  - Email único en el sistema
  - Contraseña con requisitos de seguridad
  - Todos los campos obligatorios
  - Formato de email válido

#### **EditarUsuario.jsx** (`src/components/Usuarios/`)
- **Propósito:** Modal de edición de datos de usuarios existentes
- **Capacidades:**
  - Actualización de información personal
  - Cambio de estado activo/inactivo
  - Modificación de roles de usuario
  - Validación de cambios antes de guardar

### **4. Componentes de Seguridad**

#### **ProtectedRoute.jsx** (`src/components/`)
- **Propósito:** Protección de rutas administrativas
- **Funcionamiento:**
  - Verificación de autenticación con hook `useAuth`
  - Redirección automática a login si no autenticado
  - Preservación de ruta de destino para redirección post-login
  - Integración con React Router para navegación

### **5. Herramientas de Desarrollo**

#### **BackendToggle.jsx** (`src/components/BackendToggle/`)
- **Propósito:** Alternador entre backend real y datos mock
- **Disponibilidad:** Solo visible en modo desarrollo
- **Características avanzadas:**
  - Widget draggable para reposicionamiento
  - Verificación automática de salud del backend
  - Persistencia de configuración en localStorage
  - Diagnóstico de conexión integrado
  - Interfaz visual de estado de conexión

#### **DiagnosticTool.jsx** (`src/components/DiagnosticTool/`)
- **Propósito:** Herramienta de diagnóstico de problemas de conexión
- **Pruebas que realiza:**
  - Verificación de configuración del sistema
  - Health check del backend Spring Boot
  - Test de endpoints principales de API
  - Validación de configuración CORS
  - Análisis de respuestas HTTP detallado

## 🎣 Custom Hooks y Lógica de Negocio

### **useAuth Hook** (`src/hooks/useAuth.js`)
- **Propósito:** Gestión centralizada de autenticación y sesión de usuario
- **Estados gestionados:**
  - `user`: Datos completos del usuario actual logueado
  - `isAuthenticated`: Estado booleano de autenticación
- **Funciones implementadas:**
  - `login(userData)`: Procesar login y almacenar datos de sesión
  - `logout()`: Cerrar sesión y limpiar datos almacenados
  - `hasPermission(role)`: Verificar permisos específicos de usuario
- **Persistencia:** Utiliza localStorage para mantener sesión entre recargas
- **Validaciones:** Verificación flexible de roles (ADMIN, super-admin)

## 🌐 API REST - Integración y Endpoints

### **Base URL Frontend:** `http://localhost:5173`
### **Base URL Backend:** `http://localhost:3000/api`

### **ApiService** (`src/services/apiService.js`)
- **Propósito:** Cliente HTTP centralizado para todas las comunicaciones
- **Características principales:**
  - Soporte dual para backend real y modo mock para desarrollo
  - Manejo centralizado de errores con logging detallado
  - Cache automático de imágenes en localStorage
  - Headers automáticos con tokens de autenticación
  - Configuración CORS para comunicación cross-origin

#### **Métodos de Autenticación:**
| Método | Función | Descripción |
|--------|---------|-------------|
| `login(credenciales)` | Autenticar usuario | Valida email/password y obtiene datos de sesión |
| `logout()` | Cerrar sesión | Limpia tokens y datos de usuario |
| `checkBackendHealth()` | Verificar backend | Comprueba estado de conexión con el servidor |

#### **Métodos de Gestión de Productos:**
| Método | Función | Descripción |
|--------|---------|-------------|
| `getProductos()` | Listar productos | Obtiene inventario completo desde API/mock |
| `createProducto(data)` | Crear producto | Agrega nuevo producto al inventario |
| `updateProducto(id, data)` | Actualizar producto | Modifica producto existente |
| `deleteProducto(id)` | Eliminar producto | Remueve producto del sistema |

#### **Métodos de Gestión de Usuarios:**
| Método | Función | Descripción |
|--------|---------|-------------|
| `getUsuarios()` | Listar usuarios | Obtiene lista completa de usuarios del sistema |
| `createUsuario(data)` | Crear usuario | Registra nuevo usuario con rol administrativo |
| `updateUsuario(id, data)` | Actualizar usuario | Modifica datos de usuario existente |
| `deleteUsuario(id)` | Inhabilitar usuario | Cambia estado a inactivo (no elimina) |

#### **Sistema Avanzado de Imágenes:**
| Método | Función | Descripción |
|--------|---------|-------------|
| `setProductImage(id, url)` | Guardar en cache | Almacena URL de imagen en localStorage |
| `getProductImage(id)` | Recuperar del cache | Obtiene imagen cacheada para producto |

### **Configuración API** (`src/config/api.js`)
- **API_CONFIG:** Configuración principal del sistema con endpoints
- **MOCK_DATA:** Datos de prueba completos para desarrollo sin backend
- **ERROR_MESSAGES:** Mensajes de error estandarizados y localizados

---

## ⚙️ Configuración del Sistema

### **Configuración de Vite** (`vite.config.js`)
```javascript
export default defineConfig({
  plugins: [react()],
  server: {
    port: 5173,                    // Puerto del servidor de desarrollo
    strictPort: true,              // Fallar si puerto está ocupado
    host: true                     // Permitir acceso desde red local
  }
})
```

### **Configuración de Variables de Entorno**
- **Modo Desarrollo:** `import.meta.env.DEV` - Habilita herramientas de debug
- **Modo Producción:** Optimizaciones automáticas de Vite
- **Backend Toggle:** Solo visible en desarrollo para facilitar testing

### **Configuración de API** (`src/config/api.js`)
```javascript
export const API_CONFIG = {
    USE_REAL_BACKEND: false,                           // Alternar backend real/mock
    BASE_URL: 'http://localhost:3000/api',             // URL base del backend
    HEALTH_CHECK_URL: 'http://localhost:3000/api/health', // Endpoint de salud
    ENDPOINTS: {
        LOGIN: '/usuarios/login',                      // Autenticación
        USUARIOS: '/usuarios',                         // Gestión de usuarios
        PRODUCTOS: '/productos',                       // Gestión de productos
        // ... más endpoints
    },
    ERROR_MESSAGES: {
        NETWORK_ERROR: 'Error de conexión...',         // Mensajes localizados
        UNAUTHORIZED: 'No autorizado...',
        // ... más mensajes
    }
};
```

## 🛣️ Configuración de Rutas y Navegación

### **Configuración Principal de Rutas** (`src/App.jsx`)

#### **Rutas Públicas (Acceso libre):**
| Ruta | Componente | Descripción | Función |
|------|------------|-------------|---------|
| `/` | `Home.jsx` | Página de inicio | Presentación de la marca y navegación principal |
| `/contacto` | `Contacto.jsx` | Información de contacto | Datos de contacto y redes sociales |
| `/login` | `Login.jsx` | Autenticación | Formulario de login para administradores |

#### **Rutas Protegidas (Requieren autenticación):**
| Ruta | Componente | Descripción | Función |
|------|------------|-------------|---------|
| `/inventario` | `Inventario.jsx` | Gestión de productos | Listado completo y administración de inventario |
| `/crear-producto` | `CrearProducto.jsx` | Crear producto | Formulario de alta de nuevos productos |
| `/admin-usuarios` | `Adminusuarios.jsx` | Gestión de usuarios | Panel de administración de usuarios del sistema |
| `/crear-usuario` | `CrearUsuario.jsx` | Crear usuario | Formulario de registro de nuevos administradores |

#### **Rutas de Fallback:**
| Ruta | Comportamiento | Descripción |
|------|----------------|-------------|
| `*` | `Navigate to="/"` | Cualquier ruta no definida redirige al inicio |

### **Sistema de Protección de Rutas:**
- **ProtectedRoute:** Wrapper que verifica autenticación antes de permitir acceso
- **Redirección inteligente:** Preserva la ruta de destino para redirección post-login
- **Estado de sesión:** Integración con hook `useAuth` para verificación de permisos

## 🎨 Sistema de Estilos y Diseño

### **Tema Visual de la Marca**
- **Colores principales:**
  - `#b0417a`: Rosa principal de la marca Kebumy
  - `#925c93`: Rosa secundario para degradados
  - `#e8e2d8`: Fondo beige claro y cálido
  - `#cfc7bf`: Gris neutro para navbar y elementos

### **Estilos Globales** (`src/styles/GlobalStyles.css`)
- Definición de variables CSS custom properties
- Estilos de componentes comunes reutilizables
- Diseño responsive con breakpoints definidos
- Clases utilitarias para estados (activo/inactivo)
- Estilos para modales, tablas y formularios

### **Integración con Bootstrap 5.3.8**
- Framework CSS base para componentes predefinidos
- Sistema de grid responsive de 12 columnas
- Componentes como modales, botones y alertas
- Clases utilitarias para spacing y typography
- Customización de variables Bootstrap con tema Kebumy

### **Diseño Responsive Implementado**
- **Mobile First:** Diseño optimizado para móviles primero
- **Breakpoints definidos:**
  - Mobile: < 768px
  - Tablet: 768px - 1024px  
  - Desktop: > 1024px
- **Adaptaciones específicas:**
  - Navegación colapsible en móviles
  - Tablas con scroll horizontal
  - Botones optimizados para touch
  - Imágenes adaptativas con max-width

## 🧪 Testing y Debugging del Sistema

### **Herramientas de Desarrollo Integradas**

#### **BackendToggle** (`src/components/BackendToggle/BackendToggle.jsx`)
- **Propósito:** Alternar entre backend Spring Boot real y datos mock
- **Disponibilidad:** Solo visible en modo desarrollo (`import.meta.env.DEV`)
- **Características avanzadas:**
  - Widget draggable para reposicionamiento en pantalla
  - Verificación automática de salud del backend
  - Persistencia de configuración en localStorage
  - Diagnóstico detallado de conexión
  - Interfaz visual de estado de conexión

#### **DiagnosticTool** (`src/components/DiagnosticTool/DiagnosticTool.jsx`)
- **Propósito:** Diagnóstico completo de problemas de conexión
- **Pruebas automáticas que realiza:**
  - Verificación de configuración del sistema
  - Health check del backend en puerto 3000
  - Test de endpoints principales de API REST
  - Validación de configuración CORS
  - Análisis de headers y respuestas HTTP

### **Sistema de Logging y Debugging**
- **Console logs estructurados** con prefijos por funcionalidad:
  - 🔐 Autenticación
  - 📦 Productos  
  - 👥 Usuarios
  - 🌐 API Calls
  - 🖼️ Sistema de imágenes
- **Niveles de log** por ambiente de desarrollo
- **Source maps habilitados** para debugging en navegador
- **React Developer Tools** completamente compatible

### **Endpoints de Prueba Disponibles**
```bash
# Verificar estado del servidor backend
GET http://localhost:3000/api/health

# Test de conexión a base de datos  
GET http://localhost:3000/api/productos/test

# Verificar configuración CORS
GET http://localhost:3000/api/test-cors

# Frontend development server
GET http://localhost:5173
```

## 🔒 Seguridad Implementada

### **Validaciones de Entrada**
- Email único verificado en tiempo real
- Campos requeridos validados con Yup schemas
- Tipos de datos verificados antes del envío
- Estados válidos para usuarios y productos

### **Protección de Datos**
- Tokens de autenticación en headers automáticos
- Validación de sesión activa para rutas protegidas
- Manejo seguro de errores sin exposición de información sensible
- LocalStorage usado de forma segura para persistencia

### **Configuración CORS Frontend**
- Configurado para comunicarse con backend en puerto 3000
- Headers específicos para autenticación
- Credenciales controladas en requests
- Manejo de preflight requests OPTIONS

## 📊 Patrones de Diseño Utilizados

1. **Component-Based Architecture:** Separación clara en componentes reutilizables
2. **Custom Hooks Pattern:** Lógica compartida mediante hooks personalizados
3. **Service Layer Pattern:** Abstracción de llamadas API en servicio centralizado
4. **Protected Routes Pattern:** Seguridad de navegación mediante HOCs
5. **Container/Presentational Pattern:** Separación de lógica y presentación
6. **Observer Pattern:** Estado reactivo con React hooks

## 🔧 Herramientas de Desarrollo y Optimización

- **Vite:** Build tool moderno con HMR y optimizaciones automáticas
- **ESLint:** Linter configurado con reglas de React y mejores prácticas
- **React DevTools:** Extensión compatible para debugging de componentes
- **Hot Module Replacement:** Recarga instantánea durante desarrollo
- **Source Maps:** Debugging con código fuente original
- **Tree Shaking:** Eliminación automática de código no utilizado

## 📈 Escalabilidad y Mantenimiento

### **Estructura Modular**
- Cada componente tiene responsabilidades específicas y bien definidas
- Fácil agregar nuevas funcionalidades siguiendo patrones establecidos
- Servicios reutilizables con interfaces consistentes
- Configuración centralizada para fácil mantenimiento

### **Configuración Flexible**
- Variables de entorno para diferentes modos de ejecución
- Configuración de API externalizada y modificable
- Temas y estilos organizados en archivos separados
- Sistema de build optimizable para diferentes entornos

## 🎯 Objetivos Académicos Cumplidos

1. **✅ Arquitectura por Componentes:** Implementación completa con separación clara
2. **✅ SPA con Routing:** Navegación fluida con React Router DOM
3. **✅ Integración con API:** Comunicación completa con backend REST
4. **✅ Gestión de Estado:** Implementación eficiente con React Hooks
5. **✅ Validaciones:** Formularios con validación client-side robusta
6. **✅ Responsive Design:** Interfaz adaptable a dispositivos móviles
7. **✅ Autenticación:** Sistema completo de login y protección de rutas
8. **✅ CRUD Completo:** Operaciones completas para usuarios y productos
9. **✅ Manejo de Errores:** Sistema robusto de feedback y logging
10. **✅ Documentación:** Código bien documentado y estructura clara

---

## 📊 Flujo de Datos

### **1. Autenticación:**
```
Login Form → apiService.login() → useAuth.login() → localStorage → Protected Routes
```

### **2. Gestión de Productos:**
```
Productos Component → apiService.getProductos() → State Update → UI Render
```

### **3. Creación de Elementos:**
```
Form Submit → Validation → apiService.create*() → Success → Navigation → List Refresh
```

---

## 🚨 Sistema de Notificaciones

### **Tipos de Alertas:**

#### **JavaScript Alerts:**
- Confirmaciones de creación exitosa
- Errores de operaciones
- Confirmaciones de eliminación

#### **Mensajes de Error en UI:**
- Contenedores estilizados con Bootstrap
- Estados de error por componente
- Indicadores de carga

#### **Ubicaciones:**
- **Login:** Errores de autenticación
- **Usuarios:** Confirmaciones y errores CRUD
- **Productos:** Validaciones y confirmaciones
- **Backend:** Alertas de conexión

---

## 📱 Diseño Responsive

### **Breakpoints:**
- **Mobile:** < 768px
- **Tablet:** 768px - 1024px
- **Desktop:** > 1024px

### **Adaptaciones:**
- Navegación colapsible en móviles
- Tablas scrollables horizontalmente
- Botones optimizados para touch
- Imágenes adaptativas

---

## 🔒 Seguridad

### **Autenticación:**
- Tokens JWT (preparado para backend)
- Validación de sesión
- Logout automático en errores 401

### **Autorización:**
- Rutas protegidas por rol
- Verificación de permisos
- Acceso controlado a funcionalidades admin

### **Validación:**
- Validación client-side con Yup
- Sanitización de inputs
- Validación de archivos de imagen

---

## 🧪 Modo de Desarrollo vs Producción

### **Desarrollo:**
- Backend toggle visible
- Datos mock disponibles
- Herramientas de diagnóstico
- Logging detallado en consola

### **Producción:**
- Solo backend real
- Optimizaciones de Vite
- Assets minificados
- Error handling production-ready

---

## 📈 Funcionalidades Avanzadas

### **Sistema de Imágenes:**
- Cache automático en localStorage
- Soporte múltiples formatos
- Fallbacks automáticos
- Optimización de carga

### **Gestión de Estado:**
- React Hooks para estado local
- Context implícito via props
- Persistencia en localStorage

### **Optimización:**
- Lazy loading preparado
- Code splitting por rutas
- Optimización de bundle con Vite

---

## 🐛 Debugging y Logs

### **Sistema de Logging:**
- Console.log estructurado
- Prefijos por funcionalidad (🔐, 📦, 🌐)
- Niveles de log por ambiente

### **Herramientas de Debug:**
- React Developer Tools compatible
- Source maps habilitados
- Error boundaries preparados

---

## 📋 Checklist de Funcionalidades

### ✅ **Completadas:**
- [x] Sistema de autenticación
- [x] CRUD completo de productos
- [x] CRUD completo de usuarios
- [x] Diseño responsive
- [x] Validación de formularios
- [x] Sistema de imágenes
- [x] Navegación protegida
- [x] Manejo de errores
- [x] Herramientas de desarrollo

### 🔄 **Posibles Mejoras Futuras:**
- [ ] Implementación de notificaciones toast
- [ ] Sistema de roles más granular
- [ ] Paginación en listados
- [ ] Filtros avanzados
- [ ] Exportación de datos
- [ ] Dashboard con estadísticas
- [ ] Chat de soporte
- [ ] PWA (Progressive Web App)

---

## 👩‍🏫 Notas para Evaluación

### **Aspectos Técnicos Destacados:**

1. **Arquitectura Limpia:** Separación clara de responsabilidades
2. **Código Reutilizable:** Componentes modulares y hooks personalizados
3. **Gestión de Estado:** Implementación eficiente con React Hooks
4. **Experiencia de Usuario:** Interfaz intuitiva y responsive
5. **Manejo de Errores:** Sistema robusto de validación y feedback
6. **Herramientas de Desarrollo:** Toggle y diagnóstico para facilitar testing

### **Patrones de Desarrollo Aplicados:**
- **Component-Based Architecture**
- **Custom Hooks Pattern**
- **Service Layer Pattern**
- **Protected Routes Pattern**
- **Error Boundary Pattern**

### **Buenas Prácticas Implementadas:**
- Validación tanto client-side como preparada para server-side
- Manejo centralizado de API calls
- Persistencia de sesión de usuario
- Feedback visual para todas las acciones
- Código documentado y estructurado

---

## 📞 Información de Contacto del Proyecto

**Empresa:** Kebumy  
**Email:** kebumy.cliente@gmail.com  
**Instagram:** @kebumy  
**Descripción:** Diseños únicos que reflejan lo especial que quieres transmitir  

---

## 📄 Licencia

Este proyecto es desarrollado como parte de evaluación académica.

---

**Desarrollado por:** Danny y Cony  
**Framework:** React 19.1.1 + Vite 7.1.7  
**Fecha:** Octubre 2025  
**Propósito:** Proyecto académico - Frontend de Sistema de Gestión
