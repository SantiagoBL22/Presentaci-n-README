# Taller de Salesforce Administrador - ProContacto RRHH
Este repositorio contiene los pasos y respuestas para el taller de Analista Salesforce proporcionado por ProContacto RRHH.
## Preguntas sobre HTTP
### ¿Qué es un servidor HTTP?
Un servidor HTTP es un software que procesa las solicitudes de los clientes y entrega los recursos solicitados, que generalmente son páginas web. El servidor escucha las solicitudes en un puerto específico (por defecto, el puerto 80 para HTTP y el puerto 443 para HTTPS) y responde con los datos apropiados.

### ¿Qué son los verbos HTTP?
Los verbos HTTP, también conocidos como métodos HTTP, indican la acción a realizar sobre el recurso especificado. Los verbos más comunes son:
- **GET**: Solicita la representación de un recurso específico, las peticiones que usan el método GET solo deben recuperar datos.
- **POST**: Se usa para enviar datos al servidor para crear o actualizar un recurso.
- **PUT**: Se usa para enviar datos al servidor para actualizar un recurso existente.
- **DELETE**: Se usa para eliminar un recurso específico.
- **PATCH**: Se usa para aplicar modificaciones parciales a un recurso.
- **HEAD**: Similar a GET, pero solo solicita los encabezados de la respuesta.
- **OPTIONS**: Describe las opciones de comunicación para el recurso de destino.

### ¿Qué es un request y un response en una comunicación HTTP?
- **Request**: Una solicitud HTTP enviada por el cliente (generalmente un navegador web) al servidor. Contiene información sobre qué recurso se está solicitando y cómo se debe procesar la solicitud.
- **Response**: La respuesta HTTP enviada por el servidor al cliente. Contiene el estado de la solicitud y los datos solicitados o un mensaje de error si la solicitud no se pudo completar.

### ¿Qué son los headers?
Los headers (encabezados) son componentes de las solicitudes y respuestas HTTP que transportan información adicional sobre la petición o la respuesta. Por ejemplo:
- **Content-Type**: Indica el tipo de contenido que se está enviando o recibiendo (e.g., `application/json`).
- **Authorization**: Contiene credenciales para autenticar al cliente con el servidor.
- **Cache-Control**: Instrucciones para el almacenamiento en caché del contenido.
  
### ¿Qué es un queryString?
Un queryString es una parte de la URL que contiene datos para ser enviados al servidor dónde se encuentra después del símbolo `?` y consiste en pares de clave-valor separados por `&`.

### ¿Qué es el responseCode?
El responseCode o código de respuesta es un código numérico devuelto por el servidor para indicar el resultado de la solicitud dentro de los cuales encontramos:
- **200 OK**: La solicitud fue exitosa.
- **201 Created**: La solicitud fue exitosa y se creó un nuevo recurso.
- **400 Bad Request**: La solicitud es inválida o malformada.
- **401 Unauthorized**: Autenticación requerida o fallida.
- **404 Not Found**: El recurso solicitado no fue encontrado.
- **500 Internal Server Error**: Error interno del servidor.

### ¿Cómo se envía la data en un GET y en un POST?
- **GET**: La data se envía como parte de la URL, a través de query strings.
- **POST**: La data se envía en el cuerpo del request, lo que permite enviar información más grande y estructurada.

### ¿Qué verbo HTTP utiliza el navegador cuando accedemos a una página?
El navegador utiliza el verbo GET para solicitar una página web.

### JSON y XML
- **JSON (JavaScript Object Notation)**: Un formato de texto ligero para el intercambio de datos. Ejemplo:
  ```json
  {
    "name": "John",
    "age": 30,
    "city": "New York"
  }
- **XML (eXtensible Markup Language)**: Un lenguaje de marcado que define un conjunto de reglas para codificar documentos en un formato legible tanto por humanos como por máquinas. Ejemplo:
  ```xml
   {
    <person>
    <name>John</name>
    <age>30</age>
    <city>New York</city>
    </person>
    }

