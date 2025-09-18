# Bug Report - BUG-005

## Información General
- **ID del Bug:** BUG-005-CHECKOUT
- **Detectado en:** TC013-CHECKOUT (Checkout exitoso con datos válidos)
- **Módulo:** Checkout - Resumen de compra
- **Severidad:** Media
- **Prioridad:** Media
- **Estado:** Abierto
- **Reportado por:** Karina Hanmse
- **Fecha:** 16/09/2025

## Resumen
Los datos de envío/facturación ingresados en el formulario no aparecen en la página de resumen de checkout, impidiendo al usuario verificar su información antes de completar la compra.

## Descripción Detallada
Durante el proceso de checkout, después de ingresar los datos personales (First Name, Last Name, Postal Code) y navegar a la página de resumen (/checkout-step-two.html), la información de envío/facturación no se muestra en pantalla. Esto impide que el usuario pueda verificar y confirmar que sus datos son correctos antes de finalizar la compra.

## Precondiciones
- Navegador Chrome
- Usuario logueado: standard_user / secret_sauce
- Carrito con productos
- Proceso de checkout iniciado
- Datos válidos ingresados en formulario
- SO: Windows 11 Home

## Pasos para Reproducir
1. Loguearse exitosamente con standard_user
2. Agregar producto al carrito
3. Navegar a carrito (/cart.html)
4. Hacer clic en "Checkout"
5. Completar formulario con datos válidos:
   - First Name: "Juan"
   - Last Name: "Pérez"
   - Postal Code: "1234"
6. Hacer clic en "Continue"
7. **Observar página de resumen (/checkout-step-two.html)**

## Resultado Esperado
- **La página de resumen debería mostrar información de envío/facturación ingresada**
- **Datos claramente visibles: First Name, Last Name, Postal Code**
- **Sección etiquetada como "Información de Envío" o similar**
- **Consistencia con mejores prácticas de e-commerce**

## Resultado Actual
- **NO muestra información de envío/facturación**
- **Página de resumen omite datos ingresados por el usuario**
- **Falta verificación visual de datos antes de compra**
- **Usuario no puede confirmar exactitud de información**

## Impacto
**Experiencia de Usuario:**
- Usuario no puede verificar datos antes de comprar
- Falta de confianza en que los datos fueron capturados correctamente
- Posible abandono del proceso por falta de transparencia

**Usabilidad:**
- Violación de mejores prácticas de e-commerce
- Paso de verificación incompleto
- Proceso de checkout menos transparente

**Negocio:**
- Potencial pérdida de conversiones
- Experiencia de compra sub-óptima
- Falta de confirmación de datos de entrega

## Datos del Ambiente
- **SO:** Windows 11 Home
- **Navegador:** Chrome (versión actual)
- **URL inicial:** https://www.saucedemo.com/cart.html
- **URL afectada:** https://www.saucedemo.com/checkout-step-two.html
- **Usuario:** standard_user
- **Fecha de detección:** 16/09/2025

## Evidencia
- **Screenshot formulario completado:** `evidence/screenshots/TC013-CHECKOUT-Step2-3.png`
- **Screenshot resumen sin datos:** `evidence/screenshots/TC013-CHECKOUT-Step4-5.png`
- **Video evidencia:** `evidence/videos/TC013-CHECKOUT-SUCCESS_edit.wmv`
- **Caso de prueba:** TC013-CHECKOUT-SUCCESS.md

## Sugerencias de Solución
1. **Mostrar datos de envío:** Agregar sección en resumen que muestre First Name, Last Name, Postal Code
2. **Sección claramente etiquetada:** "Información de Envío" o "Datos de Facturación"
3. **Permitir edición:** Link para regresar y modificar datos si es necesario
4. **Consistencia:** Aplicar mismo patrón en todos los flujos de checkout
5. **Validación visual:** Permitir al usuario confirmar datos antes de finalizar

## Casos de Prueba Relacionados
- TC014-CHECKOUT: Campos vacíos (verificar si problema persiste)
- TC015-CHECKOUT: Validación de formulario (puede verse afectado)

## Frecuencia de Reproducción
- **Reproducible:** Sí
- **Frecuencia:** 100% (siempre ocurre)
- **Intermitente:** No
- **Usuarios afectados:** Todos (por confirmar)

## Etiquetas
`checkout` `resumen` `datos-envio` `informacion` `ux` `verification` `media`

## Criterios de Aceptación para Fix
- [ ] Datos ingresados en formulario aparecen en página de resumen
- [ ] Información claramente etiquetada y formateada
- [ ] Datos coinciden exactamente con lo ingresado
- [ ] Layout no se ve afectado negativamente
- [ ] Funcionalidad consistente en diferentes navegadores
- [ ] Testing de regresión exitoso

## Notas Adicionales
- **Severidad Media:** No bloquea funcionalidad pero afecta experiencia
- **Prioridad Media:** Importante para transparencia del proceso
- **Scope:** Verificar comportamiento en otros flujos de checkout
- **Tipo:** Defecto de UX/Información

---

**Reportado por:** Karina Hanmse  
**Última actualización:** 16/09/2025  
**Próxima revisión:** Pendiente equipo de desarrollo  
**Área responsable:** Frontend/UX + Desarrollo