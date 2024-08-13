---
casestudy:
  title: Diseño de soluciones de autenticación y autorización
  module: Authentication and authorization solutions
---


# Diseño de soluciones de autenticación y autorización

## Requisitos

A Tailwind Traders le está yendo muy bien y va a aumentar el personal. Ha adquirido un minorista en línea en el nicho de la ropa deportiva. La empresa también ha localizado a un socio para externalizar el contenido de marketing. Tailwind Traders usa Entra ID para cuentas de usuario y grupos. Estas son dos iniciativas específicas en las que el departamento de TI querría que echaras una mano. 

**Cuentas de usuario nuevas**

  * La adquisición de minoristas en línea agregará 75 empleados a Tailwind Traders. Todos los nuevos usuarios tienen cuentas locales en el dominio existente del minorista.

  * El nuevo asociado de marketing tendrá inicialmente 15 empleados que necesitarán acceso corporativo. Estos empleados ya tienen identidades de Microsoft Entra en el inquilino de Microsoft Entra del asociado.  

  * Los nuevos empleados se encuentran en varias ubicaciones geográficas y necesitarán privilegios de cuenta para sus nuevos puestos de trabajo. Se esperan algunos cambios en los puestos existentes. 

  * El departamento de TI quiere aprovechar esta oportunidad para incluir nuevas características de seguridad de identidad. 

**Nuevo acceso a la aplicación**

  * El equipo de desarrollo empresarial tiene una aplicación que se ejecuta en una máquina virtual de Azure y los datos se almacenan en una instancia de Azure SQL Database. Deben permitir de forma segura que la máquina virtual consulte la instancia de Azure SQL Database. 
  * También necesitan un servidor local para poder acceder de forma segura a la base de datos SQL sin almacenar credenciales en el código de la aplicación ni en los archivos de configuración.

## Tareas

**Cuentas de usuario nuevas**

  * Diagrama del proceso para incorporar las cuentas de usuario adquiridas.

  * Diagrama del proceso para agregar las nuevas cuentas de asociados. 

  * Para los requisitos anteriores, asegúrate de incluir las herramientas que se usarán. Enumera al menos tres ventajas de la solución sugerida. 

* Proporciona al menos tres recomendaciones para mejorar las soluciones de identidad de usuario de Tailwind Traders. Clasifica las recomendaciones en orden de importancia. Incluye tus razones para hacer estas sugerencias. 

**Nuevo acceso a la aplicación**

  * Proporciona una solución de acceso para la aplicación de desarrollo empresarial.

  * Proporciona una solución de acceso para los recursos locales.

¿Cómo incorporas los pilares del Marco de buena arquitectura para producir una arquitectura en la nube estable, eficiente y de alta calidad?
