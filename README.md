# SauceDemo Test Suite - Manual Testing Portfolio

## Descripción del Proyecto

Este repositorio contiene una suite completa de casos de prueba manuales desarrollada para demostrar habilidades de QA Testing en un entorno de e-commerce real. Se utilizó SauceDemo como aplicación bajo prueba para ejecutar testing funcional exhaustivo.

## Objetivos Cumplidos

- **Demostrar metodología estructurada** de testing manual
- **Documentar casos de prueba** siguiendo estándares de la industria
- **Identificar y reportar defectos reales** en aplicación web
- **Generar evidencia completa** de ejecución de pruebas
- **Aplicar diferentes técnicas** de testing (positivo, negativo, casos límite)

## Estructura del Proyecto

```
SauceDemo-TestSuite/
├── casos de prueba/          # Test cases por área funcional
├── documentos/               # Documentación del proyecto  
├── evidencia/               # Screenshots y videos de ejecución
├── informes/                # Reportes y análisis
├── informes de errores/     # Bug reports documentados
├── LÉAME.md                 # Documentación principal
└── registro de cambios.md   # Historial de modificaciones
```

## Resumen de Casos de Prueba

### Cobertura Funcional
- **15 casos de prueba ejecutados**
- **4 áreas funcionales cubiertas**
- **8 casos exitosos (PASS)**
- **7 casos con defectos encontrados (FAIL)**

| Área | Casos Totales | PASS | FAIL |
|------|---------------|------|------|
| Autenticación | 4 | 3 | 1 |
| Navegación | 3 | 1 | 2 |
| Carrito | 3 | 2 | 1 |
| Checkout | 5 | 2 | 3 |

## Defectos Identificados

### 6 Bugs Reales Encontrados y Documentados

| Bug ID | Área | Severidad | Descripción |
|--------|------|-----------|-------------|
| BUG-001 | Autenticación | Media | Campos no se limpian tras error |
| BUG-002 | Navegación | Media | Logo no es clickeable |
| BUG-003 | Navegación | Menor | Menú se superpone con contenido |
| BUG-004 | Carrito | Media | Descripción de producto incorrecta |
| BUG-005 | Checkout | Media | Datos no aparecen en resumen |
| BUG-006 | Checkout | Alta | Sistema acepta datos inválidos |

## Casos de Prueba Destacados

### TC006-LOGIN - Credenciales Incorrectas
- **Defecto encontrado**: Los campos no se limpian automáticamente
- **Impacto**: Experiencia de usuario y posible riesgo de seguridad menor

### TC015-CHECKOUT - Validación de Formato
- **Defecto crítico**: Sistema acepta números en nombres y caracteres especiales
- **Impacto**: Alto - Compromete integridad de datos

### TC012-CART - Contador Múltiple
- **Caso complejo**: Validación de sincronización entre páginas
- **Resultado**: Funcionalidad robusta confirmada

## Metodología Aplicada

### Técnicas de Testing
- **Testing Funcional**: Verificación de requisitos de negocio
- **Testing Negativo**: Validación de manejo de errores
- **Testing de Usabilidad**: Experiencia de usuario
- **Testing de Compatibilidad**: Navegadores y sistemas operativos

### Documentación Estructurada
- Casos de prueba con formato estándar
- Precondiciones claramente definidas
- Pasos de ejecución detallados
- Criterios de aceptación específicos
- Evidencia completa de ejecución

### Gestión de Defectos
- Reportes de bugs con clasificación de severidad
- Pasos claros para reproducción
- Impacto en negocio y usuario final
- Sugerencias de solución

## Herramientas Utilizadas

- **Navegador**: Chrome 118+
- **SO**: Windows 11 Home
- **Documentación**: Markdown
- **Control de versiones**: Git/GitHub
- **Captura de evidencia**: Screenshots y videos
- **Aplicación bajo prueba**: https://www.saucedemo.com

## Habilidades Demostradas

### Technical Skills
- Diseño y ejecución de casos de prueba
- Identificación y reporte de defectos
- Documentación técnica estructurada
- Análisis de requisitos funcionales
- Testing de diferentes tipos (positivo/negativo)

### Soft Skills
- Atención al detalle
- Pensamiento crítico
- Comunicación técnica clara
- Organización y metodología
- Orientación a calidad

## Métricas del Proyecto

- **Tiempo total**: 3 semanas
- **Casos ejecutados**: 15
- **Defectos encontrados**: 6
- **Tasa de detección de defectos**: 40%
- **Cobertura funcional**: 4 áreas principales
- **Evidencia generada**: 50+ screenshots, 15+ videos

## Próximos Pasos

### Expansión del Portfolio
- API Testing con Postman
- Testing automatizado (Selenium)
- Testing de performance
- Mobile testing

### Mejoras Identificadas
- Implementación de testing de regresión
- Casos de prueba para diferentes navegadores
- Testing de accesibilidad
- Validaciones de seguridad más profundas

## Contacto

**Karina Hanmse**
- LinkedIn: www.linkedin.com/in/karinahanmse
- GitHub: https://github.com/karina-hanmse
- Email: karinahanmse@gmail.com

---

*Este portfolio demuestra competencias reales en testing manual y capacidad para identificar defectos críticos en aplicaciones web. Desarrollado como proyecto práctico para mostrar habilidades de QA Testing.*