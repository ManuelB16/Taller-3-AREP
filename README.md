# Microframework Web en Java para Servicios REST y Archivos Estáticos
Este proyecto implementa un **microframework web en Java** que permite:
Definir servicios REST con funciones Lambda.  
Manejar parámetros de consulta (**Query Parameters**).  
Servir archivos estáticos (HTML, JS, CSS, imágenes).  

Forma parte de la evolución del **Taller 01**, pero integrando más funcionalidades para un desarrollo web sencillo y potente.

---

## Objetivos del Proyecto
- Reutilizar conceptos del **Taller 01** en un contexto más robusto.  
- Crear servicios REST dinámicos utilizando **funciones Lambda**.  
- Procesar parámetros en las URLs (`Query Params`).  
- Especificar una ubicación para **archivos estáticos** como páginas web, imágenes y estilos.  

---

## Descripción de la Aplicación

El microframework configura y ejecuta un **servidor HTTP sencillo** que soporta:  
- Rutas REST dinámicas (`/api/...`).  
- Entrega de archivos estáticos desde un directorio configurable (`resources/Files` o `webroot`).  

Sirve como base para comprender cómo funcionan frameworks reales como **Spring Boot** o **SparkJava**.

---

## Arquitectura del Sistema

- **Usuario (User):** Envía solicitudes desde el navegador.  
- **Navegador (Browser):** Realiza peticiones HTTP y procesa la respuesta.  
- **Servidor HTTP (HttpServer):** Recibe solicitudes y responde con archivos estáticos o JSON.  

Ejemplos de rutas soportadas:
- `/index.html` → página principal  
- `/code.js` → archivo JavaScript  
- `/desing.css` → hoja de estilos CSS  
- `/Imagen/Mondongo.jpg` → imágenes  
- `/api/saludo` → servicio REST JSON  
- `/api/fecha` → retorna fecha actual  

---

## Componentes principales

- **HttpServer** → Clase central del servidor.  
- **Route** → Interfaz funcional (`lambda`) para definir rutas REST.  
- **Request / Response** → Clases de apoyo para solicitudes y respuestas.  
- **Recursos estáticos** → Archivos en `resources/Files` (HTML, CSS, JS, imágenes).  
- **APIs REST** → Endpoints declarados en `HttpServer` (`/api/saludo`, `/api/fecha`, `/api/hello`).  
- **Pruebas (JUnit)** → Casos que validan el funcionamiento del servidor.  

---

## 🚀 Instalación

🔧 Se clona el repositorio y compilar:

```
git clone https://github.com/ManuelB16/Taller02-MicroFrameworks-WEB-AREP
cd Taller02-MicroFrameworks-WEB-AREP
git checkout Taller02-MicroFrameworks-WEB-AREP
mvn clean compile
```

---

## Ejecución de la Aplicación

Levanta el servidor con:

```
mvn exec:java -Dexec.mainClass="arep.taller2.web.Microframework"
```

Luego abre en tu navegador:  
👉 [http://localhost:35000/](http://localhost:35000/)  

---

## 🧪 Ejecución de Tests

Los tests garantizan que los endpoints REST funcionen correctamente:  

```
mvn test
```

### Casos de prueba principales
- **testApiSaludo** → `/api/saludo` retorna HTTP 200 OK + JSON esperado.  
- **testApiFecha** → `/api/fecha` incluye `"fecha"` en la respuesta.  
- **testApiNotFound** → rutas inválidas devuelven **404 Not Found**.  
- **testApiPostSimulado** → verifica que POST con JSON se procesa bien.  
- **testApiHello** → `/api/hello` responde correctamente.  

Ejemplo de salida:

<img width="746" height="135" alt="image" src="https://github.com/user-attachments/assets/f0cae16f-5e6b-4241-a0bf-d32bf35d283f" />

---

## Características destacadas

1. **Frontend responsivo**  
   - Diseño limpio con tonos claros.  
   - Compatible con móviles y escritorio.  
   - Panel de búsqueda de archivos.  

2. **Gestión de archivos estáticos**  
   - Soporte para **HTML, CSS, JS e imágenes** desde `resources/Files`.  
   - Entrega inmediata a través de HTTP.  

3. **Servicios REST flexibles**  
   - Endpoints definidos con **Lambda Functions**.  
   - Manejo de parámetros dinámicos (`/api/hello?name=Pedro`).  

---

## Demostración Visual

https://github.com/user-attachments/assets/55dcdeab-1104-4aff-b5ad-3ae5758ae833

---

## Autor

- **Manuel Felipe Barrera** – [ManuelB16](https://github.com/ManuelB16)  

---

## Licencia
Este proyecto está licenciado bajo **MIT**.  
Consulta el archivo [License](License.md) para más detalles.  

---

## Agradecimientos
Agradecimiento especial al **profesor Daniel Benavides** por su guía y apoyo en el desarrollo de este proyecto.  

---
