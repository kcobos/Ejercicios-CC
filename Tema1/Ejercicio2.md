# En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?

Como ya se ha hablado en el [Ejercicio 1](Ejercicio1.md), la arquitectura del servidor está por capas por lo que obliga a usar un mismo lenguaje de programación. También los datos obligan al comportamiento del sistema, así como herramientas adicionales. Como se puede ver, este tipo de arquitectura es muy restrictiva.

Si pasásemos el mismo sistema a una arquitectura basada en microservicios estaríamos dando libertad a la elección de emplear distintos lenguajes de programación en los distintos servicios, incluso dependiendo de la funcionalidad del servicio exprimiendo realmente el potencial a cada lenguaje de programación. Lenguajes propios de tratamiento de datos para analizarlos como R, Scala, Julia..., lenguajes más rápidos para acciones concisas como Rust, C/C++, Golang..., o lenguajes con un propósito más común como Perl, Python, Ruby...

A su vez, podríamos emplear distintos sistemas de bases de datos según sea más conveniente para almacenar los datos de las entidades controladas por los microservicios. Podríamos incorporar una base de datos InfluxDB para aquellos datos temporales, una base de datos estructurada para los datos más organizados o una base de datos NoSQL para datos no organizados...
