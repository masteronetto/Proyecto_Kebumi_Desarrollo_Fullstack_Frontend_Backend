# Proyecto_Kebumi_Desarrollo_Fullstack_Frontend_Backend
# 🚀 Proyecto Kebumy - Backend Spring Boot

## 📋 Descripción del Proyecto

**Proyecto Kebumy** es una aplicación backend desarrollada con **Spring Boot** que proporciona una API REST completa para la gestión de usuarios y productos. La aplicación implementa un sistema de autenticación básico, operaciones CRUD y está diseñada para trabajar con un frontend en React/Vue.js.

## 🏗️ Arquitectura del Proyecto

### **Patrón de Arquitectura Implementado**
- **Arquitectura en Capas (Layered Architecture)**
- **Patrón MVC (Model-View-Controller)**
- **Inyección de Dependencias**
- **Repository Pattern**

### **Estructura de Capas**
```
┌─────────────────────────────────────┐
│          CAPA PRESENTACIÓN          │
│            (Controllers)            │
├─────────────────────────────────────┤
│           CAPA NEGOCIO              │
│            (Services)               │
├─────────────────────────────────────┤
│         CAPA PERSISTENCIA           │
│          (Repositories)             │
├─────────────────────────────────────┤
│           CAPA DATOS                │
│         (Entities/Models)           │
└─────────────────────────────────────┘
```

## 📁 Estructura del Proyecto

```
src/main/java/com/danny/proyectokebumyspringbootbackend/
├── 📄 ProyectokebumyspringbootbackendApplication.java  # Clase principal
├── 📁 config/
│   └── 📄 CorsConfig.java                              # Configuración CORS
├── 📁 controllers/                                     # Capa de Presentación
│   ├── 📄 HealthController.java                        # Endpoints de estado
│   ├── 📄 ProductoRestController.java                  # API REST Productos
│   └── 📄 UsuarioRestController.java                   # API REST Usuarios
├── 📁 entities/                                        # Capa de Datos
│   ├── 📄 Producto.java                                # Entidad Producto
│   └── 📄 Usuario.java                                 # Entidad Usuario
├── 📁 repositories/                                    # Capa de Persistencia
│   ├── 📄 ProductoRepository.java                      # Repositorio Productos
│   └── 📄 UsuarioRepository.java                       # Repositorio Usuarios
└── 📁 services/                                        # Capa de Negocio
    ├── 📄 ProductoService.java                         # Interfaz Servicio Productos
    ├── 📄 ProductoServiceImpl.java                     # Implementación Productos
    ├── 📄 UsuarioService.java                          # Interfaz Servicio Usuarios
    └── 📄 UsuarioServiceImpl.java                      # Implementación Usuarios
```

## 🛠️ Tecnologías Utilizadas

| Tecnología | Versión | Propósito |
|-----------|---------|-----------|
| **Java** | 17 | Lenguaje de programación |
| **Spring Boot** | 3.5.6 | Framework principal |
| **Spring Data JPA** | - | Persistencia de datos |
| **Spring Web** | - | API REST |
| **Hibernate** | 6.6.29 | ORM (Mapeo Objeto-Relacional) |
| **MySQL** | 8.0.42 | Base de datos |
| **Maven** | - | Gestión de dependencias |
| **Lombok** | - | Reducción de código boilerplate |

## 🗃️ Modelo de Datos

### **Entidad Usuario**
```sql
CREATE TABLE usuario (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255),
    email VARCHAR(255) UNIQUE,
    password VARCHAR(255),
    rol VARCHAR(255) DEFAULT 'cliente',
    estado VARCHAR(255) DEFAULT 'activo',
    fecha_creacion DATETIME(6)
);
```

**Atributos y Funciones:**
- `id`: Identificador único autogenerado
- `nombre`: Nombre completo del usuario
- `email`: Correo electrónico (único en el sistema)
- `password`: Contraseña del usuario
- `rol`: Tipo de usuario (cliente, admin)
- `estado`: Estado del usuario (activo, inactivo)
- `fechaCreacion`: Timestamp automático de creación

### **Entidad Producto**
```sql
CREATE TABLE producto (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255),
    descripcion VARCHAR(255),
    precio DECIMAL(38,2),
    stock INTEGER NOT NULL,
    estado VARCHAR(255) DEFAULT 'activo',
    categoria_nombre VARCHAR(255),
    imagen_url VARCHAR(255),
    fecha_creacion DATETIME(6)
);
```

