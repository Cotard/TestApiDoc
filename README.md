# TestApiDoc

### Ограничения числа обращений к API
К методам API SuperJob можно обращаться не более 60 раз в минуту.

### Как узнать, сколько доступных обращений осталось?
После каждого вызова метода API сервер возвращает несколько HTTP-заголовков с текущим статусом ограничения запросов.

``` 
curl -i https://api.superjob.ru/2.0/vacancies/29955599/

HTTP/1.1 200 OK 
Date: Fri, 06 Oct 2017 14:16:39 GMT 
X-RateLimit-Limit: 60 
X-RateLimit-Remaining: 56 
X-RateLimit-Reset: 1372700873 * 

{"id_client":14449,
"payment_to":110000,
"date_archived":1506176701,
"address":null,
"profession":"Технический писатель", 
...}

```

*предполагаю, что время будет в UTC. 

