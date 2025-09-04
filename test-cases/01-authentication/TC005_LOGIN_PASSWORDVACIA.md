# TC005-LOGIN - Login con username válido y password vacía

## 📋 Información General
- **ID:** TC005-LOGIN
- **Módulo:** Autenticación
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 03/09/2025

## 🎯 Objetivo
Verificar que el sistema no permita ingresar cuando el campo password está vacío, aún teniendo un username válido.

## 📚 Precondiciones
- [ ] Navegador Chrome 118+ instalado
- [ ] Conexión a internet estable
- [ ] URL https://www.saucedemo.com accesible
- [ ] No hay sesiones previas activas

## 🧪 Datos de Prueba
| Campo       | Valor         | Notas |
|-------      |-------        |-------|
| Username    | standard_user | Username válido del sistema  |
| Password    | Sin completar | Campo vacío |
| Environment | Production    | https://www.saucedemo.com |

## 🔄 Pasos de Ejecución

### Paso 1: Navegación inicial
**Acción:** Abrir navegador y navegar a https://www.saucedemo.com
**Resultado Esperado:** Página de login carga correctamente

### Paso 2: Validación de elementos
**Acción:** Verificar presencia de campos Username, Password y botón Login
**Resultado Esperado:** Todos los elementos están visibles y habilitados

### Paso 3: Ingreso de credenciales
**Acción:** 
- Ingresar "standard_user" en campo Username
- Dejar vacío campo Password
**Resultado Esperado:** Solo el campo Username contiene datos, Password permanece vacío

### Paso 4: Intento de Autenticación 
**Acción:** Hacer clic en botón "LOGIN"
**Resultado Esperado:** 
- Sistema no procesa la autenticación
- Sistema muestra mensaje de error: "Epic sadface: Password is required"
- Usuario permanece en página de login
- Campo Username mantiene el valor ingresado

## ✅ Criterios de Aceptación
- [ ] Sistema muestra mensaje de error apropiado
- [ ] No permite acceso al sistema
- [ ] Mensaje aparece en menos de 3 segundos
- [ ] Username ingresado se mantiene visible tras el error

## 🐛 Posibles Defectos a Observar
- Sistema permite envío del formulario sin validar campo password obligatorio
- Mensaje de error no aparece o es incorrecto
- Sistema muestra mensaje genérico en lugar del específico esperado
- Campo username se limpia incorrectamente tras el error
- Tiempos de respuesta excesivos (más de 3 segundos)
- Sistema permite acceso indebido con password vacía

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [02/09/2025]
- **Navegador:** Chrome 118.0.5993.88
- **SO:** Windows 11 Home
- **Estado:** ✅ PASS 
- **Tiempo de ejecución:** [2.1 segundos]

## 📝 Observaciones
 - Login no fue ejecutado.
 - Mensaje error luego de clickear Login.
 - No se observaron errores en consola del navegador.
 - Funcionalidad opera según lo esperado.

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot credenciales:** `evidence/screenshots/TC005_step1_credencialpasswordvacia_04092025.png`
- **Screenshot error:** `evidence/screenshots/TC005_step2_error_message_04092025.png`
- **Video ejecución completa:** `evidence/videos/TC005_credencialpasswordvacia.wmv`

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-AUTH-003 (Validación de campos obligatorios)
- **Requisito seguridad:** REQ-SEC-001 (Prevención acceso no autorizado)
- **Historia de usuario:** US-001 (Como usuario quiero que el sistema me avise si olvido completar datos obligatorios)
- **Casos relacionados:** 
  - TC001-LOGIN (Login exitoso con credenciales válidas)
  - TC003-LOGIN (Login con ambos campos vacíos)
  - TC004-LOGIN (Login con username vacío y password válida)
  - TC006-LOGIN (Login con credenciales incorrectas)
- **Documentación técnica:** [Políticas de autenticación SauceDemo v1.0]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de validación  | < 3 segundos    | [2.1 segundos]  | ✅ Pass   |
| Acceso bloqueado      | 100%            | 100%            | ✅ Pass   |
| Mensaje específico    | Sí              | Sí              | ✅ Pass   |
| Permanencia en login  | Sí              | Sí/No           | ✅ Pass   |

## 🛡️ Validaciones de Seguridad
- ✅ No hay bypass de validación de campo password obligatorio
- ✅ Mensaje de error apropiado y específico mostrado
- ✅ No hay acceso indebido al sistema con password faltante
- ✅ Comportamiento consistente independiente del browser
- ✅ Username ingresado no se procesa sin password válida

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 02/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 04/09/2025 | Ejecución del caso | Karina Hanmse |


---
**Última actualización:** 04/09/2025
**Revisado por:** [Karina Hanmse]