
## cursos
>- https://udemy.com/course/microservicios-con-spring-boot-y-spring-cloud/learn/lecture/15365312#overview

## Sección 1: Introducción al curso


### 1. Introducción

#### componentes de un microservicio
>- Autónomos
>- Especializados
>- Registro y auto-descubrimiento de servicios
>- Escalado flexible
>- Tolerancia a fallos
>- Balanceo de cargas
>- Configuración centralizada
>- Libertad tecnológica
>- Agilidad y equipos más pequeños
>- Ciclo de desarrollo más cortos
>- Código reutilizable

#### Componentes que veremos en el curso
>- Spring Boot
>- Spring IoC
>- Spring Data JPA e Hibernate
>- API REST
>- Spring Cloud
>- Servidor Eureka Netflix
>- Eureka Client
>- RestTemplate
>- Feign
>- Ribbon
>- Hystrix
>- Gateway Zuul
>- Spring Security OAuth2
>- JWT


### 2. Antes de comenzar


### 3. Herramientas necesarias


### 4. Instalación del Spring Tools Suite IDE
>- 

## Sección 2: Microservicios: la base

### 5. Introducción a los microservicios

#### ¿Qué son? Los microservicios
>- En pocas palabras, son un conjunto de componentes pequeños y autónomos que colaboran entre si

#### Características
>- Función única
>- Independientes
>- Registro y auto-descubrimiento de servicios
>- Auto escalado y agilidad
>- Confiabilidad y tolerancia a fallos
>- Balanceo de cargas

#### Ventajas
>- Nueva tecnología y adopción de procesos
>- Reducción de costo
>- Ciclos de liberación más rápidos
>- Equipos de desarrollo más pequeños


### 6. Actualización: Wizard para seleccionar dependencias en Spring Tools IDE
>- Spring Boot DevTools
>- Spring Web Starter

### 7. Creando nuestro microservicio productos
>- DevToolS
>- Web
>- JPA


### 8. Añadiendo la clase Entity Producto

### 9. Creando el repositorio JPA para los productos

### 10. Creando el compoenente service para los productos

### 11. Creando el controlador rest productos

### 12. Probando nuestra API productos con Postman

### 13. Creando microservicio items

### 14. Creando componente service en items para consumir API productos

### 15. Implementando componente service con cliente HTTP RestTemplate

### 16. Creando controlador en items

### 17. Usando cliente REST de Feign para consumir nuestra API productos

### 18. Balanceo de carga del lado del cliente con Ribbon

### 19. Probando balanceo de carga en postman

### 20. Utilizando Ribbon para balanceo de carga en RestTemplate

### 21. Descargar Código Fuente

## Sección 3: Eureka Server: registrando microservicios

### 22. Creando servidor de registro Eureka

### 23. Conectado nuestro servicios como clientes

### 24. Escalar microservicios con puerto dinámico

### 25. Tolerancia de fallos y latencia con Hystrix

### 26. Configurando timeout en Hystrix y Ribbon

### 27. Creando yy configurando servidor Zuul API Gateway
>- puedes hacer las peticiones en los endpoints sin enviar el bearer token
>- 


### 28. Zuul Filtro HTTP pre - Tiempo transcurrido

### 29. Zuul HTTP post - Tiempo transcurrido

### 30. Configurando timeout de Zuul API Gateway

### 31. Descargar Código Fuente

## Sección 4: Spring Cloud Gateway

### 32. Introducción a Spring Cloud Gateway
>- Zuul Netflix y Spring Cloud Gateway
>- Puerta de enlace, acceso centralizado
>- Enrutamiento dinámico de los microservicios
>- Balanceo de carga
>- Maneja filtros propios
>- Permite extender funcionalidades




### 33. Creando y configurando servicio Spring Cloud Gateway

### 34. Configuración de rutas usando application.properties y application.yml

### 35. Implementando filtros globales pre y post

### 36. Modificando el request en el filtro pre

### 37. Implementando Gateway Filter Factory

### 38. Configurando y probando nuestro Gateway Filter Factory personalizado

### 39. Filtros Gateway Factory que vienen de fabrica

### 40. Request Predicates Factory que vienen de fábrica

### 41. Descargar Código Fuente

## Sección 5: Resilience4J: Resiliencia y tolerancia a fallos

### 42. Introducción a Circuit Breaker (Cortocircuito)

### 43. Configurando microservicio items con Resilience4J

### 44. Simulando fallas y latencia en el microservicio items

### 45. Probando Resilience con los criterios por defecto

### 46. Personalizando parámetro del Circuit Breaker

### 47. Timeout

### 48. Llamadas lentas

### 49. Configurando Resilience4J en el application.yml

### 50. Configurando Resilience4J useando application.properties y application.yml

### 51. La anotación @CircuitBreaker

### 52. La anotación @TimeLimiter

### 53. Asunto con el fallbackMethod usando anotaciones @CircuitBreaker y @TimeLimiter

### 54. Spring Cloud Gateway con Resilience4J

### 55. [Opcional] Modificar el order en el filtro EjemploGlobalFilter en caso de error

### 56. Descargar Código Fuente

## Sección 6: Spring Cloud Config Server: centralizando la configuración

### 




































