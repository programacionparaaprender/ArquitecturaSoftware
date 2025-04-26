## Cursos
>- https://udemy.com/course/arquitectura-software-moderna-ddd-eventos-microservicios-cqrs/learn/lecture/32321188#overview

## repositorios
>- https://github.com/danielblanco96/arquitectura-software-udemy/tree/main

## Adicional
>- https://es.wikipedia.org/wiki/Arquitectura_de_software

### 1. Introducción al curso
<p><strong>Arquitectura Convencional</strong></p>

<p>Forma convencional de organizar el software.</p>
>- Monolitos.
>- Desestructurado y difícil de mantener.
>- Modelos muy dependientes del diseño de base de datos.
>- Muy poca organización.

#### Event Driven Design
>- Producción y reacción a eventos.
>- Tratamiento de acciones de forma asíncrona.
>- La parte que produce y la parte que consume están desacopladas.

#### Event Sourcing
>- Los cambios en el sistema se almacenan como eventos en BBDD.
>- Estado Actual = repetición de eventos desde un punto en el pasado.
>- Ideal para saber el estado exacto en un momento en el pasado.

#### Microservicios
>- División del sistema en pequeños dominios o subdominios.
>- Total independencia entre microservicios.
>- Cada microservicio vive en un entorno separado de los demás.
>- Máquina (física o virtual) propia.
>- Base de datos.
>- Otros recursos.
>- Comunicación mediante protocolos ligeros (HTTP, mensajería etc).
>- Posibilidad de formar equipos para cada uno de ellos.

#### Otros patrones y estilos de arquitectura
>- Arquitectura hexagonal.
>- Microkernel architecture.
>- Arquitectura testable.
>- Evolving architecture.
>- Sacrificial architecture.

### 2. Arquitectura Convencional
>-  Hace 50 o 60 años la mayoría del software era mucho más sencillo que hoy en día.
>- Necesidad de automatizar tareas.
>- CRUDs simples.
>- etc.
>- Esto llevó a software del siguiente tipo.
>- Pequeños scripts de automatización.
>- Monolitos.
>- Muchas interdependencias entre los componentes internos.
>- Código desestructurado y difícil de mantener.
>- Monolitos

#### Modelo Anémico
>- Clases que no almacenan lógica, únicamente datos.
>- Muy comunes en CRUD's
>- Lógica necesaria se implementa en servicios.
>- Considerado un antipatrón de diseño

#### Dependencia entre componentes
>- En monolitos y arquitecturas convencionales es muy común tener componentes muy acoplados. El siguiente escenario es muy común:
>- Componente A necesita un componente Z. Lo implementamos.
>- Surge una necesidad de ciertas funcionalidades de Z en el componente B.
>- Pasa lo mismo en C, D...
>- Con el tiempo, las necesidades evolucionan, y se adapta Z para que abarque todo lo que necesiten A, B, C y D.
>- !Este tipo de decisiones hacen que nuestra arquitectura sea rígida y difícil de modificar¡

### 3. Pros y Contras de la Arquitectura Convencional

<p><strong>Aspectos positivos</strong></p>
>- Mayor velocidad de desarrollo al inicio del proyecto.
>- Menor complejidad, arquitectura muy sencilla.
>- Cualquier desarrollador sin experiencia se puede adaptar rápidamente.
>- Puede ser más fácil de testear que otras arquitecturas.
>- Compilación y despliegue sencillos.

<p><strong>Aspectos negativos</strong></p>
>- Difícil de mantener a largo plazo.
>- Tendencia a una gran dependencia entre los distintos componentes.
>- Arquitectura rígida y difícil de modificar en el futuro.
>- Mayor dificultad a la hora de repartir el trabajo.
>- Si queremos actualizar el sistema, debemos desplegarlo de nuevo completamente.

<p><strong>Aspectos negativos</strong></p>
>- Proyecto pequeños, con pocos requisitos y claramente definidos.
>- Sistemas con un corto tiempo de vida.
>- Equipo con muy poca experiencia.
>- !Una arquitectura convencional no significa que no sea necesario preocuparse por escribir código de buena calidad¡
>- Se debe escribir buen código para que, en caso de que el sistema crezca, nos podamos adaptar, cambiar de arquitectura etc.


<p><strong>Arquitectura centrada en los datos</strong></p>
>- Se piensa primero en los datos que se necesitan almacenar.
>- Se recopilan requisitos para tener claras las reglas de negocio.
>- Diseño del modelo de datos.
>- Diseñamos y construimos nuestro sistema para trabajar con los datos.
>- Como consecuencia, tenemos una arquitectura de software totalmente dependiente de los datos.

### 4. ¿Qué es el Domain Driven Design?
>- Se piensa primero en el dominio del problema.
>- El objetivo es ser expertos en el dominio.
>- Se modelan todas las entidades y reglas especificas del dominio.
>- A partir de ahí, se implementan los casos de uso que queremos resolver.


#### Tiempo de desarrollo
>- Centrada en el dominio <-> Centrada en los datos
>- EL dominio es invariable, no depende del problema.
>- Los casos de uso son mucho más inestables, tienden a cambiar con el tiempo.
>- Separando los casos de uso y las reglas del dominio conseguimos independizar dos partes con inestabilidades muy diferentes.
>- Esto hace que nuestro sistema sea mucho más flexible.

##### Centrada en el dominio
>- EL dominio es invariable, no depende del problema.
>- Los casos de uso son mucho más inestables, tienden a cambiar con el tiempo.
>- Separando los casos de uso y las reglas del dominio conseguimos independizar dos partes con inestabilidades muy diferentes.
>- Esto hace que nuestro sistema sea mucho más flexible.

