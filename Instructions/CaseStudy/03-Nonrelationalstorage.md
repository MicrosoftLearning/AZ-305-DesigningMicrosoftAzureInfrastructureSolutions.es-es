---
casestudy:
  title: Diseño de una solución de almacenamiento no relacional
  module: Non-relational storage solutions
---
# Caso práctico de diseño de almacenamiento no relacional

## Requisitos

Tailwind Traders quiere reducir los costos de almacenamiento mediante la reducción del contenido duplicado y, siempre que sea aplicable, su migración a la nube. Querrían una solución que centralice el mantenimiento y proporcione acceso mundial a los clientes que navegan por archivos multimedia y contenidos de marketing. Además, querrían abordar el almacenamiento de archivos de datos de la empresa. 

![Arquitectura de almacenamiento no relacional](media/Nonrelational%20storage.png)

 

* **Archivos multimedia**. Los archivos multimedia incluyen fotos de productos y vídeos de características que se muestran en el sitio web público de la empresa, que se desarrolla y mantiene internamente. Cuando un cliente navega a un elemento, se muestran los archivos multimedia correspondientes. Los archivos multimedia están en diferentes formatos, pero JPEG y MP4 son los más comunes. 

* **Contenido de marketing**. El contenido de marketing incluye historias de clientes, folletos de ventas, gráficos de tallas e información de fabricación ecológica. Los usuarios de marketing internos acceden al contenido a través de una unidad asignada en sus estaciones de trabajo de Windows. Los clientes acceden al contenido directamente desde el sitio web público de la empresa.

* **Documentos corporativos**. Estos son documentos internos para departamentos como recursos humanos y finanzas. Una aplicación web desarrollada internamente permite acceder a estos documentos y administrarlos. El departamento jurídico requiere que se conserven varios documentos durante un período de tiempo específico. En ocasiones, los documentos deberán conservarse más tiempo cuando se investiguen problemas legales o de RR. HH. La mayoría de los documentos corporativos con más de un año de antigüedad solo se conservan por motivos de cumplimiento y rara vez se accede a ellos.

* **Ubicación de los archivos**. Todos los archivos se almacenan localmente en el centro de datos de la oficina principal. Hay numerosos recursos compartidos de archivos organizados por departamento o línea de producto. Los servidores de datos tienen dificultades para proporcionar archivos para el sitio web. Durante las horas punta, las páginas del sitio web tardan en cargar. 

* **Frecuencia de acceso a archivos**. Algunos productos son más populares y, por ello, se accede a sus datos con más frecuencia. Sin embargo, a algunos productos, como los equipos de esquí, solo se accede durante un periodo determinado. Las rebajas generan mucho interés en ciertos artículos con descuento. 

## Tareas

1. Diseña una solución de almacenamiento para Tailwind Traders. 

      * ¿Qué tipo de datos se representa? 

      * ¿Qué factores tendrás en cuenta para crear tu diseño?

      * ¿Usarás los niveles de acceso de blobs?

      * ¿Usarás almacenamiento inmutable?

      * ¿Cómo se accederá al contenido de forma segura?

2.  La solución debe tener en cuenta los archivos multimedia, el contenido de marketing y los documentos corporativos. Tus recomendaciones pueden ser diferentes en función de los datos. Prepárate para argumentar tus decisiones. 

¿Cómo incorporas los pilares del Marco de buena arquitectura para producir una arquitectura en la nube estable, eficiente y de alta calidad?
