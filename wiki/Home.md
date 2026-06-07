# Wiki del Proyecto - Actividad 4: Testing en Unisabana

Bienvenido al Wiki oficial de documentación del proyecto de **Pruebas de Integración y Sistema** desarrollado en la Universidad de Sabana.

## Contenido del Wiki

1. **[Inicio](#inicio)** - Descripción general del proyecto
2. **[Pruebas de Integración](./02-pruebas-integracion.md)** - Validación entre capas
3. **[Pruebas de Sistema](./03-pruebas-sistema.md)** - Pruebas end-to-end
4. **[Cobertura y Resultados](./04-cobertura-resultados.md)** - Métricas de JaCoCo
5. **[Registro de Defectos](./05-registro-defectos.md)** - Defectos encontrados
6. **[Conclusiones y Reflexión](./06-conclusiones.md)** - Aprendizajes y reflexión

---

## Inicio

### Descripción del Dominio y Propósito del Sistema

Este proyecto implementa un **sistema de pruebas integral** para validar la calidad del código a través de múltiples niveles de testing:

- **Pruebas Unitarias**: Validación de componentes individuales
- **Pruebas de Integración**: Validación de la comunicación entre capas (Service ↔ Repository)
- **Pruebas de Sistema**: Validación end-to-end a través de endpoints HTTP

El sistema está diseñado para garantizar la confiabilidad, mantenibilidad y robustez de la aplicación antes de su despliegue en producción.

### Diagrama de Arquitectura

```
┌─────────────────────────────────────────────────────────┐
│                    CLIENTE HTTP                          │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│              CAPA PRESENTACIÓN                           │
│  (Controllers - REST API Endpoints)                     │
│  @RestController, @RequestMapping                       │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│              CAPA DE SERVICIOS                           │
│  (Business Logic - Service Layer)                       │
│  @Service, @Transactional                              │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│              CAPA DE PERSISTENCIA                        │
│  (Repository Layer - Data Access)                       │
│  @Repository, JpaRepository                            │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│              BASE DE DATOS H2                            │
│  (Testing Database - In-Memory)                        │
└─────────────────────────────────────────────────────────┘
```

### Integrantes del Equipo

| Rol | Responsabilidad |
|-----|-----------------|
| **Desarrollador/Tester** | lm4038882-ui | Diseño, implementación y ejecución de pruebas |

---

## Estadísticas del Proyecto

| Métrica | Valor |
|---------|-------|
| **Objetivo de Cobertura** | ≥ 80% |
| **Herramientas de Testing** | JUnit 5, Mockito, MockMvc, H2 |
| **Framework** | Spring Boot |
| **Base de Datos de Prueba** | H2 (In-Memory) |

---

## Cómo Navegar por este Wiki

Cada sección del wiki contiene:
- ✅ Descripción de las pruebas realizadas
- ✅ Configuración de anotaciones Spring Boot
- ✅ Ejemplos de código
- ✅ Capturas de ejecución
- ✅ Reportes de cobertura

**Última actualización**: 2026-06-07

---

[Siguiente: Pruebas de Integración →](./02-pruebas-integracion.md)
