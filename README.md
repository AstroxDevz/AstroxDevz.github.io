# Guía rápida: `*` y `&` en C++

Tabla concisa sobre el uso de `*` y `&` en C++ con ejemplos y explicación breve para cada caso.

---

## Símbolos en C++

| Símbolo | Contexto | Significado | Ejemplo | Explicación |
|---------|----------|------------|---------|------------|
| `*` | Declaración de variable | Declara un **puntero** (variable que guarda una dirección de memoria) | `int* ptr;` | `ptr` puede almacenar la dirección de un `int`. Es una variable cuyo valor es una dirección. |
| `*` | Desreferenciación | Accede al **valor apuntado** por un puntero | `int valor = *ptr;` | Si `ptr` apunta a una dirección con un `int`, `*ptr` obtiene ese valor. |
| `*` | En función (parámetro) | Recibe un **puntero** como argumento | `void funcion(int* p)` | La función recibe la dirección de un `int` y puede modificar el valor apuntado usando `*p`. |
| `*` | En función (retorno) | Devuelve un **puntero** | `int* crearEntero();` | La función devuelve una dirección de memoria que apunta a un `int` (cuidado con la validez del objeto apuntado). |
| `&` | En declaración | Declara una **referencia** (alias de una variable) | `int& ref = valor;` | `ref` es otro nombre para `valor`; no crea copia y no puede reseñar a otro objeto tras la inicialización. |
| `&` | En uso (operador unario) | Obtiene la **dirección** de una variable | `int* ptr = &valor;` | `&valor` devuelve la dirección de `valor`. Es lo contrario de la desreferenciación. |
| `&` | En función (parámetro) | Pasa un valor **por referencia** | `void funcion(int& x)` | La función puede modificar directamente la variable original (sin usar punteros). Sintaxis clara y segura. |
| `&` | En función (retorno) | Devuelve una **referencia** | `int& obtenerRef();` | Devuelve un alias a un objeto existente para poder modificarlo desde el llamador. Evitar devolver referencias a objetos temporales. |

---

### Consejo rápido

- `*` punteros → dirección / indirección  
- `&` referencias → alias  
- `&` operador → obtiene dirección  

> ⚠️ Haz scroll horizontal si estás en móvil
