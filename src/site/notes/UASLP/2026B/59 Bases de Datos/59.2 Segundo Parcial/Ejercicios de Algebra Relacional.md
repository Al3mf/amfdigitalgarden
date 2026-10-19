---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/59-2-segundo-parcial/ejercicios-de-algebra-relacional/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---


sala(id_sala, piso, capacidad)
pelicula(id_pelicula, titulo, genero)
proyeccion(id_sala, id_pelicula, horario, fecha_inicio, fecha_fin)

1. La relacion sala almacena la informacion de todas las salas cinematograficas del cine, el piso en el que se encuentran y su capacidad
2. La relacion pelicula almacena los datos de las peliculas que se proyectan en el cine
3. La relacion oroyeccion almacena la relacion que hay entre las salas y las peliculas, asi como el horario en el que se proyecta la pelicula y el periodo en que esta se proyecta en la sala

Ejercicios"
1. Obtener los titulos de las peliculas proyectadas durante enero del año 2023
	∏ <sub>titulo (σ fecha_inicio ≥ "01/01/23" ∧ fecha_fin ≤ "31/01/23"</sub> (pelicula ⋈ proyeccion)

2. Obtener las salas en las que se ha proyectado la misma pelicula del genero de ciencia ficcion tanto en el horario de las 16:00 horas, como en el horario de las 19:00 horas
	∏ <sub>id_sala (σ genero = "Ciencia Ficcion" ∧ (horario = "16:00" ∨ horario = "19:00")</sub> 
	(proyeccion ⋈ pelicula))

3. Obtener las salas que solo se proyectan peliculas cuyo genero sea drama
	∏ <sub>id_sala (σ genero = 'Drama'</sub> (pelicula ⋈ proyeccion))

4. Obtener las salas con capacidad superior a 250 personas y que proyectan peliculas en el horario de las 13:00 horas
	∏ <sub>id_sala (σ capacidad > 250 ∧ horario = '13:00'</sub> (sala ⋈ proyeccion))

5. Obtener unicamente el titulo de las peliculas del genero de comedia
	∏ <sub>titulo (σ genero = 'Comedia'</sub> (pelicula))

6. Obtener una lista de todos los detalles de las proyecciones, que incluya el nombre de la pelicula, el genero y la sala donde se proyecta, sin repetir las peliculas ni salas
	∏ <sub>titulo, genero, sala.id_sala (σ pelicula.id_pelicula = proyeccion.id_pelucula ∧ sala.id_sala = proyeccion.id_sala</sub> (proyeccion ⋈ sala ⋈ pelicula))

7. Obtener la lista de todas las proyecciones, incluyendo todas las proyecciones, incluyendo aquellas que no tienen una sala correspondiente en la taba de sala (por ejemplo, si una proyeccion esta registrada pero no se le ha asignado una sala)
	proyeccion ⋈ <sub>proyeccion.id_sala = sala.id_sala</sub>  (sala)

8. Obtener la lista de todas las proyecicones, incluyendo todas las proyecciones, incluso aquellas que no tienen una sala correspondiente en la tabla de la sala (por eemplo, si una proyeccion mesta registrada pero no se le ha asignado una sala)

9. Obtener todas las peliculas que se proyectan, incluso aquellas que no estan asociadas con ninguna proyeccion en la tabla proyeccion
	∏ <sub>titulo</sub> (pelicula)


