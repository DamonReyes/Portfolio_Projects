# Views for Visualization 
### Skills tecnicos en este proyecto: SQL, Excel, Tableau

## Table of contents
1. [pre processing](#introduction)
2. [Visualization](#paragraph1)

vamos a prepara unas visualizaciones desde PostgreSQL <a name="introduction"></a>
```sql
--- lets create a top 10 most rented movies
select peliculas.pelicula_id as id, peliculas.titulo, count(*) as numero_rentas
from rentas
	inner join inventarios on
		rentas.inventario_id = inventarios.inventario_id
	inner join peliculas on
		peliculas.pelicula_id = inventarios.pelicula_id
group by
	peliculas.pelicula_id,
	peliculas.titulo
order by
	numero_rentas desc
limit 10;

--- now i goin to make a tipe of change
select peliculas.pelicula_id, tipos_cambio.tipo_cambio_id, 
	tipos_cambio.cambio_usd * peliculas.precio_renta as precio_mxn
from peliculas, tipos_cambio
where tipos_cambio.codigo = 'MXN'

--- lets check the sales per city
select ciudades.ciudad_id, ciudades.ciudad, count(*) as rents_per_city
from ciudades
	inner join direcciones on ciudades.ciudad_id = direcciones.ciudad_id
	inner join tiendas on tiendas.direccion_id = direcciones.direccion_id
	inner join inventarios on inventarios.tienda_id = tiendas.tienda_id
	inner join rentas on inventarios.inventario_id = rentas.inventario_id
group by ciudades.ciudad_id;

--- create a view of sales over time
select date_part('year', rentas.fecha_renta) as anio,
		date_part('month', rentas.fecha_renta) as mes,
		peliculas.titulo, 
		count(*) as numero_rentas
from rentas
	inner join inventarios on rentas.inventario_id = inventarios.inventario_id
	inner join peliculas on peliculas.pelicula_id = inventarios.pelicula_id
group by anio, mes
------------------------------------------------------------------------------
select date_part('year', rentas.fecha_renta) as anio,
		date_part('month', rentas.fecha_renta) as mes,
		count(*) as numero_rentas
from rentas
group by anio, mes
order by anio, mes;

---names of the movies
select pelicula_id, titulo from peliculas
```
ya pasando a tableau las visualizaciones quedarian asi <a name="paragraph1"></a>
![Image 1](https://github.com/DamonReyes/Portfolio_Projects/blob/main/Screenshots/Dashboard%201%20(1).png)


dejo tambien el codigo original en formato de sql en esta misma carpeta

Dejo también el link original del dataviz [Tableau Viz](https://public.tableau.com/profile/damon.reyes#!/vizhome/SQL_routine/Dashboard1)

Y puedes ver todas mis visualizaciones en [Tableau_DamonReyes](https://public.tableau.com/profile/damon.reyes#!/vizhome/SQL_routine/Dashboard1)

> Damon reyes analista

Linkedin [Damon](https://www.linkedin.com/in/damon-reyes/)
