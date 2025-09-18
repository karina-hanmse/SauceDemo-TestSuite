# TC013-CHECKOUT - Checkout exitoso con datos válidos

## 📋 Información General
- **ID:** TC013-CHECKOUT
- **Módulo:** Proceso de compra (Checkout)
- **Prioridad:** Crítica
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 15/09/2025

## 🎯 Objetivo
Verificar que un usuario puede completar exitosamente todo el proceso de checkout ingresando datos válidos y que el sistema procesa la compra correctamente.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] **Carrito con al menos 1 producto agregado** (prerequisito)
- [ ] Estar en página de carrito (/cart.html) con productos
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo           | Valor                 | Notas |
|-------          |-------                |-------|
| Usuario         | standard_user         | Usuario estándar sin problemas |
| First Name      | Juan                  | Nombre válido |
| Last Name       | Pérez                 | Apellido válido |
| Postal Code     | 1234                  | Código postal válido |
| Productos       | Al menos 1 en carrito | Prerequisito del flujo |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación del estado inicial
**Acción:** Confirmar que se está en la página del carrito con productos
**Resultado Esperado:** 
- URL muestra /cart.html
- Al menos 1 producto visible en el carrito
- Botón "Checkout" disponible y habilitado

### Paso 2: Iniciar proceso de checkout
**Acción:** Hacer clic en el botón "Checkout"
**Resultado Esperado:** 
- Navegación exitosa a página de información (/checkout-step-one.html)
- Formulario de datos personales se muestra correctamente
- Campos First Name, Last Name y Postal Code visibles

### Paso 3: Completar datos personales
**Acción:** Ingresar datos válidos en todos los campos
- First Name: "Juan"
- Last Name: "Pérez"  
- Postal Code: "1234"
**Resultado Esperado:** 
- Datos se ingresan correctamente en cada campo
- No hay errores de validación
- Botón "Continue" habilitado

### Paso 4: Continuar al resumen
**Acción:** Hacer clic en el botón "Continue"
**Resultado Esperado:** 
- Navegación exitosa a página de resumen (/checkout-step-two.html)
- Información del producto mostrada correctamente
- Información de envío/facturación visible
- Total de la compra calculado correctamente

### Paso 5: Verificar información de resumen
**Acción:** Revisar toda la información mostrada en el resumen
**Resultado Esperado:** 
- Productos listados con precios correctos
- Datos de envío coinciden con lo ingresado
- Cálculos (subtotal, tax, total) son precisos
- Botón "Finish" disponible

### Paso 6: Completar la compra
**Acción:** Hacer clic en el botón "Finish"
**Resultado Esperado:** 
- Navegación exitosa a página de confirmación (/checkout-complete.html)
- Mensaje de confirmación de compra exitosa
- Información de confirmación apropiada

### Paso 7: Verificar estado post-compra
**Acción:** Navegar de vuelta a productos y verificar carrito
**Resultado Esperado:** 
- Carrito queda vacío (contador en 0 o invisible)
- Productos vuelven a mostrar "Add to cart"
- Estado del carrito se resetea correctamente

## ✅ Criterios de Aceptación
- [ ] Proceso de checkout se completa sin errores
- [ ] Navegación entre páginas funciona correctamente
- [ ] Validación de campos acepta datos válidos
- [ ] Cálculos de precios y totales son precisos
- [ ] Página de confirmación se muestra apropiadamente
- [ ] Carrito se limpia después de compra exitosa
- [ ] No hay errores funcionales o visuales en el flujo

## 🐛 Posibles Defectos a Observar
- Errores en navegación entre páginas de checkout
- Validación incorrecta de campos con datos válidos
- Cálculos erróneos de subtotales, impuestos o total
- Información incorrecta en página de resumen
- Fallo en procesamiento de la compra
- Carrito no se limpia después de compra exitosa
- Errores en página de confirmación
- Problemas de performance en el flujo

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 16/09/2025
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ❌ Fail
- **Tiempo de ejecución:** 28.10 segundos

## 📝 Observaciones
- El producto posee una descripción incoherente (TC010)
- Al momento de revisar resumen no aparece datos de envío y/o facturación
- Los cálculos son correctos.

## 🔍 Evidencia de Prueba
- **Screenshot carrito inicial:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step1.png"
- **Screenshot formulario datos:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step2-3.png"
- **Screenshot resumen compra:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step4-5.png"
- **Screenshot confirmación:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step6.png"
- **Screenshot carrito post-compra:** "SauceDemo-TestSuite\evidence\screenshots\TC013-CHECKOUT-Step7.png"
- **Video ejecución completa:** "SauceDemo-TestSuite\evidence\videos\TC013-CHECKOUT-SUCCESS_edit.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CHECKOUT-001 (Proceso completo de compra)
- **Requisito crítico:** REQ-BUSINESS-001 (Transacciones exitosas)
- **Historia de usuario:** US-CHECKOUT-001 (Como usuario quiero completar mi compra de forma fácil y segura)
- **Casos relacionados:** 
  - TC010-CART, TC011-CART, TC012-CART (Prerrequisitos de carrito)
  - TC014-CHECKOUT (Campos vacíos)
  - TC015-CHECKOUT (Validación de formulario)
  - TC001-LOGIN (Login exitoso prerrequisito)
- **Documentación técnica:** [Especificaciones de checkout SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo total proceso  | < 30 segundos   | 28.10           | ✅ Pass   |
| Navegación exitosa    | 100%            | 100%            | ✅ Pass   |
| Cálculos correctos    | 100%            | 100%            | ✅ Pass   |
| Limpieza carrito      | Sí              | Sí              | ✅ Pass   |
| Datos Resumen         | Sí              | No              | ❌ Fail   |

## 🛡️ Validaciones de Funcionalidad
- ✅ Flujo completo de checkout funciona sin interrupciones
- ❌ Validaciones de datos operan correctamente
- ✅ Cálculos financieros son precisos
- ✅ Estados del carrito se manejan apropiadamente
- ✅ Confirmación de compra se genera correctamente

## 🛒 Flujo de Navegación Esperado
1. `/cart.html` → Carrito con productos
2. `/checkout-step-one.html` → Formulario datos personales  
3. `/checkout-step-two.html` → Resumen de compra
4. `/checkout-complete.html` → Confirmación exitosa
5. `/inventory.html` → Vuelta a productos (carrito limpio)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 15/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 16/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 16/09/2025
**Revisado por:** [Karina Hanmse]