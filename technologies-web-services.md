# Технологии

1. **SOAP (Simple Object Access Protocol)** - основанный на XML протокол обмена сообщениями.

2. **WSDL (Web Services Description Language)** - язык разметки, основанный на XML, преднзначенный для 
описания веб сервисов.

3. **UDDI (Universal Description, Discovery, and Integration)** - предоставляет всемирный реестр веб сервисов для рекламы, поиска и хранения.

4. Взаимодействие между SOAP, WSDL и UDDI:
	- Приложение играет роль веб сервисов, которые нужны клиенту для доступа к другому приложению или бизнес логике, расположенной где-то в сети. 
	- Клиент делает запрос в UDDI реестр для нахождения сервиса по имени, категории, идентификатору или какой-то другой спецификации. 
	- Как только сервис найден, клиент получает информацию о местонахождении WSDL документа из UDDI реестра. 
	- WSDL документ содержит информацию о том, как обратиться к веб сервису, и формат запросов в XML схему.
	- Клиент создает SOAP сообщение в соответствии с XML схемой, взятой из WSDL, и посылает запрос хосту (где находится веб сервис).

### 1. SOM

1. **SOM (Service-Oriented Model)** сосредаточена на тех аспектах архитектуры, которые относятся к сервису и действиям. <sup>[\[source\]][som]</sup>
	- Главная цель SOM - устанавливать отношения между агентом, сервисом, который он реализует, и запросами.
	- SOM построен на основе MOM, но сосредочен больше на действия, чем на сообщения.

1. **Message** - единица информации, отсылаемая одним агентом другому в конексте веб сервисов. <sup>[\[source\]][message]</sup>

1. **Action** - любое действие, представленное агентом в качестве отклика на получение сообщения, или посылки сообщения, или другого изменения состояния. <sup>[\[source\]][action]</sup>

1. **Service** - набор действий, которые формируют целостную систему с точки зрения провайдеров и реквесторов. <sup>[\[source\]][service]</sup>

1. **Agent** - программа, выполняющая функции, указанные пользователем, сущностью или процессом. <sup>[\[source\]][agent]</sup>
	- Агент представляет программу, выполняющую функции согласно действиям пользователя, сущности или процесса.
	- Агент обладает идентификатором, владельцем (сущностью) и может предоставлять 1 и более сервисов или запрашивать 0 и более сервисов.

1. **Choreography** - определяет очередность и условия, которые позволяют объеденению независимых веб сервисов обмениваться информацией с целью достичь некоторую полезную функцию. <sup>[\[source\]][choreography]</sup>

1. **Choreography Description Language** - нотация для описания хореографии. <sup>[\[source\]][choreography-description-language]</sup>

1. **Service Description** - набор документов, описывающих интерфейс и семантику сервиса. <sup>[\[source\]][service-description]</sup>
	- Описание выражается через XML и обуславливается одним или более стандартами.

1. **Service Operation** - абстрактная группировка сообщений, которую сервис посылает и получает, чтобы совершить определенную задачу. <sup>[\[source\]][service-operation]</sup>

1. **Service Platform** - среда, используемая для хостинга одного или более веб сервисов. <sup>[\[source\]][service-platform]</sup>
	- Она включает в себя один или более SOAP серверов, ни одного или несколько UDDI реестров, защиту и транзакционные сервисы, используемые веб сервисами, которые хостятся на ней, и прочую инфраструктуру.
 
1. **Service Provider** - агент, который способен и предназначен для совершения действий, связанных с сервисом. <sup>[\[source\]][service-provider]</sup>
	- Провайдер предоставляет 1 или более сервисов.
	- Провайдер представляет или вызывает представление действий, связанных с сервисом.

1. **Service Requester** - сущность, которая отвечает за запросы к сервису через провайдер. <sup>[\[source\]][service-requestor]</sup>
	- Реквестор запрашивает 1 или более сервисов.

1. **Service Registry (Broker)** - логически-централизованная директория сервисов, куда девелоперы публикуют новые 
сервисы и где можно найти существующие. Поэтому этот элемент является координационным центром для компаний и их услуг. <sup>[\[source\]][service-registry]</sup>
	- Реестр предоставляет следующего вида информацию: бизнес данные, такие как имя, описание, контактная информация, или данные, необходимые для использования веб сервиса.
 
