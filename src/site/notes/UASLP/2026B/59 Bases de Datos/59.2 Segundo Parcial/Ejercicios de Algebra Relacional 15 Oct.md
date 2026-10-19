---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/59-2-segundo-parcial/ejercicios-de-algebra-relacional-15-oct/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

## Bloque I. Selección (σ)
1. **Obtener todos los datos de los empleados cuyo salario sea mayor a $15,000**
	σ salario > 15000 (empleado)

2. **Obtener todos los datos de las máquinas cuyo estado sea igual a Operativa**
	∏ estado = 'Operativa' (maquina)

3. **Obtener todos los datos de los productos que pertenezcan a la categoría Electrónica y cuyo costo unitario sea menor a $5,000**
	σ categoria = 'electronica' ∧ costo_unitario < 5000 (producto)

4. **Obtener todos los datos de las órdenes de producción cuya cantidad sea mayor a 500 unidades y cuyo estado sea En proceso**
	σ Cantidad > 500 ∧ estado = 'En proceso' (orden_produccion)

5. **Obtener todos los datos de las máquinas cuyo estado sea Mantenimiento o Fuera de servicio, y que pertenezcan a la planta con identificador 3**
	σ id_palanta = 3 ∧ (estado = 'Mantenimiento' ∨ estado = 'Fuera de servicio')(Maquina)

## Bloque II. Proyección y selección (π, σ)
6. **Obtener únicamente el nombre y el salario de todos los empleados**
	∏ nombre, salario (empleado)

7. **Obtener el nombre del producto y su costo unitario de aquellos productos cuyo costo sea superior a $2,000**
	∏ nombre_producto, costo_unitario (σ costo_unitario > 2000 (producto))

8. **Obtener los diferentes tipos de máquinas registrados en la empresa, sin mostrar valores repetidos**
	∏ tipo (maquina)

9. **Obtener el identificador de la orden, la fecha de inicio y la cantidad de las órdenes de producción cuyo estado sea Finalizada y cuya cantidad sea mayor o igual a 1,000 unidades**
	∏ id_orden, fecha_inicio, cantidad (σ estado = 'Finalizada' ∧ cantidad >= 1000 (orden_produccion))

10. **Obtener el nombre y el puesto de los empleados que trabajen en la planta con identificador 2 y cuyo salario se encuentre entre $12,000 y $25,000, incluyendo ambos límites**
	∏ nombre, puesto (σ id_planta = 2 ∧ salario > 12000 ∧ salario < 25000 (empleado))

## Bloque III. Producto cartesiano (×), selección y proyección
11. **Obtener todas las combinaciones posibles entre los empleados y las máquinas registradas en la empresa, mostrando el nombre del empleado y la descripción de la máquina, independientemente de la planta a la que pertenezcan**
	∏ nombre.empleado, maquina.descripcion (empleado x maquina)

12. **Obtener el nombre de cada empleado y el nombre de la planta a la que pertenece, utilizando el producto cartesiano y una condición que relacione los identificadores de planta**
	∏ nombre, nombre_planta (σ planta.id_planta = empleado.id_planta (empleado x planta))

13. **Obtener la descripción, el tipo y el estado de las máquinas, junto con el nombre de la planta donde se encuentran, considerando únicamente las máquinas cuyo estado sea Operativa**
	∏ descripcion, tipo, estado, nombre_planta(σ estado = 'Operativa' ∧ maquina.id_planta = planta.id_planta (Planta x Maquina))

14. **Obtener el identificador de la orden de producción, el nombre del producto y la cantidad solicitada, considerando únicamente las órdenes cuyo estado sea En proceso y cuya cantidad sea mayor a 300 unidades**
	∏ <sub>id_orden, nombre_producto, cantidad
	(σ estado = 'En proceso' ∧ cantidad > 300 ∧ producto.id_producto = orden_produccion.id_producto</sub> (producto x orden_produccion))

