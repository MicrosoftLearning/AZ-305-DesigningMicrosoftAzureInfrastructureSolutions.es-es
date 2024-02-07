---
casestudy:
  title: 'Diseño de una solución de red: aplicación empresarial de BI'
  module: Network infrastructure solutions
---
# Diseño de una solución de infraestructura de red  

## Requisitos

A medida que el equipo de TI de Tailwind Traders Enterprise se prepara para definir la estrategia para migrar algunas de las cargas de trabajo de la empresa a Azure, debe identificar los componentes de red necesarios y diseñar una infraestructura de red necesaria que los admita. Teniendo en cuenta el ámbito global de sus operaciones, Tailwind Traders va a usar varias regiones de Azure para hospedar sus aplicaciones. La mayoría de estas aplicaciones tienen dependencias de infraestructura y servicios de datos, que también residirán en Azure. Las aplicaciones internas migradas a Azure deben seguir siendo accesibles para los usuarios de Tailwind Traders. Las aplicaciones accesibles desde Internet migradas a Azure deben seguir siendo accesibles para cualquier cliente externo. 

Para crear el diseño de red inicial, el equipo de TI de Tailwind Traders Enterprise eligió dos aplicaciones clave, que son representativas de las categorías de cargas de trabajo más comunes que se esperan migrar a Azure.  

## Diseño: aplicación empresarial de BI 

![Arquitectura de la aplicación empresarial de BI](media/compute.png)

-   Una aplicación empresarial de inteligencia empresarial (BI) interna de tres niveles basada en Windows con un nivel front-end que ejecuta servidores web ISS, un nivel intermedio que hospeda la lógica de negocios basada en .NET Framework y un nivel back-end implementado como una base de datos de grupo de disponibilidad Always On de SQL Server. 

-   Esta aplicación se clasifica como crítica y requiere disposiciones de alta disponibilidad con un acuerdo de nivel de servicio de disponibilidad del 99,99 % y disposiciones de recuperación ante desastres, con un objetivo de punto de recuperación de 10 minutos y un sistema operativo en tiempo real de 2 horas.

-   Para proporcionar conectividad a las aplicaciones internas migradas a Azure, Tailwind Traders deberá establecer la conectividad híbrida desde sus centros de datos locales. El grupo de TI empresarial ya ha establecido que dicha conectividad se implementará mediante el uso de un circuito ExpressRoute desde su principal centro de datos de Seattle; sin embargo, en este momento no está claro cuál sería la solución de conmutación por error en caso de que el circuito deje de estar disponible. El director financiero de Tailwind Traders quiere evitar pagar por otro circuito ExpressRoute redundante. 

- Hay consideraciones adicionales que se aplican a la conectividad local de las aplicaciones internas migradas a Azure. Dado que el entorno de Azure de Tailwind Traders constará de varias suscripciones y, en la práctica, de varias redes virtuales para minimizar el coste, es importante reducir el número de recursos de Azure necesarios para implementar las funcionalidades de red principales. Estas funcionalidades incluyen conectividad híbrida a ubicaciones locales, así como filtrado de tráfico. Además, esta necesidad de minimizar el coste se alinea con los requisitos de Seguridad y riesgo de la información, que indican que todo el tráfico entre ubicaciones locales y redes virtuales de Azure debe realizarse a través de una sola red virtual, que hospedará los componentes responsables de la conectividad híbrida y el filtrado de tráfico. 

-   Según los requisitos definidos por los equipos de Seguridad de la información y riesgo de Tailwind Traders, toda la comunicación entre las máquinas virtuales de Azure en los distintos niveles que forman parte de la misma aplicación debe permitir solo los puertos necesarios para ejecutar y mantener la aplicación. Sin embargo, debido a las limitaciones de espacio de direcciones IP, es posible que no sea posible asignar subredes específicas a cada nivel. El grupo de TI empresarial debe identificar la manera óptima de configurar el origen y el destino para el filtrado de tráfico de modo que no fuera necesario hacer referencia directamente a direcciones IP o intervalos de direcciones IP.


## Tareas: aplicación empresarial de BI 

1. Diseña una solución de red de 3 niveles para la aplicación de BI. El diseño podría incluir Azure ExpressRoute, VPN Gateways, Application Gateways, Azure Firewall y Azure Load Balancers. Los componentes de red deben agruparse en redes virtuales y se deben tener en cuenta los grupos de seguridad de red. Prepárate para explicar por qué has elegido cada componente de la solución. 

2. En lo referente a la solución de arquitectura del caso práctico de proceso, ¿cómo afectaría esto al diseño de red? ¿Necesitarías algún recurso de red adicional para garantizar el acceso a la aplicación modernizada? ¿Ya no necesitarás algunas de las soluciones recomendadas implementadas en el diseño de red original? 

3. En lo referente al caso práctico de almacenamiento (relacional), ¿cómo actualizarías el diseño de red para garantizar el acceso a la cuenta de almacenamiento y asegurarte de que solo los usuarios seleccionados tengan acceso a la cuenta de almacenamiento?

4. En lo referente a la modernización del back-end de SQL, ¿cómo planeas habilitar el acceso pragmático a la base de datos para que el front-end no tenga secretos codificados de forma rígida en su código base?

¿Cómo incorporas los pilares del Marco de buena arquitectura para producir una arquitectura en la nube estable, eficiente y de alta calidad?