**Atributos y Funciones:**
- `id`: Identificador único autogenerado
- `nombre`: Nombre del producto
- `descripcion`: Descripción detallada
- `precio`: Precio con precisión decimal
- `stock`: Cantidad disponible en inventario
- `estado`: Estado del producto (activo, inactivo)
- `categoriaNombre`: Categoría del producto
- `imagenUrl`: URL de la imagen del producto
- `fechaCreacion`: Timestamp automático de creación

## 🔗 API REST - Endpoints Disponibles

### **Base URL:** `http://localhost:3000`

### 🔍 **Endpoints de Estado**
| Método | Endpoint | Descripción |
|--------|----------|-------------|
| `GET` | `/api/health` | Verificar estado del servidor |
| `GET` | `/api/test-cors` | Verificar configuración CORS |

### 👤 **Gestión de Usuarios**
| Método | Endpoint | Descripción | Función |
|--------|----------|-------------|---------|
| `POST` | `/api/usuarios/login` | Autenticación | Validar credenciales |
| `POST` | `/api/usuarios/registro` | Registro cliente | Crear usuario con rol 'cliente' |
| `GET` | `/api/usuarios` | Listar usuarios | Obtener todos los usuarios |
| `GET` | `/api/usuarios/{id}` | Obtener usuario | Buscar por ID específico |
| `POST` | `/api/usuarios/admin` | Crear usuario admin | Crear con cualquier rol |
| `PUT` | `/api/usuarios/{id}` | Actualizar usuario | Modificar datos existentes |
| `DELETE` | `/api/usuarios/{id}` | Eliminar usuario | Borrar usuario del sistema |

### 📦 **Gestión de Productos**
| Método | Endpoint | Descripción | Función |
|--------|----------|-------------|---------|
| `GET` | `/api/productos` | Listar productos | Obtener todos los productos |
| `GET` | `/api/productos/{id}` | Obtener producto | Buscar por ID específico |
| `POST` | `/api/productos` | Crear producto | Agregar nuevo producto |
| `PUT` | `/api/productos/{id}` | Actualizar producto | Modificar producto existente |
| `DELETE` | `/api/productos/{id}` | Eliminar producto | Borrar producto del sistema |
| `GET` | `/api/productos/stock-bajo` | Stock bajo | Productos con menos de 5 unidades |
| `GET` | `/api/productos/test` | Test conexión | Verificar conexión a BD |

## 🧩 Componentes y Funcionalidades

### **1. Capa de Presentación (Controllers)**

#### **HealthController.java**
- **Propósito:** Monitoreo y diagnóstico del sistema
- **Funciones:**
  - Verificar estado del servidor
  - Validar configuración CORS
  - Proporcionar información de conectividad

#### **UsuarioRestController.java**
- **Propósito:** API REST para gestión completa de usuarios
- **Funciones principales:**
  - **Autenticación:** Validar email y contraseña
  - **Registro:** Crear nuevos usuarios automáticamente como 'clientes'
  - **CRUD Completo:** Crear, leer, actualizar, eliminar usuarios
  - **Seguridad:** Ocultar contraseñas en respuestas
  - **Validaciones:** Email único, campos requeridos

#### **ProductoRestController.java**
- **Propósito:** API REST para gestión de inventario de productos
- **Funciones principales:**
  - **CRUD Completo:** Operaciones completas sobre productos
  - **Gestión de Inventario:** Control de stock y disponibilidad
  - **Filtros:** Búsqueda de productos con stock bajo
  - **Diagnóstico:** Endpoint de prueba para conexión

### **2. Capa de Negocio (Services)**

#### **UsuarioService & UsuarioServiceImpl**
- **Propósito:** Lógica de negocio para usuarios
- **Validaciones Implementadas:**
  - Email requerido y único en el sistema
  - Contraseña requerida
  - Estado activo para login
  - Roles válidos (cliente, admin)
- **Funciones:**
  - Creación con valores por defecto
  - Actualización selectiva (password opcional)
  - Validación de credenciales para autenticación

#### **ProductoService & ProductoServiceImpl**
- **Propósito:** Lógica de negocio para productos
- **Validaciones Implementadas:**
  - Nombre de producto requerido
  - Precio mayor a cero
  - Stock no negativo
- **Funciones:**
  - Gestión completa de inventario
  - Alertas de stock bajo
  - Logging detallado para debugging

### **3. Capa de Persistencia (Repositories)**

#### **UsuarioRepository**
- **Hereda de:** `CrudRepository<Usuario, Long>`
- **Métodos personalizados:**
  - `findByEmail(String email)`: Búsqueda por email único
- **Operaciones automáticas:** save, findById, findAll, deleteById, existsById

#### **ProductoRepository**
- **Hereda de:** `CrudRepository<Producto, Long>`
- **Métodos personalizados:**
  - `findByStockLessThan(int limite)`: Productos con stock bajo
