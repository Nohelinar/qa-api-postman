# 🧪 Proyecto de API Testing – Gestión de Usuarios con GoRest API

Este proyecto muestra mi capacidad como QA para diseñar, ejecutar y automatizar pruebas funcionales sobre una API REST pública, documentando cada paso y generando reportes claros.

---

## 🎯 Objetivo del proyecto

- Validar operaciones CRUD sobre la API de usuarios de GoRest.
- Documentar y automatizar los tests con Postman + Newman.
- Simular errores comunes y reportarlos.
- Integrar con Notion vía API para visualización de resultados.

---

## 🛠️ Herramientas utilizadas

- Postman  
- Newman  
- Notion API  
- GitHub  

---

## 🗂️ Estructura del proyecto

```
qa-api-postman/
├── collections/
├── environments/
├── tests/
├── notion_integration/
└── README.md
```

---

## 📌 Endpoints y casos de prueba

- `GET /users` → obtener lista de usuarios
- `GET /users/{id}` → obtener un usuario específico
- `POST /users` → crear un usuario
- `PUT /users/{id}` → actualizar usuario
- `DELETE /users/{id}` → eliminar usuario

Casos negativos:
- Crear sin token
- Email duplicado
- ID inválido

---

## ▶️ ¿Cómo ejecutar los tests manuales?

1. Abrí Postman
2. Importá la colección y el ambiente desde la carpeta `/collections` y `/environments`
3. Ejecutá los endpoints manualmente

---

## 🔁 ¿Cómo ejecutar la automatización con Newman?

```bash
newman run collections/gorest_users_collection.json \
  -e environments/gorest_env.json \
  -r cli,html --reporter-html-export tests/newman-report.html
```
El reporte se guarda en /tests/newman-report.html

## 📊 Integración con Notion

Visualización de resultados de test vía API
Dashboard con test, fecha, estado, error, etc.

## 🐞 Bugs simulados reportados
Se permite crear usuario sin email válido
GET con ID inválido no devuelve 404
(Capturas incluidas en carpeta /bugs)

## 💡 Aprendizajes
Cobertura de pruebas para una API pública
Uso de Postman + Newman + automatización
Documentación clara para equipos técnicos


