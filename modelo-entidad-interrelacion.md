
## Definiciones
Un **dato** es informacion almacenable y con significado.  
Una **base de datos** es un conjunto de datos interrelacionados.  
Un **sistema gestor de base de datos (SGBD)** consiste en una base de datos y las operaciones que hacemos con los datos.

## Funciones de un SGBD
- Crear, modificar, eliminar y consultar datos
- Gestionar integridad, seguridad, concurrencia, recuperación y transacciones de datos.

## Modelos de BDD
- Modelo Entidad-Interrelación (o entidad-relacion)
- Modelo relacional
- Modelo de Objetos

# Modelo Entidad - Interrelación (E - R)
- Conjuntos de tipos de entidades
- Atributos
- Conjunto de relaciones

Las entidades se dibujan como un cuadrado con el nombre de la entidad. Puede ser un conjunto de tipos de entidades.

Los conjuntos de relaciones se representan como un rombo, pueden relacionar dos o más entidades. Se representan generalmente como verbos.

![alumno estudia en universidad](./resources/alumno%20universidad.png)

Las claves únicas ( ej DNI ) van subrayados en este modelo.
Los atributos se representan en un circulo

## Clasificación de atributos
- Simples o compuestos
- Monovaluados o multivaluados
- Almacenados o derivados

Es **simple** cuando es indivisible, **compuesto** cuando se puede separar en partes.  

Es **monovaluado** cuando tiene un valor (nombre), **multivaluado** cuando puede tener más de un valor (nombres), el multivaluado se representa poniendole dos circulos al atributo.  

Es **almacenado** lo que quiero persistir, **derivado** el que es calculable y se representa con el circulo punteado.  

![alt text](./resources/tipos%20de%20atributos.png)
Una superclave es un conjunto de entidades que identifica a una identidad.

## Restricciones estructurales
- De participación: mínimo de entidades que participan en una relación con otro tipo de entidades.
- De cardinalidades: máximo de entidades que participan en una relación con otro tipo de entidad.

## Relaciones
- Grado (binaria, ternaria): cantidad de tipos de entidades que participan de la relación.
- Participacion
- Cardinalidad
- Pueden tener atributos, pero no pueden ser la clave de la relación.

![alumno estudia en universidad con participaciones](./resources/alumno%20universidad%20participaciones.png)  

Este diagrama se lee "Un alumno puede estudiar en una universidad y una universidad puede tener muchos alumnos".  
Se relaciona un tipo de entidad con el paréntesis que está enfrente.

## Relaciones - Restricciones de unicidad

(binarias)
Si en el modelo se define que los máximos de la relación son 1 y 1 se usa una clave de cualquiera de las dos entidades, ya que usar ambas no sería un dato simple.  

Si los máximos son 1 y n, se toma la clave del que está del lado de la n. Porque el otro se relaciona a muchos de estos, por lo tanto, no sirve para representar la relación de manera única.  

Si los máximos son n y 1, idem 1 y n.  

Si los máximos son n y m, se usa el par de claves de ambas entidades.  

## Relación Unaria
![jefe empleado](./resources/jefe%20empleado.png)  
### Nótese que esta vez, el paréntesis está del mismo lado que la instancia

## Entidades fuertes y débiles
Una entidad es fuerte si se puede identificar con sus propios atributos, caso contrario es débil. 

Una entidad débil se representa con doble cuadrado, doble línea en su lado de la relación y doble línea en la relación. Tiene un campo que se llama discriminante y sirve para, junto a la clave de la otra entidad, generar la clave de la relación

![entidades fuertes y debiles](./resources/entidades%20fuertes%20y%20debiles.png)
