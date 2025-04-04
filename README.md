# 🧾 Glosario de Excepciones HTTP (NestJS)

---

## 🔴 `BadRequestException (400)`
**Cuándo usar:**  
Cuando el cliente envía datos inválidos, incompletos o que no tienen sentido.

**Ejemplos:**
- Faltan campos obligatorios
- Formato de UUID incorrecto
- Intentar desasociar un objetivo que no existe

---

## 🔐 `UnauthorizedException (401)`
**Cuándo usar:**  
Cuando el usuario **no está autenticado** (falta el token o no es válido).

**Ejemplos:**
- No se envió el token
- Token inválido o expirado

---

## 🚫 `ForbiddenException (403)`
**Cuándo usar:**  
Cuando el usuario **está autenticado pero no tiene permiso** para realizar la acción.

**Ejemplos:**
- Modificar una evaluación que no le pertenece
- Desactivar una evaluación que aún tiene un objetivo asociado

---

## ❓ `NotFoundException (404)`
**Cuándo usar:**  
Cuando el recurso solicitado **no existe**.

**Ejemplos:**
- Evaluación no encontrada por ID
- Usuario no registrado

---

## ⚠️ `ConflictException (409)`
**Cuándo usar:**  
Cuando hay un **conflicto con el estado actual** del recurso.

**Ejemplos:**
- Ya existe una evaluación con ese título
- Registro duplicado por clave única

---

## 💥 `InternalServerErrorException (500)`
**Cuándo usar:**  
Cuando ocurre un error **inesperado en el servidor**.

**Ejemplos:**
- Error en la base de datos
- Lógica no controlada que lanza una excepción

---

## 🛑 `ServiceUnavailableException (503)`
**Cuándo usar:**  
Cuando el servicio está **temporalmente no disponible**.

**Ejemplos:**
- Servicio externo caído o sin respuesta
- Sistema en mantenimiento