##### Centrada en los datos


### 5. Lenguaje Ubicuo

<p><strong>¿Qué es el lenguaje ubicuo?</strong></p>

>- Vocabulario común que describe el dominio del problema Verbos, nombres, adjetivos etc.
>- Es compartido por todos los interesados del proyecto. PMs, programadores, expertos de dominio, clientes etc.
>- Se debe usar siempre para evitar malentendidos.
>- Evitamos usar sinónimos del mundo real que podrían significar otra cosa en nuestro dominio
>- El objetivo es utilizar un lenguaje común, independientemente del rol desempeñado.

#### Características de lenguaje ubicuo
>- Se crea a partir de sesiones de brainstorming y análisis del dominio.
>- Se documenta y debe ser claro y lo menos ambiguo posible.
>- Es parte de un proceso iterativo.
>- El lenguaje ubicuo evoluciona según vamos aprendiendo más sobre el dominio
>- Ubicuo: "Que está presente a un mismo tiempo en todas partes."
>- Se debe usar en conversaciones, emails, historias de usuario y código.

#### Ejemplo
>- "Como monitor del gimnasio, quiero que los usuarios con tarifa completa se puedan registrar y asistir a clases particulares."
>- Monitor
>- Gimnasio
>- Usuario
>- Tarifa
>- Registrar 
>- Asistir
>- Clase particular

### 6. Contextos Acotados
>- contexts_acotados3.png
>- Equipo Información del gimnasio
>- Equipo Información de pago
>- Equipo Información de reservas
>- Gym
>- Address
>- Class
>- Facility

#### Definición
>- Nueva forma de organizar el modelo y la lógica de negocio guiado por el dominio.
>- Un cotexto acotado es aquel que tiene un sentido especial en el dominio.
>- Cada uno tiene su lenguaje ubicuo propio.
>- Las entidades fuera del contexto pueden tener características ligeramente diferentes.
>- Tener definida la misma entidad en diferentes contextos no implica una duplicidad de código, si no una aclaración del mismo.
>- Compartiendo modelo entre contextos, se tiende a acumular detalles e información de todos ellos, poniendo en riesgo la integridad del modelo.

### 7. Mapeo de Contextos
<p><strong>Dependencias entre distintos contextos</strong></p>

>- A pesar de que es positivo separar nuestro modelo en contextos acotados, la lógica de un sistema software complejo implica interacción entre los distintos contextos.
>- Los contextos no son completamente independientes.
>- Debemos tener clara la interacción y dependencias entre los mismos.

#### Tipos de relaciones
>- Conformista (Conformist). No existe ninguna capacidad de negociación.
>- Cliente / Proveedor (Customer / Supplier). Dependencia con cierto grado de negociación. Necesidades en el cliente pueden implicar cambios en el proveedor.
>- Socio (Partnership). Ambos contextos colaboran por una meta en común, por lo que ambos lados de la relación tienen poder para influenciar al otro.
>- Núcleo compartido (Shared Kernel). Dos o más contextos comparten un mismo modelo. Todos necesitan estar de acuerdo para realizar cambios. Difícil de mantener.

#### Tipos de relaciones 2
>- Capa anticorrupción (Anticorruption Layer). Interfaz que utiliza Downstream para interactura con Upstream, sin importar los cambios realizados en el último.
>- Open Host Service / Published Language. Relaciones de tipo conformista en las que se provee de documentación al Downstream context. Además se proporcionan versiones y compatibilidades entre ellas.

### 8. Capas del Domain Driven Design

#### Capa de presentación
>- En el pasado, se construía la vista desde el servidor, por eso se consideraba parte de la presentación.
>- Ahora es muy común tener la vista separada. React, Angular, Vue etc.
>- API de entrada a nuestro sistema que da soporte a la interfaz de usuario.
>- Es la fachada e interactúa con los servicios de aplicación para iniciar los casos de uso.
>- @Controller en Spring


#### Capa de aplicación
>- Encargada de orquestar todos los casos de uso necesarios para el funcionamiento de nuestro sistema.
>- Interactúa con el dominio para ejecutar su lógica especificada.
>- Interactúa con la infraestructura para la persistencia, framework, logging etc.
>- Responde a la presentación con los datos formateados correctamente.
>- @Service en Spring

#### Dominio
>- Datos y lógica central de nuestro sistema, diseñada bajo los principios de DDD.
>- Debe estar lo más aislado posible del exterior. Se comunica con infraestructura si necesita algún aspecto como logging.
>- Se compone de entidades de dominio y servicios de dominio.
>- Entidades de dominio
>- Datos.
>- Lógica.
>- No son entidades de persistencia (@Entity en Spring).
>- Servicios de dominio
>- Lógica de dominio que no se pueda asignar a una entidad de dominio específica.
>- Siguen los principios del DDD.
>- @Service en Spring

#### Capa de infraestructura
>- Persistencia.
>- Objetos de ORMs (@entity etc).
>- Detalles del Framework
>- Clases de configuración
>- Arranque de la aplicación
>- Otros aspectos de infraestructura
>- Logging

#### Dependencias
>- Las flechas indican el flujo de la información, no la dependencia.
>- Es importante conseguir la IoC usando técnicas como la inyección de dependencias.

#### Dependencias 2
>- Es importante que el dominio sea lo más estable de nuestro sistema.
>- Nunca debemos modificar nuestro dominio para adaptarlo al exterior, como por ejemplo BBDD.
>- En ese caso, lo apropiado es adaptar la capa de infraestructura.

