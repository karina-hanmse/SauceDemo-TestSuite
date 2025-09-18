# TC015-CHECKOUT - Validación de formulario de datos personales

## 📋 Información General
- **ID:** TC015-CHECKOUT
- **Módulo:** Proceso de compra (Checkout)
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 16/09/2025

## 🎯 Objetivo
Verificar que el sistema valida correctamente el formato y contenido de los datos ingresados en el formulario de checkout, rechazando datos inválidos pero aceptando formatos correctos.

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
| Campo           | Datos Válidos    | Datos Inválidos        | Notas |
|-------          |-------           |-------                 |-------|
| First Name      | Juan, María      | 123, @#$, (vacío)      | Solo letras esperadas |
| Last Name       | Pérez, García    | 456, !@#, (vacío)      | Solo letras esperadas |
| Postal Code     | 1234, A1B2C3     | abc, @#$, (muy largo)  | Formato postal válido |

## 🔄 Pasos de Ejecución

### Paso 1: Navegación al formulario
**Acción:** Desde carrito con productos, hacer clic en "Checkout"
**Resultado Esperado:** 
- Navegación exitosa a (/checkout-step-one.html)
- Formulario con 3 campos visible
- Campos inicialmente vacíos y listos para entrada

### Paso 2: Probar datos inválidos en First Name
**Acción:** Ingresar datos inválidos: "123" en First Name, completar otros campos válidos
**Resultado Esperado:** 
- Sistema rechaza datos inválidos
- Mensaje de error específico para formato de nombre
- Campo se marca visualmente como inválido
- No permite continuar

### Paso 3: Probar datos inválidos en Last Name
**Acción:** Corregir First Name, ingresar "!@#" en Last Name, mantener Postal Code válido
**Resultado Esperado:** 
- Sistema rechaza caracteres especiales en apellido
- Mensaje de error apropiado
- First Name mantiene valor válido
- Validación específica para Last Name

### Paso 4: Probar datos inválidos en Postal Code
**Acción:** Corregir Last Name, ingresar código postal inválido muy largo o con caracteres especiales
**Resultado Esperado:** 
- Sistema valida formato de código postal
- Mensaje de error específico para Postal Code
- Otros campos mantienen valores válidos
- Validación granular funciona

### Paso 5: Probar longitudes extremas
**Acción:** Ingresar nombres muy largos (más de 50 caracteres) en campos
**Resultado Esperado:** 
- Sistema maneja límites de caracteres apropiadamente
- Trunca o rechaza entradas excesivamente largas
- Mensajes claros sobre límites de longitud
- Comportamiento consistente

### Paso 6: Validar datos correctos
**Acción:** Ingresar datos válidos: "Juan", "Pérez", "1234"
**Resultado Esperado:** 
- Sistema acepta todos los datos válidos
- No hay mensajes de error
- Botón "Continue" habilitado
- Puede proceder al siguiente paso

### Paso 7: Verificar combinaciones mixtas
**Acción:** Probar un campo válido, otro inválido simultáneamente
**Resultado Esperado:** 
- Validación independiente por campo
- Solo campos inválidos muestran error
- Campos válidos conservan estado correcto
- Experiencia de usuario clara

## ✅ Criterios de Aceptación
- [ ] Sistema rechaza datos con formato incorrecto
- [ ] Validaciones específicas para cada tipo de campo
- [ ] Mensajes de error claros y útiles
- [ ] Campos válidos mantienen valores durante validación
- [ ] Límites de longitud manejados apropiadamente
- [ ] Datos válidos son aceptados sin problemas

## 🐛 Posibles Defectos a Observar
- Sistema acepta datos claramente inválidos
- Validaciones muy estrictas que rechazan datos válidos
- Mensajes de error confusos o incorrectos
- Campos pierden valores durante validación
- Inconsistencia en validación entre campos
- Falta de validación de longitud de caracteres
- Comportamiento errático con caracteres especiales
- Problemas con diferentes tipos de entrada

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [18/09/2025]
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ❌ Fail
- **Tiempo de ejecución:** [X segundos]

## 📝 Observaciones
- El sistema permite ingresar datos inválidos en cualquiera de los campos.
- El sistema permite continuar con la compra.
## 🔍 Evidencia de Prueba
- **Screenshot datos inválidos First Name:** "SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step1.png"
"SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step1-1.png"
- **Screenshot datos inválidos Last Name:** "SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step2-1.png"
"SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step2.png"
- **Screenshot datos inválidos Postal Code:** "SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step3-1.png"
"SauceDemo-TestSuite\evidence\screenshots\TC015-Check-valida-Step3.png"
- **Screenshot datos válidos aceptados:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step2-3.png"
- **Video ejecución completa:** [Ruta del video]

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CHECKOUT-003 (Validación de formato de datos)
- **Requisito calidad:** REQ-QUALITY-001 (Integridad de datos)
- **Historia de usuario:** US-CHECKOUT-003 (Como sistema debo asegurar que los datos ingresados sean válidos)
- **Casos relacionados:** 
  - TC013-CHECKOUT (Checkout exitoso con datos válidos)
  - TC014-CHECKOUT (Campos obligatorios vacíos)
  - TC006-LOGIN (Validación de credenciales incorrectas)
- **Documentación técnica:** [Especificaciones de validación SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Rechazo datos inválidos| 100%           | 0%            | ❌ Pendiente   |
| Aceptación datos válidos| 100%          | 100%           | ✅ Pendiente   |
| Mensajes apropiados   | Sí              | No        | ❌ Pendiente   |
| Validación granular   | Sí              | No         | ❌ Pendiente   |

## 🛡️ Validaciones de Funcionalidad
- ❌ Validación de formato funciona correctamente
- ❌ Datos inválidos son rechazados apropiadamente
- ✅ Datos válidos son aceptados sin problemas
- ❌ Mensajes de error útiles y claros
- ❌ Comportamiento consistente entre campos

## 🎯 Matriz de Casos de Validación
| Campo | Entrada | Resultado Esperado |
|-------|---------|-------------------|
| First Name | "Juan" | ✅ Válido |
| First Name | "123" | ❌ Inválido - solo letras |
| First Name | "@#$" | ❌ Inválido - caracteres especiales |
| Last Name | "Pérez" | ✅ Válido |
| Last Name | "456" | ❌ Inválido - solo letras |
| Postal Code | "1234" | ✅ Válido |
| Postal Code | "A1B2C3" | ✅ Válido (alfanumérico) |
| Postal Code | "abc" | ❌ Inválido - formato |
| Todos | Muy largos (>50 chars) | ❌ Inválido - longitud |

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 16/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.0 | 18/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 18/09/2025
**Revisado por:** [Karina Hanmse]