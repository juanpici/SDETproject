# SDETproject
Project for SDET works



¿Qué he construido?
He creado un framework de portfolio estilo empresa para demostrar competencias de SDET Lead / Quality Engineering: automatización UI + API, BDD con Cucumber, ejecución por tags, paralelismo, CI, reporting, evidencias, tracing y una capa de contract-lite con validación de JSON Schema.
El objetivo es que cualquier recruiter o tech lead pueda clonar el repo y ver en minutos:

cómo estructuro un framework mantenible,
cómo lo hago observable y “debuggable”,
cómo lo preparo para CI/CD y escalado.


Stack y decisiones
He implementado el framework con:

Java 17 + Maven
Playwright (Java) para UI
Cucumber + JUnit 5 Platform Suite para BDD/runner
RestAssured para API
Allure results para reporting adicional (además de Cucumber HTML/JSON)
Playwright Tracing para análisis profundo de fallos
GitHub Actions para CI
Paralelismo vía configuración oficial de Cucumber


Qué cubre (funcionalmente)
UI (Playwright) — target: the-internet.herokuapp.com
He creado pruebas UI contra un sitio de demo estable:

Form Authentication

Login exitoso (@ui @smoke)
Login fallido (@ui @smoke)


Checkboxes

Toggle de checkbox (@ui @smoke)



API (RestAssured) — target: reqres.in
He creado una suite de API smoke con:

listar usuarios
obtener usuario
usuario no encontrado (404)
login success (200)
login fail (400)

Además, he añadido validación de esquema JSON (contract-lite) en los casos principales.