### 9. Modelo de Dominio
>- Entidades
>- Clases con datos y comportamiento
>- Value Objects
>- Clases con simplemente datos.
>- Sirven para representar de manera más clara los atributos de las entidades.
>- Deben ser inmutables
>- Aggregates
>- Grupos de entidades y Value Objects
>- Separan conceptos diferentes de nuestro dominio.
>- Como norma general, la comunicación entre distintos aggregates se debe hacer a través de la raíz de los mismos. Una raíz no puede acceder a otro elemento no raíz de un aggregate diferente.

### 10. Modelo de BBDD vs Modelo de Dominio

#### Modelo de persistencia
>- Modelo ligado totalmente a nuestro modelo de bases de datos.
>- Está orientado a que nos sea más fácil realizar las operaciones en base de datos.
>- Consultas
>- Inserciones
>- Modificaciones
>- Eliminaciones
>- Sólo contiene información, no comportamiento.
>- Se puede usar una herramienta de mapeo objecto-relacional.
>- Hibernate
>- Entity Framework

#### Modelo de dominio
>- Orientado a modelar el dominio del problema
>- Datos
>- Compontamiento
>- Es un modelo que se puede persistir.
>- Mapeo entre modelo de dominio y de persistencia.
>- No tiene ningún conocimiento sobre la BBDD.

### 11. Servicios de Dominio
>- Ejecutan lógica que no tiene cabida en ninguna de las entidades.
>- Suele ser para coordinar dos o más tipos de aggregates, pero no tiene por qué.
>- Son parte del dominio, no se crean de forma arbitraria.
>- Se identifican en las sesiones de brainstorming
>- Son parte del lenguaje ubicuo.
>- Acciones como save, delete, upsert no tienen cabida en los servicios de dominio.

#### Servicios de dominio
>- Estimación de la esperanza de vida para una persona.
>- Implementarlo en la entidad País.
>- No tiene sentido que el País calcule ese dato para una persona.
>- Implementarlo en la entidad Persona.
>- Podría tener sentido, pero violaríamos el SRP en esa entidad.
>- La mejor opción es implementar esa lógica en un servicio de dominio, que coordine ambos aggregates.

### 12. Resumen Domain Driven Design
<p><strong>La importancia del dominio</strong></p>

>- El DDD se centra en la importancia de entender bien el dominio de nuestro problema para crear buen software.
>- En contraste al enfoque tradicional, centrado en los datos que tratamos.
>- Para identificar los elementos del dominio se utiliza
>- Lenguaje ubicuo, brainstorming.
>- Identificación de los contextos acotados.
>- Mapeo de contextos.
>- Todo esto se hace con el fin de separar la lógica de aplicación (casos de uso) de la lógica de dominio.
>- Los casos de uso varían mucho más frecuentemente.

#### Modelar el dominio
1. Entidades.
>- Elementos del dominio con entidad propia.
>- Comportamiento + datos.

2. Value Objects.
>- Elementos que almacenan solo datos.
>- Creados para representar de forma más clara los atributos de las entidades.

3. Aggregates.
>- Conjunto de entidades y value objects con un sentido común.

4. Domain Services.
>- Elementos del dominio con lógica que no tiene cabida en ninguna de las entidades.

### 13. Pros y Contras Domain Driven Design

#### Aspectos positivos
>- Lenguaje común compartido por todos los integrantes del proyecto. Perfiles técnicos y no técnicos.
>- Al tener lógica de aplicación y dominio separadas, el coste de realizar modificaciones suele ser menor, ya que el dominio cambia con poca frecuencia.
>- El código del dominio es autoexplicativo.
>- Mayor velocidad de desarrollo a medio y largo plazo. Mucho más mantenible.

#### Aspectos negativos
>- Mucho más lento al principio de un proyecto.
>- Requiere tener expertos en el dominio del problema.
>- Cambio de mentalidad de los desarrolladores para enfocarse en la funcionalidad más que en los datos.
>- Los frameworks actuales nos "empujan" a un modelo anémico y a pensar centrándonos en los datos.

#### Cuándo usar
>- Proyectos complejos con un largo tiempo de vida esperado.
>- Incertidumbre en los casos de uso. Previsión de cambios en el futuro.
>- Problemas con una lógica de dominio presente.
>- Si lo único que necesitas es un CRUD, no tiene sentido.
>- Disponibilidad de un equipo comprometido en analizar detalladamente el dominio.

## Sección 3: Command Query Responsibility Segregation (CQRS)

### 14. Introducción a CQRS
##### Comandos y consultas
1. Comandos.
>- Acciones que realizan una modificación en el estado del sistema y que no devuelven información.
>- Ejemplo: Iniciar un partido de tenis.
 2. Consultas.
 >- Acciones que no alteran el estado del sistema, tan sólo devuelven datos.
 >- Ejemplo: Obtener los últimos diez partidos de tenis.

 ### 15. CQRS Avanzado
 ¿Qué sucede si necesitamos eficiencia en las lecturas pero no queremos sacrificar tiempo en las escrituras?

#### Métodos de sincronización
1. Consistencia inmediata.
>- Método síncrono.
2. Consistencia eventual.
>- Sincronización asíncrona.
3. Consistencia programada.
>- Sincronización a ciertas horas del día.
4. Consistencia bajo demanda.
>- Se realiza la sincronización cuando se determine necesaria.

### 16. Ejemplo Practico CQRL


