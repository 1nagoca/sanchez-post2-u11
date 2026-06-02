# PostContenido 2 - Unidad 11

## Logging Profesional y Documentación de API con Swagger

### Autor

Camilo Sánchez

### Descripción del Proyecto

Este proyecto corresponde al laboratorio PostContenido 2 de la Unidad 11 de Programación Web.

El objetivo principal fue mejorar una API REST de catálogo de productos mediante la implementación de:

* Logging profesional con SLF4J.
* Configuración avanzada de Logback.
* Generación automática de archivos de log.
* Documentación interactiva con Swagger OpenAPI.
* Buenas prácticas de monitoreo y trazabilidad.

La aplicación permite registrar todas las operaciones realizadas sobre los productos y documentar automáticamente los endpoints REST para facilitar su consumo y mantenimiento.

---

## Arquitectura Implementada

```text
Cliente HTTP
      |
      v
+----------------------+
| ProductoController   |
+----------------------+
           |
           v
+----------------------+
| ProductoServiceImpl  |
| (SLF4J Logging)      |
+----------------------+
           |
           v
+----------------------+
| ProductoRepository   |
+----------------------+
           |
           v
+----------------------+
| Base de Datos        |
+----------------------+

           ^
           |
+----------------------+
| Swagger OpenAPI      |
+----------------------+

           ^
           |
+----------------------+
| Logback + SLF4J      |
+----------------------+
```

---

### Crear producto

```http
POST /api/productos
```

Respuestas:

```http
201 Created
400 Bad Request
```

---

### Eliminar producto

```http
DELETE /api/productos/{id}
```

Respuestas:

```http
204 No Content
404 Not Found
```

---

# Conclusiones

Se implementó una solución profesional de monitoreo y documentación para una API REST utilizando SLF4J, Logback y SpringDoc OpenAPI. Los logs permiten realizar seguimiento detallado de las operaciones realizadas por los usuarios, mientras que Swagger UI facilita la comprensión y prueba de los endpoints, mejorando significativamente la mantenibilidad y calidad del proyecto.
