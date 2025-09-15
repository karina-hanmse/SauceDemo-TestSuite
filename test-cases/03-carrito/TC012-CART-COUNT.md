# TC012-CART - Validar contador de carrito múltiples productos

## 📋 Información General
- **ID:** TC012-CART
- **Módulo:** Carrito de compras
- **Prioridad:** Alta
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 15/09/2025

## 🎯 Objetivo
Verificar que el contador del carrito se actualiza correctamente al agregar y remover múltiples productos diferentes, manteniendo la cuenta exacta en todo momento.

## 📚 Precondiciones
- [ ] Navegador Chrome instalado
- [ ] Conexión a internet estable
- [ ] Usuario logueado satisfactoriamente en el sitio
- [ ] Username: standard_user
- [ ] Password: secret_sauce
- [ ] Estar en la página de productos (/inventory.html)
- [ ] Carrito inicialmente vacío (contador en 0 o invisible)
- [ ] Al menos 3 productos disponibles en la página
- [ ] SO: Windows 11 Home

## 🧪 Datos de Prueba
| Campo         | Valor                    | Notas |
|-------        |-------                   |-------|
| Usuario       | standard_user            | Usuario estándar sin problemas |
| Producto 1    | Sauce Labs Backpack      | Primer producto a agregar |
| Producto 2    | Sauce Labs Bike Light    | Segundo producto a agregar |
| Producto 3    | Sauce Labs Bolt T-Shirt  | Tercer producto a agregar |
| Secuencia     | Agregar 3, remover 1     | Para validar diferentes estados |

## 🔄 Pasos de Ejecución

### Paso 1: Verificación del estado inicial
**Acción:** Confirmar que el carrito está vacío
**Resultado Esperado:** 
- Contador de carrito no visible o muestra "0"
- Todos los productos muestran botón "Add to cart"
- Página de productos carga correctamente

### Paso 2: Agregar primer producto
**Acción:** Hacer clic en "Add to cart" del Sauce Labs Backpack
**Resultado Esperado:** 
- Contador cambia a "1"
- Botón cambia a "Remove"
- Badge del carrito aparece y muestra "1"

### Paso 3: Agregar segundo producto
**Acción:** Hacer clic en "Add to cart" del Sauce Labs Bike Light
**Resultado Esperado:** 
- Contador se actualiza a "2"
- Botón del segundo producto cambia a "Remove"
- Badge del carrito muestra "2"

### Paso 4: Agregar tercer producto
**Acción:** Hacer clic en "Add to cart" del Sauce Labs Bolt T-Shirt
**Resultado Esperado:** 
- Contador se actualiza a "3"
- Botón del tercer producto cambia a "Remove"
- Badge del carrito muestra "3"

### Paso 5: Verificar contenido del carrito
**Acción:** Hacer clic en el ícono del carrito para verificar productos
**Resultado Esperado:** 
- Navegación exitosa a página de carrito (/cart.html)
- Los 3 productos aparecen listados correctamente
- Información de cada producto es precisa
- Contador en página coincide con badge

### Paso 6: Remover un producto desde página carrito
**Acción:** Remover el segundo producto (Sauce Labs Bike Light) desde el carrito
**Resultado Esperado:** 
- Producto se remueve de la lista
- Contador se actualiza a "2"
- Los otros 2 productos permanecen

### Paso 7: Regresar a página productos y verificar
**Acción:** Navegar de vuelta a página de productos y verificar estados
**Resultado Esperado:** 
- Contador sigue mostrando "2"
- Productos 1 y 3 muestran "Remove"
- Producto 2 muestra "Add to cart"

## ✅ Criterios de Aceptación
- [ ] Contador se actualiza correctamente con cada adición
- [ ] Contador se actualiza correctamente con cada remoción
- [ ] Badge del carrito muestra número exacto en todo momento
- [ ] Consistencia entre contador y contenido real del carrito
- [ ] Estados de botones coherentes con contador
- [ ] Sincronización entre página productos y página carrito

## 🐛 Posibles Defectos a Observar
- Contador no se actualiza al agregar productos
- Contador no se actualiza al remover productos
- Número mostrado no coincide con productos reales
- Delay o lag en actualización del contador
- Contador se resetea incorrectamente
- Inconsistencia entre páginas (productos vs carrito)
- Problemas de sincronización
- Contador muestra números negativos o incorrectos

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [15/09/2025]
- **Navegador:** Chrome
- **SO:** Windows 11 Home
- **Estado:** ✅ Pass
- **Tiempo de ejecución:** [X segundos]

## 📝 Observaciones
[Completar después de la ejecución]

## 🔍 Evidencia de Prueba
- **Video ejecución completa:** "SauceDemo-TestSuite\evidence\videos\TC012-CarritoMultiple1.wmv"

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-CART-003 (Contador preciso del carrito)
- **Requisito UX:** REQ-UX-005 (Feedback visual continuo del estado del carrito)
- **Historia de usuario:** US-CART-003 (Como usuario quiero ver siempre cuántos productos tengo en mi carrito)
- **Casos relacionados:** 
  - TC010-CART (Agregar producto al carrito)
  - TC011-CART (Remover producto del carrito)
  - TC001-LOGIN (Login exitoso prerrequisito)
  - Futuros TC013+ (Proceso de checkout)
- **Documentación técnica:** [Especificaciones de carrito SauceDemo]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Precisión contador    | 100%            | 100%            | ✅ Pass   |
| Tiempo actualización  | < 1 segundo     | 0.9 segundos    | ✅ Pass   |
| Sincronización páginas| 100%            | 100%            | ✅ Pass   |
| Consistencia estados  | Sí              | Sí              | ✅ Pass   |

## 🛡️ Validaciones de Funcionalidad
- ✅ Contador se actualiza correctamente en todas las operaciones
- ✅ Sincronización perfecta entre diferentes páginas
- ✅ Estados visuales coherentes en todo momento
- ✅ Performance aceptable en actualizaciones múltiples
- ✅ Funcionalidad robusta con múltiples productos

## 🧮 Matriz de Validación de Estados
| Acción | Contador Esperado | Estado Producto 1 | Estado Producto 2 | Estado Producto 3 |
|--------|------------------|-------------------|-------------------|-------------------|
| Inicial | 0                | Add to cart      | Add to cart       | Add to cart |
| +Prod1  | 1                | Remove           | Add to cart       | Add to cart |
| +Prod2  | 2                | Remove           | Remove            | Add to cart |
| +Prod3  | 3                | Remove           | Remove            | Remove |
| -Prod2  | 2                | Remove           | Add to cart       | Remove |

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 15/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 15/09/2025 | Ejecución  del caso | Karina Hanmse |

---
**Última actualización:** 15/09/2025
**Revisado por:** [Karina Hanmse]