### 17. Mejorando las Escrituras
>- Dependencia directa con el mecanismo de sincronización.
>- Complejidad para insertar el modelo de escritura en la BBDD de lectura.
>- Sistemas que almacenan el estado como una secuencia de eventos.

#### Beneficios event sourcing + cqrs
1. Independencia del sistema de sincronización.
>- No es necesario realizar una llamada directa para activarlo.
>- Command Stack genera eventos y el sistema de sincronización los consume.

2. Las traducciones de eventos son más sencillas.
>- Traducir una entidad completa es más complejo que traducir un evento.
>- Podemos elegir desde dónde sincronizar.

### 18. Pros y Contras de CQRS

#### Aspectos positivos
1. Tratamiento independiente de las lecturas y las escrituras.
>- Posibilidad de tener dos modelos distintos.
>- Uso de bases de datos adecuadas para cada situación.
>- Escalado independiente en función de las necesidades de lectura / escritura.
>- Normalización y desnormalización independientes.

2. Posibilidad de tener dos equipos independientes.
>- Un equipo para el stack de comandos.
>- Otro equipo para el stack de consultas.

#### Aspectos negativos
1. Gran complejidad
>- Mantenimiento de dos stacks distintos para escritura y lectura.
>- Mantenimiento de múltiples bases de datos.
2. Sincronización
>- Mantener la consistencia de los datos es un problema añadido.

3. Duplicidad / redundancia de código

#### Cuándo usar
>- Sistemas dónde la escalabilidad es muy importante o crítica.
>- Volumen de datos y transacciones elevados.
>- Proyectos con problemas de rendimiento.
>- No es necesaria una consistencia inmediata de la información.
>- Distinto tratamiento para las escrituras y lecturas.
>- Equipos grandes

## Eventos

### 19. Introducción a los Eventos
#### ¿Que es un evento?
>- Un evento es algo que ha sucedido en el pasado, por lo tanto, son entidades inmutables.
>- Forma básica de interacción en el mundo real. Menos usado en el software, dónde es más frecuente el estado.
>- Es una forma de representar la información a más bajo nivel. Ofrecen más información que el simple estado final de una entidad.
>- No nos perdemos nada de lo que sucede en nuestro sistema.

#### ¿Donde aplicar eventos?
1. Event Sourcing
>- Persistencia de eventos, en lugar del estado actual.
>- Se ejecutan los eventos para obtener el estado en cierto momento.
>- Se puede combinar con CQRS.

2. Event Driven Programming
>- Eventos de aplicación.
>- Una entidad los produce y los lanza, otra los recibe y procesa.
>- Procesamiento asíncrono.

3. Event Driven Architecture

### 20. Introducción al Event Sourcing

#### ¿Que es event sourcing?
>- Técnica que se basa en almacenar todos los cambios producidos en el sistema en un almacén de datos, en lugar de almacenar el estado actual.

#### Captura del momento de una acción
>- Problema muy común.
>- Login / logout, tiempo de sesión, acción específica realizada en tu sistema etc.

#### Constancia del momento de una acción
1. Problema muy común.
>- Login / logout, tiempo de sesión, acción específica realizada en tu sistema etc.
2. Soluciones específicas
>- Herramientas de logging.
>- New Relic.
>- Google Analytics.

#### No es algo nuevo ni innovador
>- Las bases de datos relacionales ya almacenan todas las acciones realizadas sobre cada entidad de la misma forma. Estas acciones son las transacciones.

### 21. Event Sourcing al Detalle

#### Propiedades de los eventos
>- Son acciones que han sucedido en el pasado.
>- Los eventos deben ser entidades inmutables.
>- Nunca deben ser eliminados o modificados, tan solo insertados.
>- Para desechar una acción realizada por un evento pasado debemos lanzar otro evento que revierta los cambios.
>- Permiten conocer el estado del sistema en un punto en concreto del pasado. Ejecutar los eventos hasta el punto deseado.

#### campos de un evento
>- ID
>- TIMESTAMP
>- Detalles del evento

#### Operaciones event sourcing
>- add
>- update
>- delete: El borrado es lógico, nunca físico.

#### DDD y Event Sourcing
>- Los eventos no se limitan a las operaciones de un CRUD.
>- Create
>- Update
>- Delete
>- Si se usa DDD, los eventos son expresiones del lenguaje ubicuo.
>- Eventos del partido de tenis.
>- Start
>- Finish
>- Point
>- Warn

#### Proyección de datos a partir de eventos
1. Consulta de eventos, filtrado por ID de reserva y ordenados por timestamp
2. Creamos una nueva instancia de la entidad.
3. Aplicamos los eventos en orden.
4. Devolvemos la entidad que representa el estado actual.

#### Problemas de eficiencia
1. En entidades con muchos eventos, podría ser lento ejecutarlos todos. Ejemplo del carrito de una web de compras.
2. Uso de snapshots. 
>- Representación del estado de la entidad en un momento concreto del pasado.
>- Para obtener el estado actual ejecutamos los eventos a partir de la última snapshot.
1. Gestionar snapshots implica procesamiento y espacio. 
>- Usar en situaciones dónde la ganancia sea sustancial.
>- Eficiencia necesaria 

### 22. Event Sourcing y CQRS
1. CQRS
>- La gran ventaja es la independencia de las lecturas y las escrituras, pudiendo optimizar ambas.
>- El gran problema es la necesidad de sincronizar ambos almacenes de datos

2. Event Sourcing
>- La gran ventaja es la trazabilidad del estado del sistema.
>- EL gran problema es obtener el estado actual.

