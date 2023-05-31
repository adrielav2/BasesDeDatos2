Adriel Araya Vargas 
2019312845 
Instituto Tecnológico de Costa Rica.
Bases de Datos 2
IC-4302

# Quiz 9

1. Suponiendo que un sistema de bases de datos relacional que presenta un read-heavy
workload y los queries son muy diferentes, explique detalladamente ¿porque el uso
de caches puede afectar el rendimiento del sistema de forma negativa? 

Este se puede ver afectado principalmente por la falta de aprovechamiento del espacio de caché. Sí existen mucha variedad de consultas es bastante probable que las consultas y datos accedidos no se repitan lo suficiente como para que se este aprovechando el almacenamiento en caché de forma eficiente. También sí hay demasiadas consulta es probable que hayá una alta evicción de datos para almacenar nuevos datos y descartar existentes.

2. El particionamiento de tablas en bases de datos relacionales es un concepto muy
parecido al de shards en bases de datos NoSQL, explique detalladamente ¿Cómo
afecta el particionamiento y el sharding en el rendimiento de bases de datos SQL y
NoSQL?

En SQL el particionamiento permite distribuir la carga de trabajo entre diferentes particiones. Esto puede mejorar la de consultas y operaciones en cada partición. De forma negativa puede afectar a la hora de acceder datos en diferentes particiones y que requiera operaciones de combinación o unión de datos. Según la administración esto implica gestionar multiples particiones y las copias de seguridad, indexación o restauraciones deben realizarse de forma individual y con buena planeación.

En NoSQL el sharding afecta la escalabilidad horizontal, esto debido a que cada shard o nodo puede manejar una parte del tráfico y las consultas lo que mejora la capacidad de respuesta del sistema. También puede distribuir entre multiples shards la carga de trabajo y evitar los cuellos de botella. Este también afectaría la consistencia y la disponibilidad de los datos. Si se utiliza un enfoque de sharding con replicación, es posible que se necesite tiempo para que los cambios se propaguen a todos los shards.

3. En un sistema de bases de datos con Strong Consistency cuyo workload es de
read-heavy y write-heavy, ¿Cómo afectan los exclusive locks el rendimiento de las
bases de datos NoSQL?

En un sistema de bases de datos NoSQL con strong consistency y una carga de trabajo equilibrada entre lecturas y escrituras, el uso de exclusivelocks puede generar cuellos de botella, reducir la capacidad de operaciones concurrentes, aumentar la latencia y limitar la escalabilidad del sistema. Las escrituras adquieren exclusivelocks, bloqueando otras escrituras y generando esperas, mientras que las lecturas deben esperar por los exclusivelocks adquiridos por las escrituras. 

4. Explique detalladamente, ¿Cómo afecta la selección de discos físicos el rendimiento
de una base de datos SQL y NoSQL?

Bases de datos SQL: La selección de discos físicos afecta el rendimiento de una base de datos SQL. Optar por discos de estado sólido en lugar de discos duros mejora la velocidad de lectura/escritura y reduce el tiempo de acceso. 

Bases de datos NoSQL: La elección de discos físicos también impacta en el rendimiento de las bases de datos NoSQL. Se recomienda utilizar discos de estado sólido  debido a su mayor velocidad y menor tiempo de acceso, especialmente en entornos distribuidos. La configuración de almacenamiento específica, como el uso de column families, puede optimizar la eficiencia. Además, distribuir los datos de manera equilibrada entre los nodos y utilizar técnicas de particionamiento o sharding ayudan a aprovechar el paralelismo. 