### Explicación de SOAP y REST
- **SOAP (Simple Object Access Protocol)**: Un protocolo basado en XML para intercambiar información en la implementación de servicios web. SOAP define una estructura estricta para los mensajes y se utiliza sobre varios protocolos de red, como HTTP y SMTP.
- **REST (Representational State Transfer)**: Un estilo de arquitectura para diseñar servicios web que utiliza HTTP y se centra en los recursos, cada uno identificado por una URL. Los servicios RESTful utilizan verbos HTTP para realizar operaciones sobre los recursos.

## Ejercicio Postman
- De acuerdo con el ejercicio relizado en POSTMAN, se evidencia que al realizar el primer GET en la URL trae una sería de nombres con emails prefedefinido, y cuando se ejecuta el POST y nuevamete se llama a la URL, se logra evidenciar que se inserta el nuevo dato (Nombre y apellido con correo) en el formto json:

![Captura de pantalla 2024-07-01 174231](https://github.com/SantiagoBL22/Taller-de-Salesforce-Administrador---ProContacto-RRHH/assets/174379337/68305332-0bb3-4515-9aca-79f41b124d9f)

## Ejercicio Trailmix
- Perfil usuario Trailhead: https://www.salesforce.com/trailblazer/sbolivarleal

## Ejercicio Salesforce
### Objetos Clave

- **Lead**: Un potencial cliente que ha mostrado interés en tus productos o servicios en dónde se almacena información como nombre, empresa, correo electrónico y teléfono.
- **Account**: Una empresa o entidad con la que haces negocios en la que se almacena información como nombre de la cuenta, dirección, industria y número de empleados.
- **Contact**: Una persona asociada a una cuenta y almacena información como nombre, título, correo electrónico y teléfono.
- **Opportunity**: Una posible venta o transacción en proceso. Almacena información como nombre de la oportunidad, valor, etapa de la venta y fecha de cierre.
- **Product**: Un artículo que vendes. Almacena información como nombre del producto, código, descripción y precio.
- **PriceBook**: Una lista de precios para tus productos. Almacena información como nombre del price book y los productos asociados con sus precios.
- **Quote**: Una propuesta de precios para un cliente. Almacena información como nombre del quote, productos y precios.
- **Asset**: Un producto que un cliente ha comprado. Almacena información como nombre del asset, número de serie, fecha de compra y estado.
- **Case**: Un problema o incidencia reportada por un cliente. Almacena información como número del caso, descripción, estado y prioridad.
- **Article**: Información almacenada en la base de conocimientos. Almacena información como título del artículo, contenido y categorías.

- **¿Qué es Salesforce?**
  Salesforce es una plataforma de gestión de relaciones con el cliente (CRM) basada en la nube que permite a las empresas gestionar sus ventas, servicios y marketing. Ofrece una suite de aplicaciones diseñadas para ayudar en la gestión de relaciones con los clientes y la automatización de procesos empresariales.

- **¿Qué es Sales Cloud?**
  Sales Cloud es una parte de Salesforce que se enfoca en las ventas. Permite a las empresas gestionar su proceso de ventas, desde la captación de leads hasta el cierre de oportunidades. Incluye herramientas para la gestión de contactos, cuentas, oportunidades, y permite el seguimiento y análisis del rendimiento de ventas.

- **¿Qué es Service Cloud?**
  Service Cloud es una solución de Salesforce que permite a las empresas gestionar su servicio al cliente. Ofrece herramientas para la gestión de casos, la automatización del servicio, el soporte omnicanal y una base de conocimientos. Ayuda a mejorar la eficiencia del servicio al cliente y la satisfacción del cliente.

- **¿Qué es Health Cloud?**
  Health Cloud es una solución de Salesforce diseñada específicamente para la industria de la salud. Permite a los profesionales de la salud gestionar las relaciones con los pacientes, coordinar la atención y mejorar los resultados de los pacientes. Incluye herramientas para la gestión de historiales médicos, la coordinación de la atención y el análisis de datos de salud.

- **¿Qué es Marketing Cloud?**
  Marketing Cloud es una plataforma de marketing digital que permite a las empresas gestionar y automatizar sus campañas de marketing. Ofrece herramientas para la personalización, la automatización de campañas, el email marketing, las redes sociales y el análisis de datos de marketing.

### Funcionalidades y Conceptos de Salesforce

- **RecordType**: Permite personalizar diferentes tipos de registros dentro de un objeto. Por ejemplo, un objeto "Cuenta" puede tener diferentes tipos de registros para "Clientes" y "Proveedores", cada uno con sus propios campos y valores predeterminados.

- **ReportType**: Es una plantilla que define los objetos y campos que se pueden usar en un informe. Por ejemplo, un tipo de informe de "Cuentas con Contactos" permite crear informes que incluyen datos de ambos objetos.

- **Page Layout**: Define la disposición de los campos, botones, enlaces y componentes relacionados en la página de un registro. Ayuda a personalizar la experiencia del usuario y a mostrar solo la información relevante.

- **Compact Layout**: Define un conjunto mínimo de campos que se muestran en una vista compacta, como en las tarjetas de registro de una lista o en una vista móvil.

- **Perfil**: Define los permisos de acceso y las capacidades de los usuarios en Salesforce. Cada usuario tiene un perfil que determina a qué objetos y campos pueden acceder y qué acciones pueden realizar.

- **Rol**: Define la jerarquía de acceso a los datos. Los roles ayudan a determinar qué datos son visibles para los usuarios en función de su posición en la jerarquía de la empresa.

- **Validation Rule**: Son reglas que se utilizan para verificar que los datos introducidos en un campo cumplen ciertos criterios antes de que el registro pueda ser guardado. Ayudan a mantener la calidad de los datos.

- **Master Detail vs. Lookup**:
  - **Master Detail**: Es una relación estrecha entre dos objetos en la que un registro hijo no puede existir sin un registro padre. El registro hijo hereda la propiedad y la seguridad del registro padre.
  - **Lookup**: Es una relación más flexible que permite que un registro hijo se relacione con un registro padre, pero el registro hijo puede existir independientemente del registro padre.

- **Sandbox**: Es una copia del entorno de producción utilizada para desarrollo, pruebas y capacitación. Las sandboxes permiten hacer cambios y probar nuevas configuraciones sin afectar los datos en producción.

- **ChangeSet**: Es una colección de componentes que se pueden desplegar de un entorno de Salesforce a otro. Se utiliza para mover configuraciones y personalizaciones entre diferentes entornos.

- **Import Wizard**: Herramienta que facilita la importación de datos a Salesforce desde archivos CSV. Permite la importación de cuentas, contactos, leads, soluciones y registros personalizados.

- **Web to Lead**: Funcionalidad que permite capturar información de leads desde un formulario web y crear registros de leads en Salesforce automáticamente.

- **Web to Case**: Funcionalidad que permite capturar información de casos desde un formulario web y crear registros de casos en Salesforce automáticamente.

- **Omnichannel**: Herramienta que permite a las organizaciones gestionar interacciones con los clientes a través de múltiples canales (chat, correo electrónico, teléfono, redes sociales) desde una única plataforma.

- **Chatter**: Herramienta de colaboración que permite a los empleados comunicarse y compartir información dentro de Salesforce. Incluye funcionalidades de redes sociales como la creación de publicaciones, comentarios y seguimientos.

## Conceptos Generales de Salesforce

### ¿Qué significa SaaS?
SaaS (Software as a Service) es un modelo de distribución de software donde las aplicaciones se alojan en la nube y son accesibles a través de Internet. En lugar de instalar y mantener software, los usuarios acceden a él a través de la web, generalmente mediante una suscripción.

### ¿Salesforce es SaaS?
Sí, Salesforce es un ejemplo de SaaS. Ofrece aplicaciones CRM (Customer Relationship Management) basadas en la nube que permiten a las empresas gestionar sus relaciones con los clientes sin necesidad de infraestructura local.

### ¿Qué significa que una solución sea Cloud?
Una solución Cloud significa que los recursos, como almacenamiento y procesamiento, se proporcionan a través de Internet desde servidores remotos. Las soluciones en la nube permiten acceso desde cualquier lugar con conexión a Internet, eliminando la necesidad de hardware local.

### ¿Qué significa que una solución sea On-Premise?
Una solución On-Premise es un software instalado y ejecutado en los servidores propios de una empresa, dentro de su infraestructura física. Requiere inversión en hardware y mantenimiento por parte de la empresa.

### ¿Qué es un pipeline de ventas?
Un pipeline de ventas es una visualización del proceso de ventas, desde el contacto inicial con un cliente potencial hasta el cierre de la venta. Ayuda a los equipos de ventas a gestionar y prever sus actividades y oportunidades.

### ¿Qué es un funnel de ventas?
Un funnel de ventas (embudo de ventas) es un modelo que representa las etapas por las que pasan los clientes potenciales, desde el conocimiento del producto hasta la compra. Las etapas típicas incluyen conocimiento, interés, decisión y acción.

### ¿Qué significa Customer Experience?
Customer Experience (CX) es la percepción general que los clientes tienen de una empresa basada en todas sus interacciones a lo largo del tiempo. Una buena experiencia del cliente puede mejorar la lealtad y satisfacción del cliente.

### ¿Qué significa omnicanalidad?
La omnicanalidad es una estrategia de marketing y servicio al cliente donde todas las interacciones y canales de comunicación (como tiendas físicas, online, redes sociales, etc.) están integrados para proporcionar una experiencia de cliente coherente y fluida.

### ¿Qué significa que un negocio sea B2B? ¿Qué significa que un negocio sea B2C?
- **B2B (Business to Business)**: Un negocio B2B vende productos o servicios a otras empresas.
- **B2C (Business to Consumer)**: Un negocio B2C vende productos o servicios directamente a los consumidores.

### ¿Qué es un KPI?
KPI (Key Performance Indicator) es una métrica utilizada para evaluar el rendimiento de una actividad o proceso en relación con un objetivo específico. Los KPIs ayudan a medir el éxito y la eficiencia de las operaciones empresariales.

### ¿Qué es una API y en qué se diferencia de una Rest API?
- **API (Application Programming Interface)**: Es un conjunto de definiciones y protocolos que permite que diferentes aplicaciones se comuniquen entre sí.
- **Rest API**: Es un tipo de API que utiliza el estilo arquitectónico REST (Representational State Transfer). Las Rest APIs son diseñadas para ser simples y ligeras, utilizando métodos HTTP para realizar operaciones (GET, POST, PUT, DELETE).

### ¿Qué es un Proceso Batch?
Un proceso batch es un tipo de procesamiento de datos donde se ejecutan un conjunto de tareas sin intervención del usuario, generalmente programadas para ejecutarse en momentos específicos o bajo ciertas condiciones.

### ¿Qué es Kanban?
Kanban es una metodología de gestión de proyectos y flujo de trabajo visual que utiliza tarjetas y tableros para representar tareas y su progreso. Ayuda a visualizar el trabajo, limitar el trabajo en progreso y maximizar la eficiencia.

### ¿Qué es un ERP?
ERP (Enterprise Resource Planning) es un software de gestión empresarial que integra y automatiza muchos de los procesos de negocio relacionados con operaciones, producción y distribución. Un ERP centraliza la información y permite su acceso en tiempo real.

### ¿Salesforce es un ERP?
No, Salesforce no es un ERP. Salesforce es una plataforma CRM que se enfoca en gestionar las relaciones con los clientes y la automatización de ventas, marketing y servicio al cliente, sin embargo, puede integrarse con sistemas ERP para proporcionar una solución más completa.



