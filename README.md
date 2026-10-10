# ⚡ API Harry Potter 

<p align="center">
  <img src="https://img.shields.io/badge/Universe-Harry%20Potter-740001?style=for-the-badge" alt="Harry Potter" />
  <img src="https://img.shields.io/badge/Data-JSON-3776AB?style=for-the-badge" alt="JSON" />
  <img src="https://img.shields.io/badge/Status-In%20Development-orange?style=for-the-badge" alt="Project Status" />
</p>

<p align="center">
  API de personajes inspirada en el universo mágico de Harry Potter.
</p>

---

## Descripción

**Harry Potter API** es un proyecto que organiza información de personajes del universo creado por J. K. Rowling, incluyendo estudiantes de Hogwarts, profesores, magos y otras criaturas mágicas.

El proyecto utiliza una estructura de datos JSON para almacenar y consultar información de los personajes, facilitando su integración con aplicaciones web y otros proyectos de software.

Cada personaje contiene información como nombre, actor, casa de Hogwarts, especie, patronus, ascendencia e imagen de referencia.

## Características

- Catálogo de personajes del universo de Harry Potter.
- Información sobre las casas de Hogwarts.
- Datos sobre especies, patronus y ascendencia.
- Información de los actores que interpretan a los personajes.
- URLs de imágenes de referencia.
- Datos organizados en formato JSON.
- Posibilidad de integración con aplicaciones frontend y backend.

## Personajes incluidos

El catálogo inicial contiene 30 personajes, entre ellos:

| ID | Personaje | Casa |
|---:|---|---|
| 1 | Harry Potter | Gryffindor |
| 2 | Hermione Granger | Gryffindor |
| 3 | Ron Weasley | Gryffindor |
| 4 | Draco Malfoy | Slytherin |
| 5 | Albus Dumbledore | Gryffindor |
| 6 | Severus Snape | Slytherin |
| 7 | Lord Voldemort | Slytherin |
| 8 | Rubeus Hagrid | Gryffindor |
| 9 | Minerva McGonagall | Gryffindor |
| 10 | Luna Lovegood | Ravenclaw |

El catálogo también incluye personajes como Neville Longbottom, Ginny Weasley, Sirius Black, Remus Lupin, Bellatrix Lestrange, Dobby, Cedric Diggory y muchos más.

## Tecnologías

- **JSON:** almacenamiento y organización de los datos.
- **Node.js:** entorno de ejecución para el backend, si se utiliza Express.
- **Express:** framework para construir las rutas HTTP, si está configurado en el proyecto.

> Las tecnologías del servidor deben ajustarse a la implementación real del repositorio.

## Estructura de los datos

Cada personaje puede incluir los siguientes campos:

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | Number | Identificador único. |
| `name` | String | Nombre del personaje. |
| `actor` | String o null | Actor que lo interpreta. |
| `house` | String o null | Casa de Hogwarts. |
| `species` | String | Especie o naturaleza del personaje. |
| `patronus` | String o null | Patronus conocido. |
| `hogwartsStudent` | Boolean | Indica si es estudiante de Hogwarts. |
| `hogwartsStaff` | Boolean | Indica si pertenece al personal de Hogwarts. |
| `ancestry` | String o null | Ascendencia mágica. |
| `image_url` | String | URL de imagen. |
| `firstAppearance` | String | Primera aparición documentada en el catálogo. |

## Ejemplo de datos JSON

```json
{
  "Harry Potter": [
    {
      "id": 1,
      "name": "Harry Potter",
      "actor": "Daniel Radcliffe",
      "house": "Gryffindor",
      "species": "Human",
      "patronus": "Stag",
      "hogwartsStudent": true,
      "hogwartsStaff": false,
      "ancestry": "Half-blood",
      "image_url": "https://ik.imagekit.io/hpapi/harry.jpg",
      "firstAppearance": "Harry Potter and the Philosopher's Stone (1997)"
    }
  ]
}
```

## Instalación

Clona el repositorio y entra en su directorio:

```bash
git clone URL_DE_TU_REPOSITORIO
cd NOMBRE_DE_TU_PROYECTO
```

Si el proyecto utiliza Node.js y Express, instala las dependencias:

```bash
npm install
```

Inicia el servidor con el comando configurado en `package.json`. Por ejemplo, si existe un script llamado `start`:

```bash
npm start
```

**Nota:** estos comandos presuponen que el proyecto está configurado con Node.js. Si solamente contiene el archivo JSON, no necesitas instalar Express para consultar los datos localmente.

## Endpoints

Si el backend está implementado con las rutas sugeridas, puedes documentar los siguientes endpoints:

| Método | Endpoint | Descripción |
|---|---|---|
| GET | `/api/personajes` | Obtiene todos los personajes. |
| GET | `/api/personajes/:id` | Obtiene un personaje por su identificador. |

Ejemplo de solicitud:

```http
GET /api/personajes/1
```

Ejemplo de respuesta:

```json
{
  "id": 1,
  "name": "Harry Potter",
  "actor": "Daniel Radcliffe",
  "house": "Gryffindor",
  "species": "Human",
  "patronus": "Stag"
}
```

Los endpoints anteriores corresponden a una implementación propuesta con Express; no estarán disponibles hasta que se creen las rutas en el servidor.

## Pruebas

Puedes utilizar herramientas como Postman, Insomnia o `curl` para comprobar las respuestas HTTP una vez que el servidor esté en ejecución.

Ejemplo:

```bash
curl http://localhost:3000/api/personajes
```

Ajusta el puerto y la URL según la configuración de tu aplicación.

## Mejoras futuras

- [ ] Incorporar filtros por casa de Hogwarts.
- [ ] Buscar personajes por nombre.
- [ ] Consultar personajes por identificador.
- [ ] Añadir paginación.
- [ ] Implementar validaciones y manejo de errores.
- [ ] Documentar la API con Swagger/OpenAPI.
- [ ] Publicar la API para que otros desarrolladores puedan consumirla.

## Aviso legal

Este es un proyecto independiente con fines educativos y de práctica de desarrollo de software. No está afiliado, patrocinado ni respaldado oficialmente por Warner Bros., J. K. Rowling ni los titulares de los derechos de Harry Potter.

Los nombres, personajes y elementos relacionados pertenecen a sus respectivos titulares. Las imágenes enlazadas pueden estar sujetas a derechos de autor y pertenecen a sus respectivas fuentes.

---

<p align="center">
  Desarrollado con fines de aprendizaje y práctica de desarrollo de software.
</p>