1. **Service Semantics** - контракт между провайдером и реквестором, который отображает вызов сервиса.  <sup>[\[source\]][service-semantics]</sup>
	- Семантика является обобщением таксов, которые составляют сервис.
	- Семантика может выражаться с помощью языка описания сервиса.

1. **Service Task** - еденица активности, связанная с сервисом. <sup>[\[source\]][service-task]</sup>

***

### 2. ROM

1. **ROM (Resource-Oriented Model)** сосредоточена на тех аспектах архитектуры, которые относятся к ресурсам, и сервис модель которых связана с манипулированием ресурсами. <sup>[\[source\]][rom]</sup>

***

### 3. SOAP

1. **SOAP** - протокол обмена структурированными сообщениями в распределенной вычислительной среде. Также предоставляет стандарт структуры упаковки данных для транспортировки XML документов с помощью различных интернет-технологий, как: SMTP, HTTP, FTP. <sup>[\[source\]][soap]</sup>
	- Так как SOAP обладает стандартным механизмом транспортировки, различные клиенты и серверы могут взаимодействовать, например, с EJB через .NET клиент и наоборот.

2. Пример взаимодействия клиента с Web приложением (регистрация аккаунта):
	- Программа на клиентской стороне конвертирует информацию о регистрации аккаунта в SOAP сообщение.
	- SOAP сообщение отсылается в веб сервис, как тело HTTP POST запроса.
	- Веб сервис распаковывает SOAP реквест и конвертирует в комманду, которую понимает приложение на сервере.
    - Приложение обрабатывает информацию своей логикой и отправляет ответ с новым уникальным номером аккаунта.
    - Следующим шагом, веб сервис конвертирует ответ сервера в SOAP сообщение, которое отправляет назад в клиентское 
    приложение, как ответ на HTTP запрос.
    - Клиентское приложение распаковывает SOAP сообщение и предоставляет клиенту соотвествующую информацию.

3. Клиент/сервер связь:
   ```
                  HTTP POST of SOAP request document
     SOAP: client ----------------------------------> service

           client <---------------------------------- service
	                   SOAP (maybe JSON) document
   ```

4. **SOAP Building Blocks**. SOAP сообщение - это обычный XML документ, содержащий следующие элементы:
	- Оболочка - идентифицирует XML документ как SOAP сообщение.
	- Заголовок - содержит различного рода информацию о сообщении, которая помещается обычно в заголовки.
	- Тело - содержит информацию о вызове и ответе.
	- Ошибка - содержит все ошибки и текущий статус.

***

### 4. WSDL

1. **WSDL (Web Service Description Language)** - XML технология, которая описывает интерфейс веб сервиса в стандартизированном виде. WSDL указывает стандарт, как веб сервис должен представлять входные и выходные параметры при вызове извне, как должна выглядеть структура функции, природа вызова и как осуществлять связывание протокола сервера. <sup>[\[source\]][wsdl]</sup>
   - WSDL позволяет различным клиентам автоматически распознавать, как взаимодействовать с веб сервисом.

1. **WSDL документ** - описывает веб сервис. Он указывает местоположение сервиса и его методы, используя следующие элементы:
    - `<types>` - определяет типы данных, используемые веб сервисом.
    - `<message>` - определяет элементы данных для каждой операции.
    - `<portType>` - описывает операции и сообщение, которые могут встретиться в сервисе.
    - `<binding>` - определяет протокол и формат данных для каждого типа порта.
    - `<service>` - определяет адрес веб сервиса.
    - `<definition>` - корневой элемент каждого WSDL документа.
    - `<operation>` - абстрактное определение операции для сообщения.
    - `<documentation>` - предоставляет документацию
    - `<import>` - импортирует сторонние WSDL документы или XML Schemas.
    
