&#x20;Diseño y Validación de Resultados de Liga MX con XML y XML Schema (XSD)



&#x20;Descripción

Este repositorio contiene la estructura y validación de los resultados de fútbol de la Liga MX, correspondientes a la jornada del domingo 27 de septiembre de 2026, utilizando la tecnología de esquemas `XML Schema Definition (XSD)`.



&#x20;Estructura del Repositorio

\* `xml/resultados.xml`: Documento XML que almacena la información jerárquica de la jornada, los partidos, los equipos, los marcadores y las estadísticas.

\* `xsd/resultados.xsd`: Archivo de validación de esquema que define estrictamente los tipos de datos (como `xs:date` para la fecha y `xs:integer` para los goles y tiros), la cardinalidad y los atributos obligatorios.



&#x20;Ventajas del diseño con XSD

A diferencia de DTD, el uso de XML Schema permitió:

1\. \*\*Tipado de datos:\*\* Garantizar que el marcador y el número de jornada sean estrictamente números enteros (`xs:integer`), y que la fecha respete el formato universal (`xs:date`).

2\. \*\*Reutilización:\*\* Se creó un tipo complejo `tipoEquipo` que se aplicó tanto para `<equipoLocal>` como para `<equipoVisitante>`, evitando duplicar las reglas de validación para ambos elementos.