- **Operaciones automáticas:** CRUD completo mediante herencia

### **4. Configuración (Config)**

#### **CorsConfig.java**
- **Propósito:** Habilitar comunicación con frontend
- **Configuración:**
  - **Origen permitido:** `http://localhost:5173` (puerto frontend)
  - **Métodos HTTP:** GET, POST, PUT, DELETE, OPTIONS
  - **Headers:** Todos permitidos (*)
  - **Credenciales:** Habilitadas
  - **Rutas:** Aplicado a toda la aplicación (**)

## ⚙️ Configuración de la Aplicación

### **application.properties**
```properties
# Configuración del servidor
server.port=3000

# Base de datos MySQL
spring.datasource.url=jdbc:mysql://localhost:3306/proyecto_kebumy
spring.datasource.username=root
spring.datasource.password=

# Configuración JPA/Hibernate
spring.jpa.hibernate.ddl-auto=create-drop
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
spring.jpa.show-sql=true

# Logging para desarrollo
logging.level.com.danny.proyectokebumyspringbootbackend=DEBUG
```

**Explicación de configuraciones clave:**
- `server.port=3000`: El servidor corre en puerto 3000
- `ddl-auto=create-drop`: Las tablas se recrean en cada inicio (desarrollo)
- `show-sql=true`: Muestra las consultas SQL en consola para debugging
- Logging DEBUG: Permite ver el flujo de ejecución detallado

## 🚀 Instalación y Ejecución

### **Prerrequisitos**
- Java 17 o superior
- MySQL 8.0 o superior
- Maven (incluido con wrapper)

### **Pasos para ejecutar:**

1. **Clonar el repositorio**
```bash
git clone [url-del-repositorio]
cd proyectokebumyspringbootbackend
```

2. **Configurar base de datos**
- Crear base de datos MySQL llamada `proyecto_kebumy`
- Verificar usuario `root` sin contraseña (o modificar en `application.properties`)

3. **Ejecutar la aplicación**
```bash
# Opción 1: Maven Wrapper
./mvnw spring-boot:run

# Opción 2: Desde VS Code
# Abrir ProyectokebumyspringbootbackendApplication.java y presionar F5
```

4. **Verificar funcionamiento**
- Acceder a: `http://localhost:3000/api/health`
- Debería retornar status "OK"

## 🧪 Testing y Debugging

### **Endpoints de Prueba**
```bash
# Verificar estado del servidor
GET http://localhost:3000/api/health

# Test de conexión a base de datos
GET http://localhost:3000/api/productos/test

# Verificar CORS
GET http://localhost:3000/api/test-cors
```

### **Logging Configurado**
- **SQL Queries:** Todas las consultas se muestran en consola
- **Debug Level:** Información detallada de Spring y la aplicación
- **Error Handling:** Excepciones capturadas y logs informativos

## 🔒 Seguridad Implementada

### **Validaciones de Entrada**
- Email único en el sistema
- Campos requeridos validados
- Tipos de datos verificados
- Estados válidos para usuarios y productos

### **Protección de Datos**
- Contraseñas ocultas en respuestas JSON
- Validación de estado activo para login
- Manejo de errores sin exposición de información sensible

### **CORS Configurado**
- Solo permite conexiones desde localhost:5173
- Headers y métodos específicamente definidos
- Credenciales controladas

## 📊 Patrones de Diseño Utilizados

1. **Repository Pattern:** Abstracción de la capa de datos
2. **Service Layer Pattern:** Lógica de negocio centralizada
3. **Dependency Injection:** Gestión automática de dependencias
4. **DTO Pattern:** Transferencia segura de datos (implícito)
5. **MVC Pattern:** Separación clara de responsabilidades

## 🔧 Herramientas de Desarrollo

- **Lombok:** Reduce código boilerplate (getters, setters, constructores)
- **Spring DevTools:** Recarga automática durante desarrollo
- **Maven:** Gestión de dependencias y construcción del proyecto
- **JPA/Hibernate:** ORM para mapeo objeto-relacional automático

## 📈 Escalabilidad y Mantenimiento

### **Estructura Modular**
- Cada capa tiene responsabilidades específicas
- Fácil agregar nuevas entidades siguiendo el mismo patrón
- Servicios reutilizables e interfaces bien definidas

### **Configuración Flexible**
- Propiedades externalizadas en `application.properties`
- Perfiles de Spring Boot para diferentes entornos
- Fácil migración entre bases de datos
---
**Desarrollado por:** Danny y Cony 
**Framework:** Spring Boot 3.5.6  
**Fecha:** Octubre 2025  
**Propósito:** Proyecto académico - Backend API REST