15. **Obtener el nombre del empleado, la descripción de la máquina y las horas trabajadas en cada operación, considerando únicamente las operaciones con más de 8 horas trabajadas. Se deberán relacionar las tres relaciones correspondientes mediante productos cartesianos y condiciones de selección**
	∏ empleado.nombre, maquina, descripcion, operacion.horas_trabajadas
	(σ operacion.id_empleado = empleado.id_empleado ∧ operacion.id_maquina = maquina.id+maquina ∧operacion.horas_trabajadas > 8 (empleado x operacion) x maquina))
## Bloque IV. Reunión natural (⋈), selección y proyección
16. **Obtener el nombre de cada empleado y el nombre de la planta donde trabaja**
	∏ nombre, nombre_planta (empleado ⋈ planta)

17. **Obtener el nombre de los productos, la cantidad solicitada y el estado de sus órdenes de producción, considerando únicamente las órdenes que se encuentren En proceso**
	∏ nombre_producto, cantidad, estado (σ estado = 'En proceso' (producto ⋈ orden_produccion))

18. **Obtener el nombre de cada producto y el nombre de los materiales que se requieren para su fabricación, incluyendo la cantidad requerida de cada material**
	∏ nombre_producto, nombre_material, cantidad_requerida (producto ⋈ producto_material) ⋈ material))

19. **Obtener el nombre de la planta, el nombre del producto, la fecha de inicio y la cantidad solicitada de todas las órdenes de producción cuyo estado sea Finalizada**
	∏ nombre_planta, nombre_producto, fecha_inicio, cantidad 
	(σ estado = 'Finalizada'(orden_produccion ⋈ planta) ⋈ producto))

20. **Obtener el nombre de los empleados y la descripción de las máquinas que han utilizado en operaciones de producción, considerando únicamente las máquinas de tipo CNC y las operaciones con más de 5 horas trabajadas**
	∏ nombre, descripcion, tipo, horas_trabajadas
	(σ tipo = 'CNC' ∧ horas_trabajadas > 5 (empleado ⋈ maquina) ⋈ operacion))

21. **Obtener el nombre de los productos y los nombres de los materiales utilizados para fabricarlos, considerando únicamente los materiales cuyo costo por unidad de medida sea mayor a $500 y cuya cantidad requerida por producto sea superior a 10 unidades de medida**
	∏ nombre_producto, nombre_material 
	(σ costo > 500 ∧ cantidad_requerida >10 (producto ⋈ producto_material) ⋈ material))

22. **Obtener el nombre del empleado, el nombre de la planta, el nombre del producto, la descripción de la máquina y las horas trabajadas de las operaciones asociadas con órdenes de producción Finalizada, considerando únicamente operaciones con más de 6 horas trabajadas**
	∏ nombre, nombre_planta, nombre_producto, descripcion, horas_trabajadas
	(σ  estado = 'Finalizada' ∧ horas_trabajadas > 6 (empleado ⋈ planta) ⋈ orden_produccion) producto) ⋈ operacion)

## Bloque V. Funciones de agregación (𝒢)
23. **Obtener el número total de empleados registrados en cada planta, mostrando el identificador de la planta y la cantidad de empleados**
	id_planta 𝒢 count(id_empleado) (empleado)

24. **Obtener el salario promedio, el salario máximo y el salario mínimo de los empleados, agrupados por puesto**
	puesto 𝒢 avg(salario), min (salario), max(salario) (empleado)

25. **Obtener el identificador de cada producto y la cantidad total de unidades solicitadas en sus órdenes de producción, considerando únicamente las órdenes cuyo estado sea Finalizada**
	id_producto 𝒢 sum(cantidad) (σ estado = 'Finalizado' (orden_produccion))

26. **Obtener el nombre de cada planta y la suma total de las horas trabajadas en las operaciones asociadas con sus órdenes de producción. Para este ejercicio, la planta se determinará a partir de la orden de producción, no de la adscripción del empleado o la máquina**
	nombre_planta 𝒢 sum(horas_trabajadas) (operacion ⋈ orden_produccion) ⋈ planta)