2. **Структура WSDL документа** выглядит следующим образом:
    ```xml
    <definitions>
        <types>
          data type definitions........
        </types>
        <message>
          definition of the data being communicated....
        </message>
        <portType>
          set of operations......
        </portType>
        <binding>
          protocol and data format specification....
        </binding>
    </definitions> 
   ```

3. `<portType>` - элемент, который определяет веб сервис, операции, приводимые в нем, и задействованные сообщения.
    - __request-response__ - самый распространенный тип операции. Она получает запрос и возвращает ответ.
    - __one-way__ - операция может получать сообщения, но не будет возвращать ответ.
    - __solicit-response__ - операция может отправлять запрос и будет ждать ответа.
    - __notification__ - операция может посылать сообщений, но не будет ждать ответа.
    
4. Пример Request-Response операции (словарь терминов):
   ```xml
    <message name="getTermRequest">
      <part name="term" type="xs:string"/>
    </message>
    <message name="getTermResponse">
      <part name="value" type="xs:string"/>
    </message>
    <portType name="glossaryTerms">
      <operation name="getTerm">
        <input message="getTermRequest"/>
        <output message="getTermResponse"/>
      </operation>
    </portType> 
      ```
    - `<portType>` определяет "glossaryTerms" как имя порта, а `getTerm` - имя операции
    - `<message>` элементы определяют `<part>` сообщений "getTermRequest" и "getTermResponse".
      
5. Пример One-Way операции (словарь терминов):
   ```xml
    <message name="newTermValues">
      <part name="term" type="xs:string"/>
      <part name="value" type="xs:string"/>
    </message>
    <portType name="glossaryTerms">
      <operation name="setTerm">
        <input name="newTerm" message="newTermValues"/>
      </operation>
    </portType > 
   ```
   - В этом примере "glossaryTerms" определяет one-way операцию "setTerm".
   - "setTerm" операция позволяет вводить новое сообщение используя "newTermValues".
   
