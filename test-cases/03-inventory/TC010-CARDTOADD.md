# TC010-CART - Agregar producto al carrito

## 📋 Información General
- **ID:** TC010-CART
- **Módulo:** Carrito de compras
- **Prioridad:** Alta
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 10/09/2025

## 🎯 Objetivo
Verificar que un usuario puede agregar exitosamente un producto al carrito de compras y que el sistema actualiza correctamente el estado del carrito.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] Estar en la página de productos (/inventory.html)
- [ ] Carrito inicialmente vacío
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo       | Valor                    | Notas |
|-------      |-------                   |-------|
| Usuario     | standard_user            | Usuario estándar sin problemas |
| Producto    | Sauce Labs Backpack      | Primer producto de la lista |
| Precio      | $29.99                   | Precio esperado del producto |
| Acción      | Click "Add to cart"      | Botón específico del producto |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación del estado inicial
**Acción:** Confirmar que se está en la página de productos con carrito vacío
**Resultado Esperado:** 
- URL muestra /inventory.html
- Contador de carrito no visible o muestra "0"
- Productos disponibles en la página

### Paso 2: Localizar producto objetivo
**Acción:** Identificar el producto "Sauce Labs Backpack" en la lista
**Resultado Esperado:** 
- Producto visible con imagen, nombre y precio
- Botón "Add to cart" disponible y habilitado

### Paso 3: Agregar producto al carrito
**Acción:** Hacer clic en el botón "Add to cart" del Sauce Labs Backpack
**Resultado Esperado:** 
- Botón cambia a "Remove" 
- Contador de carrito aparece o se actualiza a "1"
- No hay errores visuales o de funcionalidad

### Paso 4: Verificar actualización del carrito
**Acción:** Observar los cambios en la interfaz tras agregar el producto
**Resultado Esperado:** 
- Icono de carrito muestra badge con número "1"
- Botón del producto cambió de "Add to cart" a "Remove"
- Estado visual del producto se actualiza apropiadamente

### Paso 5: Verificar contenido del carrito
**Acción:** Hacer clic en el ícono del carrito para ver su contenido
**Resultado Esperado:** 
- Navegación exitosa a página de carrito (/cart.html)
- Producto agregado aparece listado correctamente
- Información del producto (nombre, precio) es correcta

## ✅ Criterios de Aceptación
- [ ] Producto se agrega exitosamente al carrito
- [ ] Contador de carrito se actualiza correctamente
- [ ] Botón cambia de "Add to cart" a "Remove"
- [ ] Contenido del carrito muestra el producto correcto
- [ ] Precio y detalles del producto son precisos
- [ ] No hay errores de funcionalidad o visuales

## 🐛 Posibles Defectos a Observar
- Botón "Add to cart" no responde al clic
- Contador de carrito no se actualiza
- Producto no aparece en el carrito al verificar
- Información incorrecta del producto en carrito
- Errores de precio o cálculos
- Problemas de estado del botón (no cambia a "Remove")
- Performance lenta en la actualización

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 15/09/2025
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ❌ Fail
- **Tiempo de ejecución:** [1.8 segundos]

## 📝 Observaciones
- ✅ Producto se agrega exitosamente al carrito
- ✅ Contador de carrito se actualiza correctamente
- ✅ Botón cambia de "Add to cart" a "Remove"
- ✅ Contenido del carrito muestra el producto correcto
- ❌ Precio y detalles del producto son precisos
- ❌ Hay errores de funcionalidad o visuales

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** "SauceDemo-TestSuite\evidence\screenshots\TC010-Step1-verif_estado_inicial.png"
- **Screenshot producto agregado:** "SauceDemo-TestSuite\evidence\screenshots\TC010-Step2-localizar_producto.png"
"SauceDemo-TestSuite\evidence\screenshots\TC010-Step3-Add-to-cart.png"
- **Screenshot carrito con producto:** "SauceDemo-TestSuite\evidence\screenshots\TC010-Step5-verificar-carrito.png"
- **Video ejecución completa:** "SauceDemo-TestSuite\evidence\videos\TC010-videocompleto.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CART-001 (Agregar productos al carrito)
- **Requisito UX:** REQ-UX-003 (Feedback visual al agregar productos)
- **Historia de usuario:** US-CART-001 (Como usuario quiero agregar productos al carrito para comprarlos después)
- **Casos relacionados:** 
  - TC001-LOGIN (Login exitoso prerrequisito)
  - TC011-CART (Remover producto del carrito)
  - TC012-CART (Validar contador de carrito)
  - Futuros TC013+ (Proceso de checkout)
- **Documentación técnica:** [Especificaciones de carrito SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de respuesta   | < 2 segundos    | [1.8 segundos]  | ✅ PASS   |
| Actualización contador| 100%            | 100%            | ✅ PASS   |
| Cambio estado botón   | Sí              | Si              | ✅ PASS   |
| Datos correctos       | 100%            | 35%             | ❌ FAil   |

## 🛡️ Validaciones de Funcionalidad
- ✅ Producto se agrega correctamente al carrito
- ✅ Contador se actualiza de forma inmediata
- ✅ Estados visuales se actualizan apropiadamente
- ❌ Información del producto se mantiene íntegra
- ✅ Funcionalidad consistente con estándares de e-commerce

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 10/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 15/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 15/09/2025
**Revisado por:** [Karina Hanmse]