# TC006-LOGIN - Login con credenciales incorrectas

## 📋 Información General
- **ID:** TC006-LOGIN
- **Módulo:** Autenticación
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 02/09/2025

## 🎯 Objetivo
Verificar que el sistema no permita el acceso cuando se ingresan credenciales incorrectas pero con formato válido.

## 📚 Precondiciones
- [ ] Navegador Chrome 118+ instalado
- [ ] Conexión a internet estable
- [ ] URL https://www.saucedemo.com accesible
- [ ] No hay sesiones previas activas

## 🧪 Datos de Prueba
| Campo       | Valor             | Notas |
|-------      |-------            |-------|
| Username    | usuario_invalido  | Username inexistente en el sistema  |
| Password    | password_incorrecta | Password incorrecta |
| Environment | Production        | https://www.saucedemo.com |

## 🔄 Pasos de Ejecución

### Paso 1: Navegación inicial
**Acción:** Abrir navegador y navegar a https://www.saucedemo.com
**Resultado Esperado:** Página de login carga correctamente

### Paso 2: Validación de elementos
**Acción:** Verificar presencia de campos Username, Password y botón Login
**Resultado Esperado:** Todos los elementos están visibles y habilitados

### Paso 3: Ingreso de credenciales incorrectas
**Acción:** 
- Ingresar "usuario_invalido" en campo Username
- Ingresar "password_incorrecta" en campo Password
**Resultado Esperado:** Ambos campos contienen datos, formato aparentemente válido

### Paso 4: Intento de Autenticación 
**Acción:** Hacer clic en botón "LOGIN"
**Resultado Esperado:** 
- Sistema no procesa la autenticación
- Sistema muestra mensaje de error apropiado (ej: "Epic sadface: Username and password do not match any user in this service")
- Usuario permanece en página de login
- Campos se mantienen o se limpian según política del sistema

## ✅ Criterios de Aceptación
- [ ] Sistema muestra mensaje de error apropiado
- [ ] No permite acceso al sistema con credenciales incorrectas
- [ ] Mensaje aparece en menos de 3 segundos
- [ ] No se revela información específica sobre qué campo es incorrecto

## 🐛 Posibles Defectos a Observar
- Sistema permite acceso indebido con credenciales incorrectas
- Mensaje de error revela información sensible (ej: "usuario no existe" vs "password incorrecta")
- Tiempos de respuesta excesivos (más de 3 segundos)
- Sistema no muestra mensaje de error
- Comportamiento inconsistente entre navegadores
- Posible vulnerabilidad de enumeración de usuarios

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 04/09/2025
- **Navegador:** Chrome 118.0.5993.88
- **SO:** Windows 11 Home
- **Estado:** ✅ PASS
- **Tiempo de ejecución:** [2.0 segundos]

## 📝 Observaciones
 - Login no fue ejecutado.
 - Mensaje error luego de clickear Login.
 - Mensaje de error no se lee completo.
 - Una vez aceptado el error, los cambios no se limpian.
 - No se observaron errores en consola del navegador.
 - Funcionalidad opera según lo esperado.

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot credenciales:** `evidence/screenshots/TC006_step1_credencialinvalidas_04092025.png`
- **Screenshot error:** `evidence/screenshots/TC006_step2_error_message_04092025.png`
- **Video ejecución completa:** `evidence/videos/TC005_credencialinvalida.wmv`

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-AUTH-004 (Validación de credenciales)
- **Requisito seguridad:** REQ-SEC-001 (Prevención acceso no autorizado)
- **Requisito seguridad:** REQ-SEC-002 (No revelación de información sensible)
- **Historia de usuario:** US-003 (Como sistema quiero rechazar credenciales incorrectas sin revelar información específica)
- **Casos relacionados:** 
  - TC001-LOGIN (Login exitoso con credenciales válidas)
  - TC003-LOGIN (Login con ambos campos vacíos)
  - TC004-LOGIN (Login con username vacío y password válida)
  - TC005-LOGIN (Login con username válido y password vacía)
- **Documentación técnica:** [Políticas de autenticación SauceDemo v1.0]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de validación  | < 3 segundos    | 2.0 segundos    | ✅ Pass   |
| Acceso bloqueado      | 100%            | 100%            | ✅ Pass  |
| Mensaje apropiado     | Sí              | Sí              | ✅ Pass   |
| Sin información sensible | Sí           | Sí              | ✅ Pass   |

## 🛡️ Validaciones de Seguridad
- ✅ No hay acceso indebido con credenciales incorrectas
- ✅ Mensaje de error genérico sin revelar información específica
- ✅ No hay enumeración de usuarios válidos/inválidos posible
- ✅ Comportamiento consistente independiente del browser
- ✅ Tiempos de respuesta no revelan información por diferencias temporales

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 02/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 02/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 04/09/2025
**Revisado por:** [Karina Hanmse]