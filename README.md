# LAS ROZAS SMART CONTAINERS AUTOMATITATION

The objective of this proyect is to intuitively display real-time information for each of the smart containers located in Las Rozas (Madrid). This proyect will be implemented using a semantic web aproach.

The primary stakeholder for this data will be the municipal government, as it will help optimize service efficiency and provide control over the various containers. The application's goal is to simplify data interpretation and organize it more effectively. The aim is to make real-time data available for each container and automate certain municipal services. The information displayed from the smart containers will be diverse, including:
* location
* recyclable materials
* total capacity
* fill percentage
* garbage collections

With this data, it will be possible to automate notifications to the garbage collection center when a certain garbage percentage is exceeded, thereby avoiding unnecessary services and scheduling pickups only when needed. Furthermore, valuable insights can be gained regarding what is being recycled the most and where, enabling the promotion of recycling in areas where lower recycling rates are detected.


## ONTOLOGY

### Classes

* Contenedor

Cada contenedor será una instancia de esta clase.

* Recolecciones Pasadas

Por cada recolección de basura, se crea una instancia de esta clase

* Location

Representa la ubicación real de cada contenedor

### Properties

* ubicadoEn

Domain: Contenedor

Range: Ubicación

Inverso de: ubicacionDe

* ubicacionDe
Domain: Contenedor

Range: Ubicación

Inverso de: ubicadoEn

* tieneRecolección
  
Domain: Contenedor

Range: Recolecciones Pasadas

Inverso de: recolectadoDe

* recolectadoDe

Domain: Contenedor

Range: Recolecciones Pasadas

Inverso de: tieneRecolección

* fecha
  
Domain: Recolecciones Pasadas

Range: Date

* motivo_de_recolección

Domain: Recolecciones Pasadas

Range: String

* tiempo_respuesta_aviso

Domain: Recolecciones Pasadas

Range: Float

* litros_recolectados
  
Domain: Recolecciones Pasadas

Range: Float

* frecuencia_media_recolecciones

Domain: Contenedor

Range: Float

* material

Domain: Contenedor

Range: String

* porcentaje_de_llenado
  
Domain: Recolecciones Pasadas

Range: nonNegativeInteger

* tieneId
  
Domain: Contenedor

Range: nonNegativeInteger
