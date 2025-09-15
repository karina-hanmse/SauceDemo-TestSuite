# TC008-NAV - Click en logo "Swag Labs"

## 📋 Información General
- **ID:** TC008-NAV
- **Módulo:** Navegación - Cabecera
- **Prioridad:** Media
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 05/09/2025

## 🎯 Objetivo
Verificar que al hacer clic en el logo "Swag Labs" de la cabecera, el usuario es redirigido a la página de productos.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: problem_user
- [ ] Password: secret_sauce
- [ ] URL actual: https://www.saucedemo.com/inventory.html
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo       | Valor         | Notas |
|-------      |-------        |-------|
| Usuario     | problem_user  | Usuario con problemas de UI |
| Elemento    | Logo "Swag Labs" | En cabecera de la página |
| Acción      | Click simple  | Sin datos de entrada adicionales |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación de estado inicial
**Acción:** Confirmar que se está en la página de productos tras login exitoso
**Resultado Esperado:** URL muestra saucedemo.com/inventory.html

### Paso 2: Localizar logo "Swag Labs"
**Acción:** Identificar el logo "Swag Labs" en la cabecera de la página
**Resultado Esperado:** Logo visible y aparentemente clickeable

### Paso 3: Click en logo "Swag Labs"
**Acción:** Hacer clic en el texto/logo "Swag Labs"
**Resultado Esperado:** 
- Redirección a la página de productos (inventory)
- URL se mantiene o actualiza apropiadamente
- Página se recarga o navega correctamente

### Paso 4: Verificar resultado de navegación
**Acción:** Observar el comportamiento tras el clic
**Resultado Esperado:** Usuario permanece o regresa a la página de productos

## ✅ Criterios de Aceptación
- [ ] Logo "Swag Labs" es clickeable
- [ ] Redirección funciona correctamente
- [ ] Usuario llega a página de productos
- [ ] No hay errores de navegación

## 🐛 Posibles Defectos a Observar
- Logo no es clickeable (sin cursor pointer)
- No hay redirección tras el clic
- Redirección a página incorrecta
- Errores 404 o de carga
- Comportamiento inconsistente

## 📊 Resultado de Ejecución
- **Ejecutado por:** Karina Hanmse
- **Fecha:** 09/09/2025
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ❌ FAIL
- **Tiempo de ejecución:** N/A

## 📝 Observaciones
- Sawg Labs es texto plano
- El logo No es clickleable, es texto plano.
- Sería importante fuera un texto cursor pointer.
- **BUG DETECTADO:** Ver BUG-002-NAV
## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot Logo Visible:** "evidence\screenshots\TC008-NAV- SAWG-STEPS2-logovisible09092025.png"
- **Screenshot error:** "evidence\screenshots\TC008-NAV- SAWG-STEPS309092025.png"
- **Video ejecución completa:** "evidence\videos\TC008-NAV-SWAG.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-NAV-002 (Navegación por logo/home)
- **Requisito UX:** REQ-UX-002 (Logo como elemento de navegación estándar)
- **Historia de usuario:** US-NAV-002 (Como usuario espero que el logo me lleve a la página principal)
- **Casos relacionados:** 
  - TC007-NAV (Menú lateral izquierdo)
  - TC001-LOGIN (Login exitoso prerrequisito)
- **Documentación técnica:** [Especificaciones de navegación SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com/inventory.html

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Navegación exitosa    | 100%            | 0%              | ❌ Fail   |
| Tiempo de redirección | < 2 segundos    | N/A             | ❌ Fail   |
| Sin errores           | Sí              | No              | ❌ Fail   |
| Funcionalidad estándar| Sí              | No              | ❌ Fail   |

## 🛡️ Validaciones de Funcionalidad
- ❌ Logo no es clickleable
- ❌ Falta implementación de navegación estándar
- ❌ No cumple con convenciones de UX (logo = home)
- ❌ Posible problema de usabilidad
- ❌ Inconsistencia en elementos de navegación

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 05/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 05/09/2025 | Ejecución caso de prueba  | Karina Hanmse |

---
**Última actualización:** 09/09/2025
**Revisado por:** [Karina Hanmse]