# 🐛 Bug Report - BUG-001

## 📋 Información General
- **ID del Bug:** BUG-001-LOGIN
- **Detectado en:** TC006-LOGIN (Credenciales incorrectas)
- **Módulo:** Autenticación
- **Severidad:** Menor
- **Prioridad:** Media
- **Estado:** Abierto
- **Reportado por:** Karina Hanmse
- **Fecha:** 02/09/2025

## 🎯 Resumen
Los campos Username y Password no se limpian automáticamente después de mostrar mensaje de error por credenciales incorrectas.

## 🔍 Descripción Detallada
Cuando se ingresan credenciales incorrectas y se muestra el mensaje de error, los campos mantienen los datos ingresados previamente. Esto puede generar confusión al usuario y representa un riesgo menor de seguridad.

## 📚 Precondiciones
- Navegador Chrome 118+ 
- URL: https://www.saucedemo.com
- Página de login cargada correctamente

## 🔄 Pasos para Reproducir
1. Navegar a https://www.saucedemo.com
2. Ingresar "usuario_invalido" en campo Username
3. Ingresar "password_incorrecta" en campo Password
4. Hacer clic en botón "LOGIN"
5. Observar mensaje de error
6. **Verificar estado de los campos**

## ✅ Resultado Esperado
- Mensaje de error se muestra correctamente
- **Los campos Username y Password se limpian automáticamente** para nueva entrada
- Usuario puede ingresar credenciales frescas sin borrar manualmente

## ❌ Resultado Actual
- Mensaje de error se muestra correctamente ✅
- **Los campos Username y Password mantienen los datos incorrectos** ❌
- Usuario debe borrar manualmente para reintentar

## 🎯 Impacto
**Experiencia de Usuario:**
- Usuario debe limpiar manualmente los campos
- Puede generar confusión sobre si debe reingresar datos
- Flujo de retry menos intuitivo

**Seguridad (Menor):**
- Datos incorrectos quedan visibles en pantalla
- En equipos compartidos, otros usuarios pueden ver intento previo

## 📊 Datos del Ambiente
- **SO:** Windows 11 Home
- **Navegador:** Chrome 118.0.5993.88
- **Resolución:** 1920x1080
- **URL:** https://www.saucedemo.com
- **Fecha de detección:** 02/09/2025

## 📸 Evidencia
- **Screenshot:** bug-reports/evidence/screenshots/BUG001_campos_no_limpios.png
- **Video Evidencia:** bug-reports/evidence/videos/BUG001_campos_no_limpios.wmv
- **Caso de prueba:** TC006-LOGIN_CREDENCIALESINVALIDAS.md

## 💡 Sugerencia de Solución
Implementar limpieza automática de campos después de mostrar mensaje de error de autenticación fallida, similar al comportamiento estándar de la mayoría de sistemas de login.

## 🔗 Casos de Prueba Relacionados
- TC003-LOGIN: Verificar comportamiento similar
- TC004-LOGIN: Verificar comportamiento similar  
- TC005-LOGIN: Verificar comportamiento similar

## 📈 Frecuencia de Reproducción
- **Reproducible:** Sí
- **Frecuencia:** 100% (siempre ocurre)
- **Intermitente:** No

## 🏷️ Etiquetas
`login` `ux` `campos` `limpieza` `autenticacion` `menor`

---

**Reportado por:** Karina Hanmse  
**Última actualización:** 05/09/2025  
**Próxima revisión:** Pendiente desarrollo