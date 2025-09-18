# 🐛 Bug Report - BUG-006

## 📋 Información General
- **ID del Bug:** BUG-006-CHECKOUT
- **Detectado en:** TC015-CHECKOUT (Validación de formulario de datos personales)
- **Módulo:** Checkout - Validación de datos
- **Severidad:** Alta
- **Prioridad:** Alta
- **Estado:** Abierto
- **Reportado por:** Karina Hanmse
- **Fecha:** 18/09/2025

## 🎯 Resumen
El sistema acepta datos claramente inválidos en el formulario de checkout (números en nombres, caracteres especiales, formatos incorrectos) y permite continuar con el proceso de compra sin validación de formato.

## 🔍 Descripción Detallada
Durante las pruebas de validación del formulario de checkout, se detectó que el sistema no realiza validación de formato en ninguno de los campos (First Name, Last Name, Postal Code). Acepta datos como números en campos de nombres, caracteres especiales, y permite proceder al siguiente paso con información claramente inválida.

## 📚 Precondiciones
- Navegador Chrome
- Usuario logueado: standard_user / secret_sauce
- Carrito con productos
- Estar en página de formulario checkout (/checkout-step-one.html)
- SO: Windows 11 Home

## 🔄 Pasos para Reproducir
1. Loguearse exitosamente con standard_user
2. Agregar producto al carrito
3. Navegar a checkout y llegar al formulario
4. Ingresar datos inválidos:
   - First Name: "123" (números)
   - Last Name: "!@#" (caracteres especiales)
   - Postal Code: "abc@#$" (formato incorrecto)
5. Hacer clic en "Continue"
6. **Observar que el sistema acepta los datos y continúa**

## ✅ Resultado Esperado
- **Sistema debe rechazar datos con formato incorrecto**
- **Mensajes de error específicos para cada tipo de validación**
- **Prevenir navegación con datos inválidos**
- **Validación en tiempo real o al enviar formulario**

## ❌ Resultado Actual
- **Sistema acepta números en campos de nombres**
- **Sistema acepta caracteres especiales en todos los campos**
- **No hay validación de formato en ningún campo**
- **Permite continuar con datos claramente inválidos**
- **Datos inválidos se procesan en pasos siguientes**

## 🎯 Impacto
**Calidad de Datos:**
- Datos inválidos ingresan al sistema
- Información de envío/facturación incorrecta
- Problemas potenciales en procesamiento de órdenes

**Seguridad:**
- Posibles inyecciones de caracteres especiales
- Falta de sanitización de entrada de datos
- Vulnerabilidades de validación del lado cliente

**Experiencia de Usuario:**
- Usuario puede ingresar datos incorrectos sin darse cuenta
- Problemas posteriores en entrega por datos inválidos
- Falta de guías sobre formatos esperados

**Negocio:**
- Órdenes con información de contacto inválida
- Problemas de entrega y facturación
- Costo de procesamiento manual de correcciones

## 📊 Datos del Ambiente
- **SO:** Windows 11 Home
- **Navegador:** Chrome (versión actual)
- **URL afectada:** https://www.saucedemo.com/checkout-step-one.html
- **Usuario:** standard_user
- **Fecha de detección:** 18/09/2025

## 📸 Evidencia
- **Screenshot datos inválidos First Name:** `evidence/screenshots/TC015-Check-valida-Step1.png`
- **Screenshot datos inválidos Last Name:** `evidence/screenshots/TC015-Check-valida-Step2.png`
- **Screenshot datos inválidos Postal Code:** `evidence/screenshots/TC015-Check-valida-Step3.png`
- **Caso de prueba:** TC015-CHECKOUT-VALIDATION.md

## 💡 Sugerencias de Solución
1. **Implementar validación de formato:**
   - First Name/Last Name: solo letras y espacios
   - Postal Code: formato alfanumérico según estándares
2. **Validación en tiempo real:** Feedback inmediato durante escritura
3. **Mensajes de error específicos:** Indicar formato esperado
4. **Longitud de campos:** Límites apropiados para cada campo
5. **Sanitización:** Limpiar entrada de caracteres potencialmente peligrosos

## 🔗 Casos de Prueba Relacionados
- TC014-CHECKOUT: Campos vacíos (funciona correctamente)
- TC013-CHECKOUT: Datos válidos (acepta correctamente)

## 📈 Frecuencia de Reproducción
- **Reproducible:** Sí
- **Frecuencia:** 100% (siempre ocurre)
- **Intermitente:** No
- **Campos afectados:** Todos (First Name, Last Name, Postal Code)
- **Usuarios afectados:** Todos

## 🏷️ Etiquetas
`checkout` `validacion` `formato` `datos-invalidos` `seguridad` `calidad` `alta`

## 📋 Criterios de Aceptación para Fix
- [ ] Sistema rechaza números en campos de nombres
- [ ] Sistema rechaza caracteres especiales inapropiados
- [ ] Validación específica para formato de código postal
- [ ] Mensajes de error claros indicando formato esperado
- [ ] Validación consistente en todos los campos del formulario
- [ ] Testing de regresión exitoso con datos válidos e inválidos

## 🔄 Notas Adicionales
- **Severidad Alta:** Afecta integridad de datos y seguridad
- **Prioridad Alta:** Debe corregirse antes de producción
- **Scope:** Verificar otros formularios del sistema
- **Tipo:** Defecto de validación/seguridad

---

**Reportado por:** Karina Hanmse  
**Última actualización:** 18/09/2025  
**Próxima revisión:** Urgente - Equipo de desarrollo  
**Área responsable:** Frontend + Backend validation