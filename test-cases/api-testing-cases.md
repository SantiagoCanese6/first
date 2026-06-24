# 🔌 Casos de Prueba - API Testing

Casos de prueba para APIs REST. Estos casos pueden ejecutarse manualmente con herramientas como Postman o automáticamente con scripts Python.

---

## TC-API-001: GET - Obtener Lista de Usuarios

**Endpoint**: `GET /api/users`  
**Prioridad**: ⭐⭐⭐ Alta  
**Tipo**: Funcional

### Precondiciones
- La API está en funcionamiento
- El servidor es accesible en `http://localhost:3000` (ajusta según tu entorno)
- Tienes un token de autenticación válido (si es requerido)

### Headers
```
Authorization: Bearer <token>
Content-Type: application/json
```

### Pasos
1. Envía una solicitud GET a `/api/users`
2. Espera la respuesta
3. Verifica el código de estado

### Respuesta Esperada
```
Status: 200 OK

{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Juan",
      "email": "juan@example.com",
      "created_at": "2024-01-15T10:30:00Z"
    },
    {
      "id": 2,
      "name": "María",
      "email": "maria@example.com",
      "created_at": "2024-01-16T11:20:00Z"
    }
  ],
  "total": 2
}
```

### Validaciones
✅ Status code es 200  
✅ Response tiene estructura JSON válida  
✅ Array `data` contiene al menos 1 usuario  
✅ Cada usuario tiene: id, name, email, created_at  
✅ Respuesta se recibe en menos de 500ms

### Resultado Actual
[ ] Pasó  [ ] Falló

---

## TC-API-002: POST - Crear Nuevo Usuario

**Endpoint**: `POST /api/users`  
**Prioridad**: ⭐⭐⭐ Alta  
**Tipo**: Funcional

### Precondiciones
- La API está disponible
- Tienes credenciales de autenticación
- El email a usar no existe en el sistema

### Headers
```
Authorization: Bearer <token>
Content-Type: application/json
```

### Request Body
```json
{
  "name": "Carlos López",
  "email": "carlos.lopez@example.com",
  "password": "SecurePass123!",
  "role": "user"
}
```

### Pasos
1. Envía POST request con los datos del usuario
2. Espera la respuesta
3. Verifica que se creó correctamente

### Respuesta Esperada
```
Status: 201 Created

{
  "success": true,
  "message": "Usuario creado exitosamente",
  "data": {
    "id": 3,
    "name": "Carlos López",
    "email": "carlos.lopez@example.com",
    "role": "user",
    "created_at": "2024-01-20T14:30:00Z"
  }
}
```

### Validaciones
✅ Status code es 201 Created  
✅ El usuario se devuelve con un ID generado  
✅ El email del usuario coincide con el enviado  
✅ created_at es una fecha válida  
✅ No se devuelve la contraseña en la respuesta

### Resultado Actual
[ ] Pasó  [ ] Falló

---

**Nota**: Reemplaza `http://localhost:3000` con la URL real de tu API.