3. Usando ambas técnicas, tenemos lo bueno de ambas y mitigamos lo malo.
>- Dos almacenes de datos con optimización independientemente.
>- Trazabilidad del estado del sistema en el tiempo.
>- Escrituras más rápidas, ya que no hay updates ni deletes físicos.
>- Sincronización más sencilla e independiente de las escrituras.

### 23. Ejemplo Práctico de Event Sourcing

### 24. Pros y Contras Event Sourcing
#### Aspectos positivos
1. Trazabilidad del estado del sistema en el tiempo.
>- Recuperación del estado en días pasados.
>- Estadisticas y análisis

2. Nos proporciona un log de las acciones de los usuarios.
>- No hay necesidad de usar librerías externas ni implementar logging propio.

3. Es más eficiente especialmente que guardar un log con la entidad completa
4. Con CQRS podemos aprovechar los beneficios de ambos, mitigando los puntos débiles.
5. Al no tener UPDATES ni DELETES físicos, es más eficiente en las escrituras.

#### Aspectos negativos
1. Eficiencia en las consultas
>- Se puede mitigar el problema con snapshots o eliminarlo usando CQRS.
2. Eficiencia espacial
>- Necesita mucho más espacio que para representar simplemente el estado.
3. Dificultad para debuggear.
>- No hay forma sencilla de hacer consultas directas para conocer el estado actual.
4. Técnica mucho menos usada.
>- Será menos intuituva para los programadores.
>- Necesita un tiempo de adaptación.
5. Tratamiento de dominios amplios.
>- Pocos eventos son fáciles de tratar, pero se puede complicar con dominios grandes.

### Cuándo usar
>- Situaciones dónde consideremos usar CQRS
>- Cuando necesitemos conocer el estado del sistema en un instante del pasado.
>- Necesidad de un log con todas las acciones realizadas por los usuarios.
>- Cuando la eficiencia de las consultas no sea algo crítico.

### 25. Event Driven Programming
>- Paradigma de programación en el que el flujo del programa viene determinado por eventos.
>- Una entidad publica un evento.
>- Otra entidad lo consume.
>- Permíte procesamiento asíncrono, pero también es posible hacerlo síncrono.

#### Eventos de aplicación
>- Todo evento lanzado en el contexto de una aplicación por una entidad para ser procesada por otra u otras.
>- Input del usuario.
>- Clicks.
>- Input de teclado.
>- Condición que se da en el sistema en un momento concreto.
>- Evento lanzado con el resultado de un procesamiento.
>- Cualquier otra interacción posible.

#### Eventos de aplicación
>- TransferService y AlertService se configuran para escuchar el evento TransferCreated
>- AccountController publica el evento TransferCreated cuando le llega una transferencia.
>- El Event Publisher busca las entidades suscritas a ese evento y se lo emite.
>- TransferService realiza la transferencia.
>- AlertService comprueba que el importe es alto y emite una alerta.

### 26. Ejemplo práctico de Event Driven Programming
 
### 27. Pros y Contras Event Driven Programming

#### Aspectos positivos
>- Desacople entre partes publicadoras y consumidoras del evento
>- Flexibilidad, es muy sencillo añadir o eliminar consumidores sin modificar el productor.
>- Proceso asíncrono sencillo, sin la necesidad de gestionar hilos.
>- Al estar las partes más desacopladas, puede ser más sencillo de testear.

#### Aspectos negativos
>- Es más complicado seguir el flujo.
>- Tarea de debug más dificil.
>- Añade la complejidad del Event Publisher.
>- Mitigado usando frameworks como .NET o Spring.

#### Cuándo usar
>- Cuando en el futuro probablemente necesitemos más entidades que procesen el mismo evento.
>- Necesidad de operaciones asíncronas.
>- Cuando la parte productora no necesite el resultado de la parte que escucha y procesa el evento.

### 28. Event Driven Architecture
1. ¿Que es la Event Driven Architecture?
>- Patrón de arquitectura software en el que el flujo de información entre los distintos subsistemas viene determinado por eventos.
>- Un componente o subsistema publica un evento.
>- Otro lo consume.
>- Muy utilizado en microservicios.

2. Comunicación a través de mensajes
>- Un servicio se subscribe a los eventos que quiere escuchar.
>- El otro servicio publica los eventos.
>- El event manager redirige los eventos a los consumidores.
>- Desacople total entre los dos servicios.
>- Procesamiento asíncrono.

### 29. Introducción a los Microservicios
#### ¿Qué son los microservicios?
>- La arquitectura de microservicios proporciona una serie de prácticas, organización de trabajo y de equipos para construir software complejo de forma más eficiente, rápida y a gran escala.
>- ¡No tiene que ver con la tecnología! La arquitectura de microservicios es agnóstica de la tecnología que se usa para implementar la solución.

#### Ciclo de vida
1. Análisis de requisitos. -> Diseño. -> Implementación. -> Pruebas. -> Despliegue y mantenimiento. -> Análisis de requisitos.
>- Análisis de requisitos.
>- Diseño.
>- Implementación.
>- Pruebas.
>- Despliegue y mantenimiento.
>- Análisis de requisitos.

#### Solución monolítica
1. Un único componente para todo el sistema.
>- Repositorio de código único.
>- Base de datos única
>- Despliegue único de todo el sistema.
>- La tecnología se mantiene desde el inicio al fin.

2. Según va creciendo el sistem, aumentan los tiempos en mantenimiento.
>- Más complicado integrar nuevas funcionalidades al código ya existente.
>- Aparición de más bugs.
>- Mantenimiento más costoso y complicado en general.

