---
casestudy:
  title: Diseño de una solución de almacenamiento relacional
  module: Relational storage solutions
---
# Caso práctico de diseño de almacenamiento relacional

## Requisitos

Tailwind Traders pretende trasladar la base de datos de su sitio web público a Azure, ya que el front-end del sitio web también se va a trasladar allí.  El front-end del sitio web solo se implementará inicialmente en 2 regiones por motivos de redundancia.  Sin embargo, se espera que, a medida que aumente el tráfico, el sitio web se replique en otras regiones de todo el mundo. La base de datos que se te ha pedido que migres contiene el catálogo de productos y todos los pedidos en línea.  Actualmente, la base de datos se ejecuta en un único grupo de disponibilidad local Always On de Microsoft SQL Server.

![Arquitectura de almacenamiento no relacional](media/relational%20storage.png)

Principales preocupaciones de Tailwind Traders:

-   **Alta disponibilidad**.  Una preocupación principal de Tailwind Traders es que esta base de datos sea de alta disponibilidad, ya que es fundamental para su negocio.  Las interrupciones pueden dar lugar a pérdidas de ventas o de confianza de los clientes.

-   **Rendimiento del sitio web.**  Aunque al hacer pedidos el rendimiento suele ser bueno, se informa de que la navegación y la búsqueda de páginas con muchos elementos son lentas.

-   **Seguridad**.  Tailwind Traders está muy preocupado por la información personal o financiera almacenada en la base de datos que se expone.  Además de implementar medidas de seguridad adecuadas, el equipo de seguridad debe comprobar que se implementan los procedimientos recomendados estándar del sector, siempre que sea posible.


## Tareas

1.  Diseña la solución de base de datos. El diseño debe incluir autorización, autenticación, precios, rendimiento y alta disponibilidad. 
2.  Haz un diagrama de tu decisión y explica la solución. 

¿Cómo incorporas los pilares del Marco de buena arquitectura para producir una arquitectura en la nube estable, eficiente y de alta calidad?
