# TC009-NAV - Navegación con botón "Back" del browser

## 📋 Información General
- **ID:** TC009-NAV
- **Módulo:** Navegación - Browser
- **Prioridad:** Media
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 05/09/2025

## 🎯 Objetivo
Verificar que la navegación con el botón "Back" del navegador funciona correctamente manteniendo el estado de sesión del usuario.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo           | Valor                 | Notas |
|-------          |-------                |-------|
| Usuario         | standard_user         | Usuario estándar sin problemas |
| Página inicial  | /inventory.html       | Página de productos |
| Producto        | Cualquiera disponible | Para navegar a detalle |
| Navegación      | Botón Back browser    | Funcionalidad nativa |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación de estado inicial
**Acción:** Confirmar que se está en la página de productos tras login exitoso
**Resultado Esperado:** URL muestra saucedemo.com/inventory.html y productos visibles

### Paso 2: Navegación a detalle de producto
**Acción:** Hacer clic en cualquier producto para acceder a su página de detalle
**Resultado Esperado:** 
- Navegación exitosa a página de detalle del producto
- URL cambia a /inventory-item.html?id=X
- Información del producto se muestra correctamente

### Paso 3: Usar botón "Back" del navegador
**Acción:** Hacer clic en el botón "Atrás" (←) del navegador
**Resultado Esperado:** 
- Regreso a la página de inventario/productos
- URL vuelve a /inventory.html
- Lista de productos se mantiene visible
- Estado de sesión se conserva

### Paso 4: Verificar integridad de la sesión
**Acción:** Verificar que todos los elementos de la página funcionan correctamente
**Resultado Esperado:** 
- Usuario sigue logueado
- Todos los productos siguen disponibles
- Funcionalidades de la página operativas
- No hay errores de carga

## ✅ Criterios de Aceptación
- [ ] Botón Back funciona correctamente
- [ ] Regreso exitoso a página de productos
- [ ] Estado de sesión se mantiene
- [ ] No hay errores de navegación o carga
- [ ] Página de destino se carga completamente

## 🐛 Posibles Defectos a Observar
- Botón Back no funciona o genera error
- Pérdida de sesión al usar navegación del browser
- Página no carga correctamente tras el Back
- Redirección incorrecta o loop infinito
- Elementos de la página no funcionan tras navegación
- Performance lenta en el regreso

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [11/09/2025]
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ✅ Pass
- **Tiempo de ejecución:** 2.3 segundos

## 📝 Observaciones
No hay observaciones

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** "evidence\screenshots\TC009-step1_urlvisible.png"
- **Screenshot Paso 2:** "evidence\screenshots\TC009-step2_urlcambia.png"
- **Screenshot Paso 3:** "evidence\screenshots\TC009-step3_backproduct01.png"
                         "evidence\screenshots\TC009-step3_backproduct01.png"
- **Video ejecución completa:** "evidence\videos\TC009-nav-back-completo.wmv"


## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-NAV-003 (Compatibilidad con navegación de browser)
- **Requisito técnico:** REQ-TECH-001 (Manejo correcto de historial de navegación)
- **Historia de usuario:** US-NAV-003 (Como usuario quiero poder usar los controles estándar del navegador)
- **Casos relacionados:** 
  - TC007-NAV (Menú lateral izquierdo)
  - TC008-NAV (Click en Swag Labs)
  - TC001-LOGIN (Login exitoso prerrequisito)
  - Futuros TC010+ (Navegación entre productos)
- **Documentación técnica:** [Especificaciones de navegación SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de navegación  | < 3 segundos    | 2.3segundos     | ✅ Pass  |
| Mantenimiento sesión  | 100%            | 100%            | ✅ Pass  |
| Carga completa página | Sí              | Sí              | ✅ Pass  |
| Sin errores           | Sí              | Sí              | ✅ Pass  |

## 🛡️ Validaciones de Funcionalidad
- ✅ Navegación Back responde correctamente
- ✅ No hay pérdida de estado de sesión
- ✅ Página de destino carga sin errores
- ✅ Compatibilidad con controles estándar del browser
- ✅ Performance aceptable en navegación

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 05/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 11/09/2025 | Ejecución del caso | Karina Hanmse 

---
**Última actualización:** 11/09/2025
**Revisado por:** [Karina Hanmse]