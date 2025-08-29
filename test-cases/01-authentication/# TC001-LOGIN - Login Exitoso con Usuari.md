# TC001-LOGIN - Login Exitoso con Usuario Estándar

## 📋 Información General
- **ID:** TC001-LOGIN
- **Módulo:** Autenticación
- **Prioridad:** Alta
- **Tipo:** Funcional - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 28/08/2025

## 🎯 Objetivo
Verificar que un usuario válido puede acceder exitosamente al sistema utilizando credenciales correctas.

## 📚 Precondiciones
- [ ] Navegador Chrome 118+ instalado
- [ ] Conexión a internet estable
- [ ] URL https://www.saucedemo.com accesible
- [ ] No hay sesiones previas activas

## 🧪 Datos de Prueba
| Campo       | Valor         | Notas |
|-------      |-------        |-------|
| Username    | standard_user | Usuario válido del sistema |
| Password    | secret_sauce  | Contraseña correcta |
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
- Escribir "standard_user" en campo Username
- Escribir "secret_sauce" en campo Password
**Resultado Esperado:** Texto se muestra correctamente en ambos campos

### Paso 4: Autenticación
**Acción:** Hacer clic en botón "LOGIN"
**Resultado Esperado:** Sistema procesa la autenticación

### Paso 5: Verificación de acceso
**Acción:** Verificar redirección y elementos de página principal
**Resultado Esperado:** 
- URL cambia a `/inventory.html`
- Título "Products" visible
- Menú hamburguesa presente
- Carrito de compras visible
- Lista de productos cargada

## ✅ Criterios de Aceptación
- [ ] Login se completa en menos de 3 segundos
- [ ] No se muestran mensajes de error
- [ ] Todos los elementos de navegación están presentes
- [ ] URL final es la correcta
- [ ] Sesión queda establecida correctamente

## 🐛 Posibles Defectos a Observar
- Campos no aceptan entrada de texto
- Botón LOGIN no responde
- Redirección incorrecta
- Elementos faltantes en página destino
- Tiempos de carga excesivos

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [28/08/2025]
- **Navegador:** Chrome 118.0.5993.88
- **SO:** Windows 11 Home
- **Estado:** ✅ PASS 
- **Tiempo de ejecución:** [2.1 segundos] (Dentro de los parámetros)

## 📝 Observaciones
[- Login ejecutado exitosamente.
 - Todos los elementos se cargaron correctamente.
 - No se observaron errores en consola del navegador.
 - Funcionalidad opera según lo esperado.
]

## 🔗 Referencias
- Requirement: REQ-AUTH-001
- Related Test Cases: TC002, TC003, TC004
- Documentation: [Link a docs]

---
**Última actualización:** 28/08/2025
**Revisado por:** [Karina Hanmse]