3. Dividimos el sistema en contextos cerrados.
>- Creamos un microservicio para cada contexto.

4. Micro en microservicios se refiere al alcance de las funcionalidades.
>- No hay estándar para lo grandes que deben ser. Deben hacer una cosa bien.

5. Cada microservicio vivirpa de forma independiente a los demás.
>- Equipo propio.
>- Repositorio de código propio.
>- Base de datos propia.
>- Cada uno elige las tecnologías más apropiadas para su caso.
>- Deben ser desplegables de forma independiente.

#### Comunicación entre microservicios
1. Importante la buena comunicación entre equipos dependientes.
>- Dejar claras las necesidades de tu equipo.
>- Poner sobre el papel las restricciones, en caso de existir.

2. Métodos de comunicación
>- API Rest
>- Sistema de mensajes. Event Driven Architecture

### 30. Elementos de los Microservicios

#### Antipatrón compartir base de datos entre microservicios

#### Nunca compartir base de datos
1. Los microservicios dejan de ser independientes.
>- No se pueden desarrollar de forma independiente.
>- No se pueden desplegar de forma independiente
>- No se pueden escalar independientemente

2. Encapsulación de los datos inexistente
>- Un microservicio podría modificar la información que no le corresponde.
>- Con BBDD independientes forzamos a realizar la operación a través del microservicio dueño de esos datos.

#### Sincronización de los datos
1. Bajo demanda
>- Un servicio solicita a otro la información sobre sus entidades cuando le sea necesario. Ej. Pedido solicita la dirección al Usuario al completar el pedido.
>- De nuevo, se pierde la independencia entre los microservicios.
2. Utilizando sistema de mensajes
>- Un microservicio publica un evento cuando sus datos han sido modificados.
>- El resto de microservicios a los que le interese el evento lo consume y actualiza la información. Ej. Usuario lanza un evento cuando la dirección se actualiza.

#### Comunicación entre microservicios
1. API Rest.
>- Simple, pero servicios acoplados.
>- Ambos tienen que estar disponibles para que la comunicación funcione.
>- Suele ser síncrono por defecto.

2. Sistema de mensajes
>- Kafca, RabbitMQ, ActiveMQ etc.
>- Desacople total entre los dos servicios.
>- Procesamiento asíncrono.
>- Si un sistema no está disponible, el mensaje permanecerá en la cola hasta que vuelva a estar disponible, momento en el cual será consumido.

#### Interfaz de usuario
>- La organización de la interfaz de usuario es un tema complejo utilizando microservicios. Hay tres formas principales de hacerlo.

1. Interfaz gráfica común.
>- Interactúa con una capa que integra todos los microservicios.

2. Interfaz gráfica que enlaza a los micrositios.
>- Cada microservicio implementa su conjunto de páginas, en caso de tener.

3. Utilización de fragmentos incorporados en una interfaz general.
>- Fragmentos de múltiples microservicios pueden componer una única página.

### 31. Servicios Distribuidos y Despliegue

#### Escalabilidad y disponibilidad
1. Escalando nuestro sistema conseguimoos mayor disponibilidad.
2. Escalabilidad vertical
>- Necesidad de mayor potencia en un nodo.
>- Tareas pesadas, que necesitan mucha memoria etc.
3. Escalabilidad horizontal
>- Mayor capacidad de procesamiento paralelo. Procesamos más peticiones en el mismo tiempo.
>- Eliminamos puntos únicos de fallo.

#### Punto único de fallo
>- Pieza que si falla por cualquier motivo el sistema entero deja de funcionar.
>- Intentar que los puntos únicos de fallo sean los menores posibles.
>- Los que existan, que sean muy robustos.

#### Servicios distribuidos - interacción http
1. Despliegue en múltiples máquinas, las cuales pueden ser dinámicas.
>- ¿Donde reside el servicio que quiero llamar?
2. Múltiples instancias del mismo servicio.
>- ¿A cual de ellos realizo la petición?

#### Múltiples máquinas - interacción por mensajes
1. No existe este problema.
2. Los microservicios no necesitan saber nada de los demás.
>- Se subscriben a los eventos que les interesean.
>- Publican los eventos necesarios.
3. El servicio de mensajes también es un punto único de fallo.

#### Múltiples instancias - interacción por mensajes
>- Tampoco existe este problema.
>- El mensaje será procesado por la primera instancia del servicio que se encuentre libre.
>- Si una instancia está sobrecargada, no va a consumir eventos.

### 32. Seguridad y Monitorización en los Microservicios

#### Autenticación

#### Monitorización
1. Logging
>- Loggear de forma clara la información deseada.
>- Distintos niveles (debug, info, warn, error).

2. Plataformas de monitorización centralizada.
>- New Relic.

### 33. Ejemplo Práctico Microservicios
>- sh start.sh
>- docker images
>- docker ps
>- ya levantados todos luego de ejecutar start.sh
>- docker run cc5e585fb2e3
>- docker run ea58c5898689
>- docker run 39a56c2f2f8e

### 34. Pros y Contras de los Microservicios

#### Aspectos positivos
1. División del sistem en subsistemas más manejables.
>- El código será más fácil de mantener.

2. Independencia real entre equipos. Cada uno es dueño de su microservicio.
3. Posibilidad de realizar escalado y optimización independiente.
>- Menor coste, empezamos con menos recursos y escalamos cuando sea necesario.
4. Despliegue independiente. Si falla un microservicio, el resto podría seguir funcionando.
5. Elección de la tecnología apropiada para cada microservicio.

