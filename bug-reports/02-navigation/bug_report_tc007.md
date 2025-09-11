# 🐛 Bug Report - BUG-003

## 📋 Información General
- **ID del Bug:** BUG-003-NAV
- **Detectado en:** TC007-NAV (Acceso al menú lateral izquierdo)
- **Módulo:** Navegación - UX/Visual
- **Severidad:** Menor
- **Prioridad:** Baja
- **Estado:** Abierto
- **Reportado por:** Karina Hanmse
- **Fecha:** 09/09/2025

## 🎯 Resumen
El menú lateral izquierdo se superpone incorrectamente con el contenido de la página principal, causando problemas visuales y de usabilidad.

## 🔍 Descripción Detallada
Cuando se despliega el menú lateral izquierdo, este se superpone por encima del contenido principal de la página en lugar de desplazarlo o crear un overlay apropiado. Esto genera confusión visual y puede dificultar la lectura del contenido subyacente.

## 📚 Precondiciones
- Navegador Chrome
- Usuario logueado: problem_user / secret_sauce
- URL: https://www.saucedemo.com/inventory.html
- SO: Windows 11 Home
- Resolución: Estándar desktop

## 🔄 Pasos para Reproducir
1. Loguearse exitosamente con problem_user
2. Confirmar que se está en página de productos (/inventory.html)
3. Localizar ícono de menú hamburguesa en cabecera
4. Hacer clic en el ícono de menú lateral izquierdo
5. **Observar que el menú se superpone sobre el contenido principal**

## ✅ Resultado Esperado
**Comportamiento UX apropiado debería ser:**
- Menú se despliega sin ocultar contenido importante
- Contenido principal se desplaza hacia la derecha, O
- Se crea un overlay semi-transparente, O  
- Menú tiene un z-index apropiado que no interfiera con usabilidad

## ❌ Resultado Actual
- **El menú se superpone directamente sobre el contenido principal**
- Parte del contenido de productos queda oculto/ilegible
- No hay desplazamiento del contenido principal
- Experiencia visual confusa para el usuario

## 🎯 Impacto
**Experiencia de Usuario:**
- Confusión visual al quedar contenido oculto
- Dificultad para leer información mientras el menú está abierto
- Sensación de interfaz mal diseñada

**Usabilidad:**
- Usuario no puede ver productos completos con menú abierto
- Necesidad de cerrar menú para acceder a contenido subyacente
- Interferencia con flujo normal de navegación

**Visual/Estético:**
- Aspecto no profesional de la interfaz
- Inconsistencia con estándares de diseño web moderno

## 📊 Datos del Ambiente
- **SO:** Windows 11 Home
- **Navegador:** Chrome (versión actual)
- **URL:** https://www.saucedemo.com/inventory.html
- **Usuario:** problem_user
- **Fecha de detección:** 09/09/2025
- **Tiempo de ejecución:** 0.3 segundos

## 📸 Evidencia
- **Screenshot menú cerrado:** "evidence\screenshots\TC007-NAV-MENU-STEPS2_MENU VISIBLE09092025.png"
- **Screenshot menú abierto (problema):** `evidence/screenshots/TC007-NAV-MENU-STEPS2_MENU VISIBLE09092025.png`
- **Screenshot superposición:** `evidence/screenshots/TC007-NAV-MENU-STEPS3-ACTIVA-MENU-LATERAL09092025.png`
- **Video evidencia:** `evidence/videos/TC007-NAV-MENU09092025.wmv`
- **Caso de prueba:** "test-cases\02-navigation\tc007_nav_menu.md"

## 💡 Sugerencias de Solución
**Opción 1 - Desplazamiento:** 
- Hacer que el contenido principal se desplace hacia la derecha cuando se abre el menú

**Opción 2 - Overlay:** 
- Crear un overlay semi-transparente que oscurezca el contenido de fondo

**Opción 3 - Z-index mejorado:** 
- Ajustar capas para que el menú no interfiera visualmente con elementos importantes

**Opción 4 - Menú más pequeño:** 
- Reducir ancho del menú para minimizar superposición

## 🔗 Casos de Prueba Relacionados
- TC008-NAV: Logo Swag Labs (verificar si tiene problemas similares)
- TC009-NAV: Navegación Back (puede verse afectada)
- Futuros casos de responsive design

## 📈 Frecuencia de Reproducción
- **Reproducible:** Sí
- **Frecuencia:** 100% (siempre ocurre)
- **Intermitente:** No
- **Resoluciones afectadas:** Desktop (por confirmar mobile)
- **Usuarios afectados:** problem_user (verificar con otros usuarios)

## 🏷️ Etiquetas
`navegacion` `menu-lateral` `superposicion` `ux` `visual` `menor` `usabilidad`

## 📋 Criterios de Aceptación para Fix
- [ ] Menú se despliega sin ocultar contenido principal
- [ ] Contenido permanece legible con menú abierto
- [ ] Comportamiento consistente en diferentes resoluciones
- [ ] Animación fluida sin saltos visuales
- [ ] Cumple estándares de UX para menús laterales
- [ ] Testing en múltiples navegadores exitoso

## 🔄 Notas Técnicas
- Posible problema de CSS z-index
- Puede requerir ajustes en responsive design
- Verificar comportamiento en mobile/tablet
- Considerar accesibilidad para usuarios con discapacidades visuales

---

**Reportado por:** Karina Hanmse  
**Última actualización:** 11/09/2025  
**Próxima revisión:** Pendiente desarrollo  
**Prioridad de fix:** Baja (no bloquea funcionalidad crítica)