# TC003-LOGIN - Login con campos vacíos.

## 📋 Información General
- **ID:** TC003-LOGIN
- **Módulo:** Autenticación
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 01/09/2025

## 🎯 Objetivo
Verificar que el sistema no permita ingresar con datos incompletos.

## 📚 Precondiciones
- [ ] Navegador Chrome 118+ instalado
- [ ] Conexión a internet estable
- [ ] URL https://www.saucedemo.com accesible
- [ ] No hay sesiones previas activas

## 🧪 Datos de Prueba
| Campo       | Valor         | Notas |
|-------      |-------        |-------|
| Username    | Sin completar | Sin datos  |
| Password    | Sin completar | sin datos |
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
-  Username sin completar
-  Password sin completar
**Resultado Esperado:** Los campos permanecen vacíos, sin validación previa.
### Paso 4: Intento de Autenticación 
**Acción:** Hacer clic en botón "LOGIN"
**Resultado Esperado:** 
- Sistema no procesa la autenticación
- Sistema muestra mensaje de error: "Epic sadface: Username is required"
- Usuario permanece en página de login



## ✅ Criterios de Aceptación
- [ ] Sistema muestra mensaje de error apropiado
- [ ] No permite acceso al sistema.
- [ ] Mensaje aparece en menos de 3 segundos.

## 🐛 Posibles Defectos a Observar
- Sistema permite envío del formulario sin validar campos obligatorios
- Mensaje de error no aparece o es incorrecto
- Sistema muestra mensaje genérico en lugar del específico esperado
- Tiempos de respuesta excesivos (más de 3 segundos)
- Sistema permite acceso indebido con campos vacíos

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [01/09/2025]
- **Navegador:** Chrome 118.0.5993.88
- **SO:** Windows 11 Home
- **Estado:** ✅ PASS 
- **Tiempo de ejecución:** [2.1 segundos] (Dentro de los parámetros)

## 📝 Observaciones
 - Login no fue ejecutado.
 - Mensaje error luego de clickear Login.
 - No se observaron errores en consola del navegador.
 - Funcionalidad opera según lo esperado.

 ## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot credenciales:** `evidence/screenshots/TC003_step3_credencialesvacias_01092025.png`
- **Screenshot error:** `evidence/screenshots/TC003_step7_error_message_01092025.png`
- **Video ejecución completa:** `evidence/videos/TC003_credencialesvacias.wmv`

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-AUTH-003 (Validación de campos obligatorios)
- **Requisito seguridad:** REQ-SEC-001 (Prevención acceso no autorizado)
- **Historia de usuario:** US-001 (Como usuario quiero que el sistema me avise si olvido completar datos obligatorios)
- **Casos relacionados:** 
  - TC001-LOGIN (Login exitoso con credenciales válidas)
  - TC004-LOGIN (Login con solo password vacío)
  - TC005-LOGIN (Login con credenciales incorrectas)
  - TC006-LOGIN (Múltiples intentos fallidos)
- **Documentación técnica:** [Políticas de autenticación SauceDemo v1.0]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de validación  | < 3 segundos    | 2.1 segundos    | ✅ Pass   |
| Acceso bloqueado      | 100%            | 100%            | ✅ Pass   |
| Mensaje específico    | Sí              | Sí              | ✅ Pass   |
| Permanencia en login  | Sí              | Sí              | ✅ Pass   |

## 🛡️ Validaciones de Seguridad
- ✅ No hay bypass de validación de campos obligatorios
- ✅ Mensaje de error apropiado y específico mostrado
- ✅ No hay acceso indebido al sistema con datos faltantes
- ✅ Comportamiento consistente independiente del browser
- ✅ No se procesan credenciales vacías en el backend

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 01/09/2025 | Creación inicial del caso | Karina Hanmse |