#### Aspectos negativos
1. Cooperación entre distintos equipos para los puntos en común entre microservicios.
2. Más complejo en general que una solución monolítica.
>- Necesidad de identificar correctamente los subdominios.
>- Test en las fronteras entre microservicios.
>- Despliegue del sistema completo.
>- Seguridad.
3. Interfaz de usuario.
>- Si es única, se puede volver un monolito difícil de mantener, y el equipo que la desarrolla puede ser el cuello de botella.
>- Si son varias puede haber problemas en la integración en una única UI.

#### Cuándo usar
>- Sistemas grandes y complejos con subdominios claramente identificables.
>- Disponibilidad de personal para asignar al equipo de cada microservicio.
>- Sistemas de alta disponibilidad en los que necesitemos escalar fácilmente cada pieza.
>- Ahorro de costes.

## Sección 6: Otros Patrones y Arquitecturas

### 35. Introducción al módulo

### 36. Arquitectura Hexagonal

#### Enfoque en el dominio DDD patron de arquitectua
1. Bases en el diseño guiado por el dominio (DDD).
>- Arquitectura de cuatro capas.
2. Intenta aislar aún más el core de nuestro sistema con el exterior.
3. También conocida como arquitectura de puertos y adaptadores.

#### Arquitectura de cuatro capas

#### arquitectura hexagonal
##### Puertos
>- Partes del sistema por las que fluye la información a capas interiores.
>- No representan puertos físicos de comuniación.
>- Interfaces en Java

#### Adaptadores
1. Implementación específica de un puerto.
>- Adaptador Amazon SQS.
>- Adaptador HTTP
>- Adaptador Redis.
2. No debe existir comunicación ente adaptadores.
3. En java son clases que implementan las interfaces que representan los puertos.
4. Deben ser totalmente reemplazables.

#### Servicios de aplicación
>- Capa de aplicación en DDD.
>- Servicios que implementan casos de uso e interactúan con las capas externas.
>- No contienen lógica de dominio

#### Dominio
1. Capa de dominio de nuestro sistema
>- Entidades.
>- Value Objects.
>- Aggregates.
>- Servicios de dominio.

### 37. Ejemplo Práctivo Arquitectura Hexagonal

### 38. Pros y Contras Arquitectura Hexagonal

#### Aspectos positivos
>- Más fácil de testear.
>- Arquitectura mucho más mantenible a largo plazo.
>- Flexibilidad en cuanto a tecnologías externas.
>- Nos permite retrasar al máximo la elección de las tecnologías.

#### Aspectos negativos
1. Arquitectura muy pesada.
>- Muchas clases e interfaces añadidas.
2. Coste de adaptación y mantenimiento.
3. Confuso al aplicar con framework.
>- ¿Se debe considerar al framework como algo externo?

#### Cuándo usar
>- Incertidumbre en las tecnologías externas que se van a utilizar.
>- Proyectos con un tiempo muy largo de vida.
>- Necesidad de una mayor flexibilidad.
>- Equipos relativamente expertos.

### 39. Microkernel Architecture

#### Arquitectura de microkernel
>- Arquitectura que se compone de los siguientes componentes: 
>- El microkernel, componente principal encargado de coordinar.
>- Plug-ins, componentes que aportan funcionalidad y se registran en el microkernel.
>- Por eso es conocida también como arquitectura de plug-ins.

#### Microkernel y plug-ins
1. Microkernel
>- Aporta la funcionalidad mínima para que el sistema se ejecute.
>- Guarda un registro de los plug-ins que están conectados al sistema.
>- Canal de comunicación entre plug-ins

2. Plug-ins
>- Aportan funcionalidad extra al sistema.
>- No pueden vivir por si mismos.

#### Aspectos positivos
>- Más fácil de testear.
>- Más fácil de mantener a largo plazo que una arquitectura monolítica.
>- Flexibilidad para añadir o eliminar plug-ins, permitiendo así una personalización del sistema según las necesidades.

#### Aspectos negativos
1. Necesita un análisis previo.
>- ¿Qué funcionalidades introducimos al microkernel?
>- ¿Que plug-ins tenemos? ¿Cuán grandes deben ser los plug-ins?
>- ¿Existe comunicación entre plug-ins?¿Mecanismo de comunicación?

2. No demasiado apto para arquitecturas web
>- Los microservicios son una mejor opción.

#### Cuándo usar
>- Aplicaciones de escritorio que necesiten el concepto de plug-ins.
>- Necesidad de un sistema escalable.
>- Sistemas con un tiempo de vida largo.

### 40. Arquitectura Testable

#### Despliegues rápidos y fiables
>- Análisis de requisitos -> Diseño -> Implementación -> Prruebas -> Despliegue y mantenimiento -> Análisis de requisitos
>- Análisis de requisitos 
>- Diseño 
>- Implementación 
>- Prruebas 
>- Despliegue y mantenimiento 
>- Análisis de requisitos
>- No basta con un despliegue rápido, debemos hacer despliegues fiables.

#### Tests unitarios
1. Objetivo: Probar los métodos públicos de una clase de forma aislada.
2. Mockear dependencias.
3. Buscar una cobertura alta (+90%)
4. Probar las distintas condiciones.

#### Tests de integración
1. Objetivo: Probar tu software con BBDD o librerias externas.
2. Desplegar BBDD real para los tests de integración.
>- Testcontainers, Docker.
3. Probar el código que use librerías externas.

#### Tests de contrato
1. Objetivo: Comprobar que las interfaces entre dos servicios se mantienen correctas.
2. Muy común en arquitecturas de microservicios.
3. Se prueban ambas partes de la comunicación.
>- Productor
>- Consumidor

