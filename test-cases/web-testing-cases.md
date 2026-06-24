# 🌐 Casos de Prueba - Web Testing

Casos de prueba para aplicaciones web. Estos casos pueden usarse para testing manual o como referencia para automatización.

---

## TC-WEB-001: Login con Credenciales Válidas

**Módulo**: Autenticación  
**Prioridad**: ⭐⭐⭐ Alta  
**Tipo**: Funcional

### Precondiciones
- El navegador está abierto
- Estás en la página de login
- Tienes credenciales de usuario válidas (usuario: `test@example.com`, contraseña: `Test123!`)

### Pasos
1. Navega a la página de login
2. Ingresa el email: `test@example.com`
3. Ingresa la contraseña: `Test123!`
4. Haz clic en el botón "Iniciar Sesión"
5. Espera 3 segundos a que cargue

### Resultado Esperado
✅ Deberías ser redirigido al dashboard  
✅ Tu nombre de usuario debe aparecer en la esquina superior derecha  
✅ Los elementos del menú principal deben ser visibles  

### Resultado Actual
[ ] Pasó  [ ] Falló

### Notas
- El sistema debe guardar la sesión en cookies
- No debe mostrar errores en la consola

---

## TC-WEB-002: Login con Contraseña Incorrecta

**Módulo**: Autenticación  
**Prioridad**: ⭐⭐⭐ Alta  
**Tipo**: Negativo

### Precondiciones
- El navegador está abierto
- Estás en la página de login
- Tienes un usuario válido pero contraseña incorrecta

### Pasos
1. Navega a la página de login
2. Ingresa el email: `test@example.com`
3. Ingresa la contraseña: `WrongPassword123`
4. Haz clic en "Iniciar Sesión"

### Resultado Esperado
❌ El login FALLA  
❌ Ves un mensaje de error: "Credenciales inválidas"  
❌ Permaneces en la página de login  
❌ El campo de contraseña se limpia

### Resultado Actual
[ ] Pasó  [ ] Falló

### Notas
- El error debe mostrarse en rojo
- No se debe procesar la solicitud al servidor si falta algún campo

---

## TC-WEB-003: Navegación por Menú Principal

**Módulo**: Navegación  
**Prioridad**: ⭐⭐ Media  
**Tipo**: Funcional

### Precondiciones
- Estás logueado en la aplicación
- El menú principal es visible

### Pasos
1. Haz clic en "Home" en el menú
2. Verifica que cargue el inicio
3. Haz clic en "Productos"
4. Verifica que aparezca la lista de productos
5. Haz clic en "Contacto"
6. Verifica que aparezca el formulario de contacto

### Resultado Esperado
✅ Cada sección carga correctamente  
✅ La URL cambia según corresponda  
✅ No hay errores 404  
✅ El contenido se carga en menos de 2 segundos

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-WEB-004: Completar Formulario de Registro

**Módulo**: Registro  
**Prioridad**: ⭐⭐⭐ Alta  
**Tipo**: Funcional

### Precondiciones
- Estás en la página de registro
- Tiene acceso a un email válido

### Pasos
1. Ingresa el nombre: `Juan Pérez`
2. Ingresa el email: `juan.perez@example.com`
3. Ingresa la contraseña: `SecurePass123!`
4. Confirma la contraseña: `SecurePass123!`
5. Marca la casilla "Acepto términos y condiciones"
6. Haz clic en "Registrarse"

### Resultado Esperado
✅ Se muestra mensaje: "Registro exitoso"  
✅ Recibes un email de confirmación  
✅ Eres redirigido a la página de login  
✅ Puedes loguearte con las nuevas credenciales

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-WEB-005: Validación de Campo Email

**Módulo**: Validación de Formularios  
**Prioridad**: ⭐⭐ Media  
**Tipo**: Negativo

### Precondiciones
- Estás en un formulario con campo de email
- El campo está vacío o con valor anterior

### Pasos
1. Intenta ingresar: `emailsinformato`
2. Presiona Tab o haz clic fuera del campo
3. Verifica si aparece error

### Resultado Esperado
❌ El campo muestra error: "Email inválido"  
❌ El campo se resalta en rojo  
❌ No puedes enviar el formulario  

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-WEB-006: Búsqueda de Productos

**Módulo**: Búsqueda  
**Prioridad**: ⭐⭐ Media  
**Tipo**: Funcional

### Precondiciones
- Estás en la página de productos
- Existe la barra de búsqueda

### Pasos
1. Haz clic en la barra de búsqueda
2. Ingresa: `laptop`
3. Presiona Enter
4. Espera los resultados

### Resultado Esperado
✅ Se muestran solo productos que contengan "laptop"  
✅ Los resultados aparecen en menos de 2 segundos  
✅ Aparece el número de resultados encontrados  
✅ Puedes ordenar y filtrar los resultados

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-WEB-007: Responsive - Vista Móvil

**Módulo**: Diseño Responsivo  
**Prioridad**: ⭐⭐ Media  
**Tipo**: No-Funcional

### Precondiciones
- Abre las DevTools (F12)
- Selecciona dispositivo móvil (iPhone 12)

### Pasos
1. Abre la página principal
2. Verifica que el menú se colapse en hamburguesa
3. Haz clic en el menú hamburguesa
4. Verifica que se despliegue correctamente
5. Navega por diferentes secciones

### Resultado Esperado
✅ El diseño se adapta correctamente  
✅ No hay elementos fuera de pantalla  
✅ Los botones son clickeables  
✅ Las imágenes se ven proporcionadas

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-WEB-008: Logout

**Módulo**: Sesión  
**Prioridad**: ⭐⭐ Media  
**Tipo**: Funcional

### Precondiciones
- Estás logueado en la aplicación
- Visible tu perfil o menú de usuario

### Pasos
1. Haz clic en tu nombre de usuario (esquina superior derecha)
2. Selecciona "Cerrar Sesión"
3. Confirma la acción si se pide

### Resultado Esperado
✅ Tu sesión se cierra  
✅ Eres redirigido a la página de login  
✅ Las cookies de sesión se eliminan  
✅ Si haces back en el navegador, no vuelves al dashboard

### Resultado Actual
[ ] Pasó  [ ] Falló

---

**Nota**: Estos son ejemplos. Adapta los casos según tu aplicación específica.