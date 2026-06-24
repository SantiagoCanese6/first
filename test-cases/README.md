# 📋 Casos de Prueba - Documentación

Esta carpeta contiene todos los casos de prueba **manuales** documentados. Los casos de prueba describen qué probar, cómo probarlo, y qué esperar.

## 📝 Estructura de un Caso de Prueba

```
ID: TC-001
Título: [Nombre del caso]
Módulo: [Funcionalidad]
Prioridad: [Alta/Media/Baja]
Estado: [Activo/Deshabilitado]

Precondiciones:
- Condiciones necesarias antes de ejecutar la prueba

Pasos:
1. Paso 1
2. Paso 2
3. Paso 3

Resultado Esperado:
- Lo que debería suceder después de cada paso

Notas:
- Información adicional importante
```

## 🌐 Web Testing Cases

Ver: [`web-testing-cases.md`](./web-testing-cases.md)

Ejemplos de casos para:
- Login y autenticación
- Navegación en sitio web
- Formularios y validaciones
- Búsqueda y filtros
- Carrito de compras (si aplica)

## 🔌 API Testing Cases

Ver: [`api-testing-cases.md`](./api-testing-cases.md)

Ejemplos de casos para:
- Endpoints GET/POST/PUT/DELETE
- Validación de respuestas JSON
- Códigos de estado HTTP
- Manejo de errores
- Autenticación y autorización

## 🎯 Cómo Usar Estos Casos

### Para Testing Manual:
1. Lee el caso completo
2. Realiza los pasos en orden
3. Compara resultado con lo esperado
4. Anota si pasó ✅ o falló ❌
5. Si falla, crea un Issue

### Para Testing Automatizado:
1. Usa el caso como referencia
2. Escribe un script automatizado (Python/Selenium/API)
3. Guarda en carpeta `web-testing/` o `api-testing/`
4. Ejecuta con pytest

## 📊 Plantilla General

```markdown
---
ID: TC-XXX
Título: [Descripción clara]
Módulo: [Funcionalidad]
Prioridad: [Alta/Media/Baja]
Estado: [Activo]
Responsable: [Quién lo ejecuta]
Fecha Creación: [YYYY-MM-DD]
---

## Descripción
[Breve descripción del objetivo]

## Precondiciones
- [ ] Precondición 1
- [ ] Precondición 2

## Pasos a Ejecutar
| # | Paso | Esperado |
|---|------|----------|
| 1 | Acción 1 | Resultado 1 |
| 2 | Acción 2 | Resultado 2 |

## Resultado Final
- [ ] El sistema se comporta como se esperaba

## Observaciones
[Cualquier nota adicional]
```

---

💡 **Tip**: Cada caso debe ser independiente. No dependa de otros casos para ejecutarse.