# Архитектурные модели

1. **SOA (Service Based Architecture)** - модульный подход к разработке программного обеспечения, основанный на использовании распределённых, слабо связанных заменяемых компонентов, оснащённых стандартизированными интерфейсами для взаимодействия по стандартизированным протоколам. <sup>[\[source\]][soa]</sup>
	- Программные комплексы, разработанные в соответствии с сервис-ориентированной архитектурой, обычно реализуются как набор веб-служб, взаимодействующих по протоколу SOAP, но существуют и другие реализации, например, на основе REST.

2. **ROA (REST-Oriented Architecture)** - архитектурный стиль приложения и подход к разработке для создания ПО в виде ресурсов с RESTful интерфейсами. Эти ресурсы являются программными компонентами, которые могут быть переиспользованы для различных целей. <sup>[\[source\]][roa]</sup>

1. **MOM (Message-Oriented Model)** сосредаточена на тех аспектах архитектуры, которые относятся к сообщениям и их обработке. <sup>[\[source\]][mom]</sup>

1. **SOM (Service-Oriented Model)** сосредаточена на тех аспектах архитектуры, которые относятся к сервису и действиям. <sup>[\[source\]][som]</sup>
	- Главная цель SOM - устанавливать отношения между агентом, сервисом, который он реализует, и запросами.
	- SOM построен на основе MOM, но сосредочен больше на действия, чем на сообщения.

1. **ROM (Resource-Oriented Model)** сосредоточена на тех аспектах архитектуры, которые относятся к ресурсам, и сервис модель которых связана с манипулированием ресурсами. <sup>[\[source\]][rom]</sup>

1. **PM (Policy Model)** сосредаточена на тех аспектах архитектуры, которые относятся к политике, расширениям, защите и качеству сервиса. <sup>[\[source\]][pm]</sup>

1. **MM (Management Model)** сосредаточена на тех аспектах архитектуры, которые относятся к регулированию веб сервисов. <sup>[\[source\]][mm]</sup>

[mom]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#message_oriented_model
[som]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#service_oriented_model
[rom]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#resource_oriented_model
[pm]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#policy_model
[mm]: https://www.w3.org/TR/2003/WD-ws-arch-20030808/#management_model
[soa]: https://ru.wikipedia.org/wiki/%D0%A1%D0%B5%D1%80%D0%B2%D0%B8%D1%81-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%B0%D1%8F_%D0%B0%D1%80%D1%85%D0%B8%D1%82%D0%B5%D0%BA%D1%82%D1%83%D1%80%D0%B0
[roa]: https://en.wikipedia.org/wiki/Resource-oriented_architecture