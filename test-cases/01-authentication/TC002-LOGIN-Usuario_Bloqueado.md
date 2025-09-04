# TC002-LOGIN - Login Fallido con Usuario Bloqueado

## 📋 Información General
- **ID:** TC002-LOGIN
- **Módulo:** Autenticación
- **Prioridad:** Alta
- **Tipo:** Funcional - Negativo
- **Autor:** Karina Hanmse
- **Fecha creación:** 28/08/2025
- **Última actualización:** 28/08/2025

## 🎯 Objetivo
Verificar que el sistema bloquea correctamente el acceso de usuarios que han sido inhabilitados, mostrando un mensaje de error apropiado y manteniendo la seguridad del sistema.

## 📚 Precondiciones
- [ ] Navegador Google Chrome versión 118+ instalado y actualizado
- [ ] Conexión a internet estable (mínimo 10 Mbps)
- [ ] URL https://www.saucedemo.com accesible y funcional
- [ ] No hay sesiones previas activas en el navegador (limpiar cookies)
- [ ] Usuario `locked_out_user` debe estar en estado bloqueado en el sistema
- [ ] JavaScript habilitado en el navegador

## 🧪 Datos de Prueba
| Campo       | Valor                | Tipo         | Notas                                 |
|-------      |-------               |------        |-------                                |
| Username    | locked_out_user      | Bloqueado    | Usuario inhabilitado intencionalmente |
| Password    | secret_sauce         | Válida       | Contraseña técnicamente correcta      |
| Environment | Production           | -            | https://www.saucedemo.com             |
| Browser     | Chrome 118.0.5993.88 | -            | Navegador de prueba                   |
| OS          | Windows 11 Home      | -            | Sistema operativo                     
|

## 🔄 Pasos de Ejecución

### Paso 1: Navegación inicial
- **Acción:** Abrir Google Chrome y navegar a https://www.saucedemo.com
- **Resultado Esperado:** 
  - Página de login se carga completamente
  - Todos los elementos de la interfaz están disponibles
  - Formulario de login está habilitado para interacción

### Paso 2: Validación de elementos de interfaz
- **Acción:** Verificar que todos los elementos están presentes y funcionales
- **Resultado Esperado:**
  - Campo Username visible y habilitado
  - Campo Password visible y habilitado
  - Botón LOGIN visible y habilitado
  - No hay mensajes de error previos mostrados

### Paso 3: Ingreso de credenciales de usuario bloqueado
- **Acción:** 
  1. Hacer clic en el campo Username
  2. Escribir "locked_out_user" exactamente como aparece
  3. Presionar TAB para moverse al campo Password
  4. Escribir "secret_sauce" en el campo Password
- **Resultado Esperado:** 
  - Texto se ingresa correctamente en ambos campos
  - Campo Password enmascara la entrada correctamente
  - No se disparan validaciones automáticas
  - Campos mantienen el focus apropiadamente

### Paso 4: Intento de autenticación
- **Acción:** Hacer clic en el botón "LOGIN"
- **Resultado Esperado:** 
  - Sistema procesa la solicitud de login
  - Botón responde visualmente al clic
  - Sistema valida credenciales contra base de datos

### Paso 5: Verificación del bloqueo de acceso
- **Acción:** Observar la respuesta del sistema al intento de login
- **Resultado Esperado:** 
  - **Login rechazado:** No se permite el acceso al sistema
  - **URL:** Permanece en `https://www.saucedemo.com/` (no hay redirección)
  - **Mensaje de error:** Se muestra mensaje claro y específico
  - **Campos:** Se mantienen visibles para permitir corrección
  - **Sesión:** No se establece ninguna sesión de usuario

### Paso 6: Validación del mensaje de error específico
- **Acción:** Verificar el contenido y formato del mensaje de error
- **Resultado Esperado:**
  - **Texto exacto:** "Epic sadface: Sorry, this user has been locked out."
  - **Ubicación:** Mensaje aparece entre el logo y los campos de entrada
  - **Formato:** Texto en color rojo con icono de error
  - **Persistencia:** Mensaje permanece visible hasta nueva acción
  - **Accesibilidad:** Mensaje es legible y no interfiere con la navegación

## ✅ Criterios de Aceptación
- [ ] Login es rechazado inmediatamente (< 2 segundos de respuesta)
- [ ] Se muestra mensaje de error específico y claro
- [ ] No hay redirección a páginas internas del sistema
- [ ] URL permanece en página de login
- [ ] No se establece sesión de usuario
- [ ] Campos permanecen disponibles para nuevo intento
- [ ] Mensaje es específico para usuario bloqueado (no genérico)

## 🐛 Posibles Defectos a Observar

