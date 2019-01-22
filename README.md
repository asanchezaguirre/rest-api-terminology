# REST API Terminology 

Fork and clone this repository. Then, push to github with all bad answers deleted and only the correct answers showing.

**1. What does it mean REST?**
REST, significa Representational State Transfer. Es un estilo arquitectónico o conjunto de principios de diseño, para proporcionar estándares que hagan que la comunición en red sea màs escalable y flexible.


**2. Who coined the REST term?**
Roy T. Fielding

**3. In which protocol REST is based?**
HTTP


**4. What are the main building blocks of a REST Architecture?**

Resources (URIs)
Respuesta de recurso
Representaciones
Mensajes que describen operación
Hipermedia


((Un servicio web son protocolos para intercambiar datos a través de la red))

**5. Identifying a resource is easy; you know how to access it and you even know how to request for a specific format. Since REST is using HTTP protocol as a standing point, there are some actions related to resources: CRUD operations.**

Complete the below table:+


|HTTP Verb|Proposed Action            
|---------|---------------            
|GET      |recupera un recurso específico por id (get)                    
|POST     |crea un nuevo recurso   (create)                      
|PUT      |actualiza un recurso específico por id (update)                     
|DELETE   | elimina un recurso específico por id   (delete)    



**6. Status Code**

Another interesting standard that REST can benefit from when based on HTTP is the usage of HTTP status codes.

+ What’s is a status code?
Los códigos de estado HTTP son códigos de respuesta estándar dados por los servidores de sitios web en Internet. Los códigos ayudan a identificar la causa del problema cuando una página web u otro recurso no se carga correctamente.


+ Explain with your own words, the meaning of next codes:

|Status Code|Description|
|-----------|-----------
|404        |  la pàgina no se pudo encontrar en el servidor         
|200        |  es una respuesta exitosa a la solicitud       
|500        |  error del servidor de internet         

**7. Status Code are grouped in five sets.**

Write what are their meaning.

|Group|Description|
|-----|-----------|
|1XX| | es una respuesta informativa que indica que la solicitud fue 
|       recibida y entendida.Se emite de manera provisional
 2XX| | la accion fue recibida, entendida y aceptada
|3XX| |	redirección
 4XX| |	el cliente causó el error
|5XX| |	errores del servidor

**8. HTTP Status Codes and Their Related Interpretation**

There are the most common status codes in HTTP responses. Please, fill with the required description.

|Status Code|Meaning|
|-----------|-------|
|200| |	respuesta exitosa
|201| |	creado
 204| | no contenido			
|301| | lo movieron permanenteemnte
|400| | mala respuesta
|401| |	
|403| | forbiden
|404| |	not found
|405| |	no reload
|500| | internal server error
 
###### [To see the full list of HTTP status codes and their meaning, please refer to the RFC of HTTP 1.1](http://tools.ietf.org/html/rfc7231#section-6)

**9. How are called the points of contact between all client apps and the API?**
endpoints


**10. The following is a good example or bad example of a named access point? And why?**

_meant to list the books in a bookstore_

+ `GET /books/action1`

mal, porque action1 no es descriptivo ni claro, no cumple con las convenciones


**11. Uniform Interface**



To solve this problem, you can apply the REST style to the endpoints, and thanks to HTTP, you also have verbs to indicate actions.

|Old Style|REST Style|
|---------|----------|
|`/getAllBooks`            |   get/books         
|`/submitNewBook`          |   post/books        
|`/updateAuthor`           |   put/authors/:id
|`/getBooksAuthors`        |   get/books/:id/authors
|`/getNumberOfBooksOnStock`|   get/books
|`/addNewImageToBook`      |   post/books/:id/image
|`/getBooksImages`         |   get/books/:id/image
|`/addCoverImage`          |   post/books/:id/image
|`/listBookCovers`         |   get/books/:id



**12. What JSON does it mean?**

javascript object notation

**13. Anatomy of a `REQUEST`**

Make a `curl` request to _GitHub API_

```sh
$ curl https://api.github.com/ --head
```
CURL ES es un proyecto de software informático que proporciona una biblioteca y una herramienta de línea de comandos para transferir datos mediante varios protocolos. Es la manera de solicitar la data


According to the responded request, answer what does it mean the next parts from the handler:

+ _`Content-Type`_. tipo de contenido del cuerpo del mensaje
+ _`Status`_. respuesta dependiendo si la respuesta fue extosa o no
+ _`Date`_. fecha
+ _`Content-Length`_. longitud del contenido


###### If response is not showing those parts, ask to google how to print them in console.

```sh
# 
```
