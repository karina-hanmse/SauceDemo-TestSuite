# TC007-NAV - Acceso al menú lateral izquierdo

## 📋 Información General
- **ID:** TC007-NAV
- **Módulo:** Navegación - Cabecera
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** Karina Hanmse
- **Fecha:** 05/09/2025

## 🎯 Objetivo
Verificar que el menú lateral izquierdo se despliega correctamente al hacer clic en el ícono hamburguesa.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: problem_user
- [ ] Password: secret_sauce
- [ ] URL actual: https://www.saucedemo.com/inventory.html
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo       | Valor                 | Notas |
|-------      |-------                |-------|
| Usuario     | problem_user          | Usuario con problemas de UI |
| URL esperada| /inventory.html       | Página de productos |
| Acción      | Click menú            | Sin datos de entrada adicionales |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación de estado inicial
**Acción:** Confirmar que se está en la página de productos tras login exitoso
**Resultado Esperado:** URL muestra saucedemo.com/inventory.html

### Paso 2: Localizar menú hamburguesa
**Acción:** Identificar ícono de menú lateral izquierdo en la cabecera
**Resultado Esperado:** Ícono de menú (hamburguesa) visible y clickeable

### Paso 3: Activar menú lateral
**Acción:** Hacer clic en el ícono de menú lateral izquierdo
**Resultado Esperado:** 
- Se despliega un menú deslizándose de izquierda a derecha
- Menú muestra opciones de navegación
- Animación fluida y correcta

### Paso 4: Verificar contenido del menú
**Acción:** Observar opciones disponibles en el menú desplegado
**Resultado Esperado:** Menú contiene opciones válidas de navegación

## ✅ Criterios de Aceptación
- [ ] Menú se despliega correctamente
- [ ] Animación de deslizamiento funciona (izquierda a derecha)
- [ ] Opciones de menú son visibles y accesibles
- [ ] No hay errores visuales o de funcionalidad

## 🐛 Posibles Defectos a Observar
- Menú no se despliega al hacer clic
- Animación defectuosa o ausente
- Opciones de menú no visibles o mal alineadas
- Errores de responsive design
- Menú se superpone incorrectamente con contenido

## 📊 Resultado de Ejecución
- **Ejecutado por:** Karina Hanmse
- **Fecha:** 09/09/2025
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ❌ Fail
- **Tiempo de ejecución:** 0.3 segundos

## 📝 Observaciones
- Se despliega un menú que se desliza de izquierda a derecha
- Funcionamiento correcto según especificación
- El menú se superpone con parte del contenido de la página principal.

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot Menú Visible:** `"evidence\screenshots\TC-007-NAV-MENU-09092025.png"`
- **Screenshot paso2:** "`evidence\screenshots\TC007-NAV-MENU-STEPS2_MENU VISIBLE09092025.png`"
- **Screenshot paso3:** "evidence\screenshots\TC007-NAV-MENU-STEPS3-ACTIVA-MENU-LATERAL09092025.png"
- **Screenshot error:** `evidence/screenshots/TC005_step2_error_message_04092025.png`
- **Video ejecución completa:** "evidence\videos\TC007-NAV-MENU09092025.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-NAV-001 (Navegación por menú lateral)
- **Requisito UX:** REQ-UX-001 (Experiencia de usuario fluida)
- **Historia de usuario:** US-NAV-001 (Como usuario quiero acceder fácilmente a opciones de navegación)
- **Casos relacionados:** 
  - TC008-NAV (Click en Swag Labs)
  - TC001-LOGIN (Login exitoso prerrequisito)
- **Documentación técnica:** [Especificaciones de navegación SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com/inventory.html

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de despliegue  | < 1 segundo     | ~0.3 segundos   | ✅ Pass   |
| Animación fluida      | Sí              | Sí              | ✅ Pass   |
| Opciones visibles     | 100%            | 100%            | ✅ Pass   |
| Sin errores visuales  | No              | No              | ❌ Pass   |

## 🛡️ Validaciones de Funcionalidad
- ✅ Menú responde correctamente al clic
- ✅ Animación de deslizamiento funciona apropiadamente
- ❌ Hay superposición incorrecta con otros elementos
- ✅ Comportamiento consistente con estándares de UX
- ✅ Funcionalidad compatible con Windows 11 y Chrome

## 📋 Historial de Cambios
| Versión | Fecha      | Cambio Realizado             | Responsable |
|---------|--------    |------------------            |-------------|
| 1.0     | 05/09/2025 | Creación inicial del caso    | Karina Hanmse |
| 1.1     | 09/09/2025 | Ejecución del caso de prueba | Karina Hanmse |

---
**Última actualización:** 09/09/2025
**Revisado por:** Karina Hanmse