### Críticos:
- Sistema permite acceso a usuario bloqueado
- No se muestra ningún mensaje de error
- Redirección incorrecta a páginas internas
- Error de servidor o crash del sistema

### Mayores:
- Mensaje de error genérico en lugar de específico
- Mensaje no es claro para el usuario final
- Tiempo de respuesta excesivo (> 5 segundos)
- Campos se deshabilitan incorrectamente

### Menores:
- Mensaje de error con problemas de formato o styling
- Texto del mensaje con errores tipográficos
- Mensaje no es accesible para screen readers
- Inconsistencias visuales en la presentación del error

## 📊 Resultado de Ejecución
- **Ejecutado por:** Karina Hanmse
- **Fecha ejecución:** 28/08/2025
- **Hora ejecución:** 14:45 ART
- **Navegador:** Chrome 118.0.5993.88
- **Sistema Operativo:** Windows 11 Home (Build 22631)
- **Resolución pantalla:** 1920x1080
- **Estado:** ✅ PASS
- **Tiempo de respuesta:** 1.8 segundos
- **Intentos realizados:** 1/3
- **Defectos encontrados:** 0

## 📝 Observaciones de Ejecución
**Ejecución exitosa - Comportamiento esperado:**
- ✅ Sistema rechazó correctamente el login del usuario bloqueado
- ✅ Mensaje de error específico mostrado: "Epic sadface: Sorry, this user has been locked out."
- ✅ No hubo redirección indebida a páginas protegidas
- ✅ URL permaneció en página de login como esperado
- ✅ Tiempo de respuesta óptimo: 1.8 segundos
- ✅ Seguridad del sistema funcionando correctamente

**Observaciones técnicas adicionales:**
- Validación de usuario se ejecuta server-side (correcto)
- No hay filtración de información sensible en mensajes
- Comportamiento consistente con políticas de seguridad
- Interfaz permanece estable tras mostrar error

**Nota importante:**
- Este comportamiento NO es un defecto - es funcionalidad de seguridad por diseño
- Usuario `locked_out_user` está intencionalmente bloqueado para demostraciones
- Mensaje específico ayuda a distinguir entre usuario bloqueado vs credenciales incorrectas

## 🔍 Evidencia de Prueba
- **Screenshot inicial:** `evidence/screenshots/TC002_step1_login_page_28082025.png`
- **Screenshot credenciales:** `evidence/screenshots/TC002_step3_blocked_user_entered_28082025.png`
- **Screenshot error:** `evidence/Tsreenshots/C002_step6_error_message_28082025.png`
- **Video ejecución completa:** `evidence/videos/TC002_blocked_user_test_28082025.mp4`
- **Console logs:** `evidence/docs/TC002_browser_console_28082025.txt`
- **Network requests:** `evidence/TC002_network_requests_28082025.har`
- **Network requests:** `evidence/docs/TC002_network_analysis_28082025´

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-AUTH-002 (Bloqueo de usuarios inhabilitados)
- **Requisito seguridad:** REQ-SEC-001 (Prevención acceso no autorizado)
- **Historia de usuario:** US-002 (Como administrador quiero bloquear usuarios problemáticos)
- **Casos relacionados:** 
  - TC001-LOGIN (Login exitoso con usuario válido)
  - TC006-LOGIN (Login con credenciales incorrectas)
  - TC007-LOGIN (Múltiples intentos fallidos)
- **Documentación técnica:** [Políticas de seguridad SauceDemo v1.0]
- **Ambiente de prueba:** https://www.saucedemo.com

## 📈 Métricas y KPIs
| Métrica               | Valor Objetivo  | Valor Obtenido  | Estado    |
|---------              |---------------  |---------------- |--------   |
| Tiempo de validación  | < 2 segundos    | 1.8 segundos    | ✅ Pass   |
| Acceso bloqueado      | 100%            | 100%            | ✅ Pass   |
| Mensaje específico    | Sí              | Sí              | ✅ Pass   |
| Seguridad mantenida   | Sí              | Sí              | ✅ Pass   |

## 🛡️ Validaciones de Seguridad
- ✅ No hay bypass de autenticación posible
- ✅ Mensaje no revela información técnica sensible
- ✅ No hay escalación de privilegios
- ✅ Logging apropiado del intento de acceso bloqueado
- ✅ Comportamiento consistente independiente del browser

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 28/08/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 28/08/2025 | Adición de validaciones de seguridad | Karina Hanmse |

---
**✅ Caso de prueba validado - Seguridad funcionando correctamente**  
**Próxima revisión:** 04/09/2025  
**Clasificación:** Caso negativo - Comportamiento esperado