6. Пример WSDL файла:
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <definitions name="HelloService"
                 targetNamespace="http://www.ecerami.com/wsdl/HelloService.wsdl"
                 xmlns="http://schemas.xmlsoap.org/wsdl/"
                 xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/"
                 xmlns:tns="http://www.ecerami.com/wsdl/HelloService.wsdl"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
        <types>
            <xsd:schema>
                <xsd:import
                        schemaLocation="http://localhost:9876/ts?xsd=1"
                        namespace="http://ts.ch02/">
                </xsd:import>
            </xsd:schema>
        </types>
        <message name="SayHelloRequest">
            <part name="firstName" type="xsd:string"/>
        </message>
        <message name="SayHelloResponse">
            <part name="greeting" type="xsd:string"/>
        </message>
        <portType name="Hello_PortType">
            <operation name="sayHello">
                <input message="tns:SayHelloRequest"/>
                <output message="tns:SayHelloResponse"/>
            </operation>
        </portType>
        <binding name="Hello_Binding" type="tns:Hello_PortType">
            <soap:binding style="rpc"
                          transport="http://schemas.xmlsoap.org/soap/http"/>
            <operation name="sayHello">
                <soap:operation soapAction="sayHello"/>
                <input>
                <soap:body
                        encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"
                        namespace="urn:examples:helloservice"
                        use="encoded"/>
                </input>
                <output>
                    <soap:body
                            encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"
                            namespace="urn:examples:helloservice"
                            use="encoded"/>
                </output>
            </operation>
        </binding>
        <service name="Hello_Service">
            <documentation>WSDL File for HelloService</documentation>
            <port binding="tns:Hello_Binding" name="Hello_Port">
                <soap:address
                        location="http://localhost:8080/soap/rpcrouter"/>
            </port>
        </service>
    </definitions>
    ```
    - `<service>`: HelloService.
    - `<types>`: Использование импортированной по локальному адресу XML Schema.
    - `<message>`: "sayHelloRequest": "firstName" параметр, "sayHelloResponse": "greeting" возвращаемое 
    значение
    - `<portType>`: sayHello операция, которая состоит из request-response сервиса.
    - `<binding>`: Указание использовать SOAP HTTP протокол.
    - `<service>`: сервис доступен по ссылке http://www.examples.com/SayHello/.
    - `<port>`: Связывает `<binding>` с URI http://www.examples.com/SayHello/, по которой доступен данный сервис.

***

### 5. UDDI

1. **UDDI (Universal Description, Discovery, and Integration)** - предоставляет всемирный реестр веб сервисов для рекламы, поиска и хранения. <sup>[\[source\]][uddi]</sup>
   - UDDI предоставляет структуру для представления деловых отношений, веб сервисов, технических метаданных и точек доступа к веб сервисам.

***

### 6. REST

1. **REST (REpresentational State Transfer)** - это стиль архитектуры программного обеспечения для распределенных систем, использующий веб протоколы и веб технологии. REST архитектура включает в себя клиентское и серверное взаимодействие, построенное вокруг передачи ресурсов. <sup>[\[source\]][rest]</sup>
   - Самая большая реализация REST - World Wide Web, которая, как правило, используется для построения веб-служб.
   - Системы, которые построены согласно REST принципам, называются RESTful.
   - REST может быть использован для сбора данных вебсайта через XML файлы веб страницы.
   - Пользователи могут обращаться к веб страницам через URL сайта, взаимодействовать с XML файлами через браузер и использовать данные как угодно.
   - Базовые REST принципы:
      + Client и Server - клиент и сервер должны быть отделены от REST операций через специальный интерфейс, который улучшает переносимость кода.
      + Stateless - каждый клиентский запрос должен содержать все требуемые данные для обработки запроса без хранения клиентского окружения на сервере.
      + Cacheable - ответы могут быть закэшированны на клиентском компьютере, чтобы ускорить веб поиск.
      + Layered System - позволяет клиентам подключаться к серверу через вспомогательный уровень для улучшения расширяемости.

2. Клиент/сервер связь:
   ```
                     HTTP GET, POST, PUT, or DELETE
     REST: client ----------------------------------> service

           client <---------------------------------- service
                    XML, JSON, plaintext,... document
   ```
 
***

### Веб-сервисы в Java

1. **Servlet API** является основой для всех остальных технологий Java, касающихся Web и дает возможность динамически генерировать любой web-контент, используя любые библиотеки, доступные для java. 

1. **JSP (JavaServer Pages)** - технология, используемая для разработки интерактивных веб страниц. JSP была разработана Sun Microsystems и является улучшенной версией Java сервлетов. <sup>[\[source\]][jsp]</sup>
	- Как и большинство серверных технологий, JSP отделяет бизнес логику от представления.
	- JSP являются обычные HTML страницы с встроенным Java кодом.
	- Чтобы обработать JSP файл, разработчику нужен JSP движок, который подключен к веб серверу. 
	- JSP страница компилируется в сервлет, который управляет сервлет движком (этот этап называется "преобразованием"). Сервлет движок затем загружает класс сервлета и реализовывает его, чтобы создать динамический HTML, который затем посылается в браузер. Такой процесс запускается каждый раз, когда запрашивается очередная страница.
	- Если вместе с JSP исользовать JDBC, то можно сделать динамические, связанные с базой данных, вебсайты.

1. **Apache Tomcat** - опенсорсный веб сервер, разработанный Apache Software Foundation. Он позволяет реализовывать Java сервлеты и JSPs для поддержки эффективных Java-серверных сред. <sup>[\[source\]][tomcat]</sup>
	- Пользователь также может получить доступ к конфигурациям и использовать XML для настройки проектов.
	- Tomcat может предоставить рантайм оболочку для Java сервлетов.
	- Ключевой элемент Java-based веб сервера - сервлет контейнер, поэтому JSP скрипты и им подобные автоматически преобразовываются в сервлет.
	- **Catalina** — контейнер сервлетов Tomcat’а, который реализует спецификацию сервлетов.

1. **Apache Ant** - Java-based опенсорсный build tool, разработанный Apache Software Foundation. Он схож с "make" утилитой, но в большинстве своем функционирует только на java платформе. <sup>[\[source\]][ant]</sup>
	- В отличии от Make, Ant написан на XML, поэтому портируемость и простота - это два главных преимущества Ant.

1. **RPC (Remote Procedure Call)** - класс технологий, позволяющих компьютерным программам вызывать функции или процедуры в другом адресном пространстве (как правило, на удаленных компьютерах). <sup>[\[source\]][rpc]</sup>
	- RPC работает по принципу: отправитель или клиент создает запрос с помощью процедуры, функции или вызова метода в удаленный сервер, который RPC обрабатывает и посылает. Когда удаленный сервер получает запрос, он отсылает ответ назад клиенту, и приложение продолжает свою работу. Перед тем, как продолжать работу программы, клиент ждет, пока сервер завершит процесс обработки.
	- В общем, RPC приложения используют модули, называемые прокси и заглушки, которые заставляют их выглядеть как простые локальные вызовы процедур.
	- RPC-ориентированное приложение - приложение, в которых существует интерактивная связь между удалёнными компонентами с небольшим временем ответов и относительно малым количеством передаваемых данных.
	- Пример RPC можно найти в GWT.

1. **RMI (Remote Method Invocation)** - программный интерфейс вызова удаленных методов в языке Java. <sup>[\[source\]][rmi]</sup>
	- Он представляет объектно-ориентированный эквивалент RPC.
	- RMI функциональность находится в `java.rmi` пакете и предоставляет распределенную объектную модель, специфицирующую, каким образом производится вызов удаленных методов, работающих на другой виртуальной машине Java.
	- При доступе к объектам на другом компьютере возможно вызывать методы этого объекта. Необходимо только передать параметры метода на другой компьютер, сообщить объекту о необходимости выполнения метода, а затем получить обратно возвращаемое значение. 
  
1. **RSS (Really Simple Syndication)**

1. **RDF (Resource Description Framework)**

[web-service]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#whatis
[agent]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#agent
[service]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service
[service-description]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service_description
[service-provider]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#id2608853
[service-requestor]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#id2608853
[action]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#action
[service-task]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service_task
[service-semantics]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#id2617100
[service-operation]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service_operation
[choreography-description-language]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#choreography_description_language
[choreography]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#choreography
[message]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#message
[mom]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#message_oriented_model
[som]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service_oriented_model
[rom]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#resource_oriented_model
[pm]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#policy_model
[mm]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#management_model
[soa]: https://ru.wikipedia.org/wiki/%D0%A1%D0%B5%D1%80%D0%B2%D0%B8%D1%81-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F_%D0%B0%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0
[roa]: https://en.wikipedia.org/wiki/Resource-oriented_architecture
[rpc]: https://www.techopedia.com/definition/24022/remote-procedure-call-rpc
[wsdl]: http://gsl.mit.edu/media/programs/south-africa-summer-2015/materials/o'reilly_-_java_web_services.pdf#page=12&zoom=auto,-83,820
[uddi]: http://gsl.mit.edu/media/programs/south-africa-summer-2015/materials/o'reilly_-_java_web_services.pdf#page=12&zoom=auto,-83,820
[soap]: http://gsl.mit.edu/media/programs/south-africa-summer-2015/materials/o'reilly_-_java_web_services.pdf#page=12&zoom=auto,-83,820
[jsp]: https://www.techopedia.com/definition/4886/javaserver-page-jsp
[rest]: https://www.techopedia.com/definition/1312/representational-state-transfer-rest
[tomcat]: https://www.techopedia.com/definition/15735/apache-tomcat
[rest]: https://www.techopedia.com/definition/1312/representational-state-transfer-rest
[ant]: https://www.techopedia.com/definition/16219/apache-ant
[tcp/ip]: http://www.w3schools.com/website/web_tcpip.asp
[http]: https://www.techopedia.com/definition/2336/hypertext-transfer-protocol-http
[https]: https://www.techopedia.com/definition/5361/hypertext-transport-protocol-secure-https
[dns]: https://www.techopedia.com/definition/5361/hypertext-transport-protocol-secure-https
[rmi]: https://www.techopedia.com/definition/1311/remote-method-invocation-rmi
[diagram]: http://gsl.mit.edu/media/programs/south-africa-summer-2015/materials/o'reilly_-_java_web_services.pdf#page=12&zoom=auto,-83,10