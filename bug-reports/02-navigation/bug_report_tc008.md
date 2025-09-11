# 🐛 Bug Report - BUG-002

## 📋 Información General
- **ID del Bug:** BUG-002-NAV
- **Detectado en:** TC008-NAV (Click en logo Swag Labs)
- **Módulo:** Navegación - Cabecera
- **Severidad:** Media
- **Prioridad:** Media
- **Estado:** Abierto
- **Reportado por:** Karina Hanmse
- **Fecha:** 05/09/2025

## 🎯 Resumen
El logo "Swag Labs" en la cabecera no es funcional - no responde al clic y no redirige a ninguna página, violando convenciones estándar de UX.

## 🔍 Descripción Detallada
El elemento "Swag Labs" en la cabecera aparenta ser clickeable pero no ejecuta ninguna acción al hacer clic. Según estándares de UX, los logos de sitios web deberían redirigir a la página principal o de productos.

## 📚 Precondiciones
- Navegador Chrome 
- Usuario logueado: problem_user / secret_sauce
- URL: https://www.saucedemo.com/inventory.html
- SO: Windows 11 Home

## 🔄 Pasos para Reproducir
1. Iniciar sesión exitosamente en SauceDemo
2. Confirmar que se está en página de productos (/inventory.html)
3. Localizar el texto/logo "Swag Labs" en la cabecera superior
4. Hacer clic en "Swag Labs"
5. **Observar que no ocurre ninguna acción**

## ✅ Resultado Esperado
- El logo "Swag Labs" debería ser clickeable
- Al hacer clic, debería redirigir a la página principal/productos
- Comportamiento consistente con estándares web (logo = home)
- Cursor pointer visible al pasar mouse sobre el logo

## ❌ Resultado Actual
- **No realiza ninguna acción** al hacer clic en "Swag Labs"
- No hay redirección ni navegación
- El elemento no responde al clic
- Falta funcionalidad estándar esperada por usuarios

## 🎯 Impacto
**Experiencia de Usuario:**
- Confusión al no funcionar elemento aparentemente clickeable
- Violación de convenciones estándar de navegación web
- Falta de consistencia en elementos de interfaz

**Usabilidad:**
- Los usuarios esperan que logos sean navegables
- Reducción en opciones intuitivas de navegación
- Posible frustración del usuario

**Funcionalidad:**
- Falta implementación de navegación básica esperada
- Inconsistencia con patrones de diseño web estándar

## 📊 Datos del Ambiente
- **SO:** Windows 11 Home
- **Navegador:** Chrome (versión actual)
- **Resolución:** 1920x1080
- **URL:** https://www.saucedemo.com/inventory.html
- **Usuario:** problem_user
- **Fecha de detección:** 05/09/2025

## 📸 Evidencia
- **Screenshot:** "bug-reports\evidence\screenshots\BUG002_logo_no_click11092025.png"
- **Caso de prueba:** "test-cases\02-navigation\tc008_nav_swag.md"
- **Video:**  "bug-reports\evidence\videos\BUG002_click_behavior.wmv"

## 💡 Sugerencia de Solución
1. **Hacer el logo clickeable:** Agregar funcionalidad de clic al elemento "Swag Labs"
2. **Redirección apropiada:** Que navegue a página principal/productos (/inventory.html)
3. **Indicador visual:** Agregar cursor pointer al pasar mouse sobre el logo
4. **Consistencia:** Aplicar misma funcionalidad en todas las páginas del sitio

## 🔗 Casos de Prueba Relacionados
- TC007-NAV: Menú lateral (funcionó correctamente)
- TC001-LOGIN: Login exitoso (prerrequisito)
- Futuros casos de navegación por logo en otras páginas

## 📈 Frecuencia de Reproducción
- **Reproducible:** Sí
- **Frecuencia:** 100% (siempre ocurre)
- **Intermitente:** No
- **Navegadores afectados:** Chrome (por confirmar otros)

## 🏷️ Etiquetas
`navegacion` `logo` `ux` `usabilidad` `cabecera` `media`

## 📋 Criterios de Aceptación para Fix
- [ ] Logo "Swag Labs" responde al clic
- [ ] Redirección exitosa a página de productos
- [ ] Cursor pointer visible al hover
- [ ] Funcionalidad consistente en todas las páginas
- [ ] Tiempo de navegación < 2 segundos
- [ ] Sin errores en consola del navegador

---

**Reportado por:** Karina Hanmse  
**Última actualización:** 11/09/2025  
**Próxima revisión:** Pendiente desarrollo