#### Test de UI
1. Objetivo: Comprobar que la interfaz de usuario se mantiene como esperamos.
2. Distinto de los tests de sistema o e2e.
3. Se puede probar la interfaz mockeando el backend, por ejemplo.
>- Angular, react, vue.
>- Jest, jasmine, mocha

#### Tests de final a final (E2E)
1. Objetivo: Probar todo nuestro sistema.
2. Pueden implicar tests de UI, pero no tiene por qué.
3. Se prueba el sistema desde el punto de entrada al lugar donde se reflejan los resultados.
4. Selenium, cypress

#### Tests de aceptación
1. Objetivo: Comprobar las funcionalidades de nuestra aplicación.
2. Se centran en los casos de uso en concreto.
3. Sintaxis given-when-then.
4. Herramientas BDD como Cucumber.

#### Tests exploratorios
1. Objetivo: Probar manualmente el sistema en busca de problemas.
2. Ni los mejores tests automáticos son perfectos
>- Nos podemos olvidar de ciertos casos.
>- Bugs en nuestros tests.
3. Probar manualmente intentando romper la aplicación.

### Evolving y Sacrificial Architectures.

#### Evolving y Sacrificial Architectures - Arquitectura que Evoluciona
1. Una buena arquitectura debe ser flexible.
>- No importa la arquitectura que se elija: monolítica, DDD, CQRD, microservicios etc.
2. Una buena arquitectura nos debe dejar tomar decisiones en el mejor momento posible.

#### Sacrificial Architecture
1. La mayoría de código que estás escribiendo ahora se desechará antes de dos o tres años.
2. No abandonar la calidad del diseñor y del código.
>- Nos traerá problemas mucho mayores rápidamente.
3. Arquitectura modular.
>- Permitir desechar un módulo o componente afectando lo menor posible al sistema.
4. Equilibrio entre una buena arquitectura / calidad de código y el hecho de que el código tiene fecha de caducidad a medio plazo.

### 42. Conclusión del Curso

#### Arquitecturas convencionales
1. Puntos clave
>- Monolitos y centradas en los datos.
>- Sin capas o tres capas típica. Presentación, lógica de negocio y acceso a datos.
>- Desarrollo rápido al inicio y fácil adaptación.
>- Difícil de mantener y evolucionar a largo plazo.
>- Proyectos con corto tiempo de vida.

#### Domain Driven Design
1. Puntos clave.
>- Centrado en el dominio del problema.
>- Lenguaje ubicuo, contextos acotados y mapeo de contextos.
>- Surge una nueva capa, la de dominio. Entidades + Servicios de Dominio.
>- Desarrollo mucho más rápido a largo plazo. Mantenible y evolucionable.
>- Lento al principio. Difícil adaptación. Necesario tener expertos de dominio.
>- Proyectos con largo tiempo de vida y con problemas con un dominio rico.

#### Command Query Responsibility Segregation
1. Puntos clave.
>- Tratamiento independiente de lecturas y escrituras
>- Posibilidad de tener dos Bases de Datos.
>- Mejora con Event Sourcing
>- Optimización de lecturas y escrituras.
>- Gran complejidad y sincronización
>- Proyectos dónde el rendimiento sea algo crítico.

#### Event Sourcing
1. Puntos clave
>- Almacenamiento de eventos en lugar de estado actual.
>- El estado actual se consigue ejecutando todos los eventos.
>- Muy útil con CQRS.
>- Trazabilidad del estado del sistema en el tiempo.
>- Eficiencia en lecturas y mayor complejidad.
>- Proyectos dónde se use CQRS o se necesite un log de las acciones.

#### Event Driven Programming
1. Puntos clave
>- Interacción mediante eventos en lugar de llamadas directas a métodos.
>- Desacople entre parte productora del evento y la consumidora.
>- Flexibilidad para añadir más consumidores del evento sin modificar nada.
>- Mayor complejidad general.
>- Cuando en el futuro se necesiten más consumidores. Procesos asíncronos.

#### Microservicios
1. Puntos clave.
>- División del dominio en subdominios. Cada uno será un microservicio.
>- Viven de forma independiente.
>- Agnósticos de la tecnología.
>- Sistemas más manejables y escalado independiente en cada microservicio.
>- Cooperación entre equipos e interfaz de usuario
>- Sistemas en los que necesitemos una alta disponibilidad.

#### Arquitectura Hexagonal
1. Puntos clave.
>- Aislar aún más el core de nuestro sistema.
>- Puertos y adaptadores.
>- Fácil de testear y muy flexible.
>- Arquitectura pesada y confusa al aplicar con frameworks.
>- Incertidumbre en las tecnologías que se van a utilizar.

#### Arquitectura de microkernel
1. Puntos clave
>- Componente con funcionalidad básica, microkernel.
>- Componentes que ofrecen la funcionalidad, plug-ins.
>- Flexibilidad y personalización de nuestro sistema.
>- Necesidad de un gran análisis previo. No demasiado apto para web.
>- Sistemas en los que el concepto de plug-in sea de utilidad.

#### El software no es una ciencia exacta
1. El mayor profesor es la experiencia.
>- Prueba y error.

2. La arquitectura se debe adaptar al problema y al equipo, no al revés.
>- No sigas al 100% la teoría aunque veas que no se ajusta del todo bien a tu caso particular. Toma los detalles que si lo hagan.

3. Lo más importante es ser flexible y estar abierto al cambio cuando sea necesario.
