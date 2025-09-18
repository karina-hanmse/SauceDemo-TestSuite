# TC014-CHECKOUT - Checkout con campos obligatorios vacíos

## 📋 Información General
- **ID:** TC014-CHECKOUT
- **Módulo:** Proceso de compra (Checkout)
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 16/09/2025

## 🎯 Objetivo
Verificar que el sistema valida correctamente los campos obligatorios durante el checkout y previene continuar el proceso sin completar la información requerida.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] **Carrito con al menos 1 producto agregado** (prerequisito)
- [ ] Estar en página de formulario checkout (/checkout-step-one.html)
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo           | Valor                 | Notas |
|-------          |-------                |-------|
| Usuario         | standard_user         | Usuario estándar sin problemas |
| First Name      | Sin completar         | Campo vacío |
| Last Name       | Sin completar         | Campo vacío |
| Postal Code     | Sin completar         | Campo vacío |
| Productos       | Al menos 1 en carrito | Prerequisito del flujo |

## 🔄 Pasos de Ejecución

### Paso 1: Navegación al formulario
**Acción:** Desde carrito con productos, hacer clic en "Checkout"
**Resultado Esperado:** 
- Navegación exitosa a (/checkout-step-one.html)
- Formulario con campos First Name, Last Name, Postal Code visible
- Campos inicialmente vacíos

### Paso 2: Verificar estado inicial de campos
**Acción:** Observar formulario sin completar ningún campo
**Resultado Esperado:** 
- Todos los campos vacíos
- Botón "Continue" disponible
- No hay mensajes de error iniciales

### Paso 3: Intentar continuar con campos vacíos
**Acción:** Hacer clic en botón "Continue" sin completar ningún campo
**Resultado Esperado:** 
- Sistema no permite continuar
- Mensaje de error apropiado indicando campos obligatorios
- Permanece en página de formulario
- Campos se mantienen enfocados para edición

### Paso 4: Verificar mensajes de validación
**Acción:** Observar mensajes de error mostrados
**Resultado Esperado:** 
- Mensajes claros indicando qué campos son obligatorios
- Mensajes específicos para cada campo (no genéricos)
- Colores o indicadores visuales apropiados
- Campos requeridos claramente identificados

### Paso 5: Completar parcialmente y probar
**Acción:** Completar solo First Name: "Juan", dejar otros vacíos, click Continue
**Resultado Esperado:** 
- Sistema aún no permite continuar
- Mensajes de error solo para campos faltantes
- Campo completado mantiene su valor
- Validación granular por campo

### Paso 6: Verificar comportamiento de campos individuales
**Acción:** Probar diferentes combinaciones de campos vacíos
**Resultado Esperado:** 
- Validación específica para cada campo faltante
- Campos completados conservan sus valores
- Mensajes de error actualizados dinámicamente

## ✅ Criterios de Aceptación
- [ ] Sistema previene continuar con campos vacíos
- [ ] Mensajes de error claros y específicos
- [ ] Validación funciona para cada campo individualmente
- [ ] Campos completados mantienen sus valores
- [ ] No hay navegación indebida sin datos completos
- [ ] Indicadores visuales apropiados para campos requeridos

## 🐛 Posibles Defectos a Observar
- Sistema permite continuar sin completar campos obligatorios
- Mensajes de error ausentes o genéricos
- Validación no funciona correctamente
- Campos pierden valores al mostrar errores
- Navegación indebida a siguiente página
- Mensajes de error confusos o incorrectos
- Problemas de usabilidad en validaciones
- Errores de JavaScript en consola

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 18/09/2025
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:**  ✅Pass
- **Tiempo de ejecución:** 06.68 segundos

## 📝 Observaciones
- El sistema no permite continuar con la compra si falta alguno de los datos o todos. Dependiendo del campo que queda vacío envía el mensaje correspondiente. Cabe destacar que sería apropiado incluir un mensaje no tan genérico en el caso que falten más de un campo. Ejemplo: First name and Last Name is required. ( Si faltasen ambos al mismo tiempo)

## 🔍 Evidencia de Prueba
- **Screenshot formulario vacío:** "SauceDemo-TestSuite\evidence\screenshots\TC014-checkempty-step1.png"
- **Screenshot mensajes error:** "SauceDemo-TestSuite\evidence\screenshots\TC014-checkempty-step2.png"
- **Screenshot validación parcial:** "SauceDemo-TestSuite\evidence\screenshots\TC014-checkempty-step3.png"
- **Video ejecución completa:** "SauceDemo-TestSuite\evidence\videos\TC014-checkEmpty-Completo.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CHECKOUT-002 (Validación de campos obligatorios)
- **Requisito seguridad:** REQ-SEC-003 (Prevención de datos incompletos)
- **Historia de usuario:** US-CHECKOUT-002 (Como sistema debo validar que se complete información requerida)
- **Casos relacionados:** 
  - TC013-CHECKOUT (Checkout exitoso con datos válidos)
  - TC015-CHECKOUT (Validación de formulario)
  - TC003-LOGIN, TC004-LOGIN, TC005-LOGIN (Casos similares de validación)
- **Documentación técnica:** [Especificaciones de validación SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Validación efectiva   | 100%            | 100%            | ✅ Pass   |
| Mensajes claros       | Sí              | Sí              | ✅ Pass   |
| Prevención navegación | 100%            | 100%            | ✅ Pass   |
| Campos conservados    | Sí              | Sí              | ✅ Pass   |

## 🛡️ Validaciones de Funcionalidad
- ✅ Sistema valida correctamente campos obligatorios
- ✅ Mensajes de error apropiados y útiles
- ✅ No hay bypass de validaciones
- ✅ Experiencia de usuario clara en caso de error
- ✅ Comportamiento consistente con otros formularios

## 🎯 Matriz de Validación
| Campos Completados | Resultado Esperado |
|------------------- |-------------------|
| Ninguno            | Error: todos los campos requeridos |
| Solo First Name    | Error: Last Name y Postal Code requeridos |
| Solo Last Name     | Error: First Name y Postal Code requeridos |
| Solo Postal Code   | Error: First Name y Last Name requeridos |
| First + Last       | Error: Postal Code requerido |
| First + Postal     | Error: Last Name requerido |
| Last + Postal      | Error: First Name requerido |

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 16/09/2025 | Creación inicial del caso | Karina Hanmse |
  1.0 | 18/09/2025 | Ejecución del caso | Karina Hanmse | 

---
**Última actualización:** 18/09/2025
**Revisado por:** [Karina Hanmse]