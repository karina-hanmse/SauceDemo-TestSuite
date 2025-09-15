# TC011-CART - Remover producto del carrito

## 📋 Información General
- **ID:** TC011-CART
- **Módulo:** Carrito de compras
- **Prioridad:** Alta
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 15/09/2025

## 🎯 Objetivo
Verificar que un usuario puede remover exitosamente un producto del carrito de compras y que el sistema actualiza correctamente el estado del carrito.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] Estar en la página de productos (/inventory.html)
- [ ] **Carrito con al menos 1 producto agregado** (prerequisito del TC010)
- [ ] Producto "Sauce Labs Backpack" ya agregado al carrito
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo       | Valor                    | Notas |
|-------      |-------                   |-------|
| Usuario     | standard_user            | Usuario estándar sin problemas |
| Producto    | Sauce Labs Backpack      | Producto previamente agregado |
| Estado inicial | 1 producto en carrito  | Contador debe mostrar "1" |
| Acción      | Click "Remove"           | Botón específico del producto |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación del estado inicial
**Acción:** Confirmar que hay un producto en el carrito
**Resultado Esperado:** 
- Contador de carrito muestra "1"
- Botón del producto muestra "Remove"
- Producto visible en página de productos con estado "agregado"

### Paso 2: Localizar botón "Remove"
**Acción:** Identificar el botón "Remove" del producto "Sauce Labs Backpack"
**Resultado Esperado:** 
- Botón "Remove" visible y habilitado
- Producto identificado correctamente

### Paso 3: Remover producto del carrito
**Acción:** Hacer clic en el botón "Remove" del Sauce Labs Backpack
**Resultado Esperado:** 
- Botón cambia de "Remove" a "Add to cart"
- Contador de carrito se actualiza a "0" o desaparece
- No hay errores visuales o de funcionalidad

### Paso 4: Verificar actualización del carrito
**Acción:** Observar los cambios en la interfaz tras remover el producto
**Resultado Esperado:** 
- Icono de carrito no muestra badge o muestra "0"
- Botón del producto cambió de "Remove" a "Add to cart"
- Estado visual del producto se actualiza apropiadamente

### Paso 5: Verificar contenido del carrito
**Acción:** Hacer clic en el ícono del carrito para verificar que está vacío
**Resultado Esperado:** 
- Navegación exitosa a página de carrito (/cart.html)
- Carrito muestra estado vacío
- No aparece el producto removido
- Mensaje apropiado de "carrito vacío" (si aplica)

## ✅ Criterios de Aceptación
- [ ] Producto se remueve exitosamente del carrito
- [ ] Contador de carrito se actualiza correctamente (0 o invisible)
- [ ] Botón cambia de "Remove" a "Add to cart"
- [ ] Carrito muestra estado vacío al verificar
- [ ] No quedan rastros del producto removido
- [ ] No hay errores de funcionalidad o visuales

## 🐛 Posibles Defectos a Observar
- Botón "Remove" no responde al clic
- Contador de carrito no se actualiza correctamente
- Producto permanece en el carrito tras remover
- Estado del botón no cambia apropiadamente
- Errores en el cálculo del total o cantidad
- Producto removido aparece duplicado
- Performance lenta en la actualización
- Problemas de sincronización entre páginas

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [15/09/2025]
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ✅ Pass
- **Tiempo de ejecución:** [2.0 segundos]

## 📝 Observaciones
No hay nada que observar

## 🔍 Evidencia de Prueba
- **Screenshot estado inicial:** "SauceDemo-TestSuite\evidence\screenshots\TC011-addcart_estadoInicial.png"
- **Screenshot botón Remove:** "SauceDemo-TestSuite\evidence\screenshots\TC011-addtocart-step2_1-urlcart.png"
- **Screenshot producto removido:** "SauceDemo-TestSuite\evidence\screenshots\TC011-addtocart-step2_2-cartsinproductos.png"
- **Screenshot carrito vacío:** "SauceDemo-TestSuite\evidence\screenshots\TC011-addtocart-step2-remove.png"
- **Video ejecución completa:** "SauceDemo-TestSuite\evidence\videos\TC011-VideoCompleto.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CART-002 (Remover productos del carrito)
- **Requisito UX:** REQ-UX-004 (Feedback visual al remover productos)
- **Historia de usuario:** US-CART-002 (Como usuario quiero poder remover productos que ya no deseo comprar)
- **Casos relacionados:** 
  - TC010-CART (Agregar producto al carrito - prerrequisito)
  - TC012-CART (Validar contador de carrito)
  - TC001-LOGIN (Login exitoso prerrequisito)
  - Futuros TC013+ (Proceso de checkout)
- **Documentación técnica:** [Especificaciones de carrito SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de respuesta   | < 2 segundos    | [2.0 segundos]  | ✅ Pass  |
| Actualización contador| 100%            | 100%            | ✅ Pass  |
| Cambio estado botón   | Sí              | Sí              | ✅ Pass  |
| Carrito vacío         | Sí              | Sí              | ✅ Pass  |

## 🛡️ Validaciones de Funcionalidad
- ✅ Producto se remueve correctamente del carrito
- ✅ Contador se actualiza de forma inmediata
- ✅ Estados visuales se actualizan apropiadamente
- ✅ Carrito queda en estado limpio tras remoción
- ✅ Funcionalidad consistente con estándares de e-commerce

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 15/09/2025 | Creación inicial del caso | Karina Hanmse 
| 1.1 | 15/09/2025 | Ejecución del caso | Karina Hanmse 

---
**Última actualización:** 15/09/2025
**Revisado por:** [Karina Hanmse]