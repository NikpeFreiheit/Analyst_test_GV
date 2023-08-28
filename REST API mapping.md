# REST API mapping

<u>**GET method**</u>

|Name|Type|Mandatory|Default|Comments|
|--|--|--|--|--|
Path - no requirements
|__|__|__|__|__|
Query
|Limit|integer|n|100|Quantity of records to return in response|
|Start_from|string|n| |The ID from which to return records. If the identifier is empty, then return the records starting from the first|
Body - no requirements
|__|__|__|__|__|


<u>**POST method**</u>
|Name|Type|Mandatory|Default|Comments|
|--|--|--|--|--|
Path - no requirements
|__|__|__|__|__|
Query - no requirements
|__|__|__|__|__|
Body
|massive_name[]|massive|y|-|--|
Massive
|id|string|y| |--|
|name|string|n| |--|

<u>**DELETE method**</u>
|Name|Type|Mandatory|Default|Comments|
|--|--|--|--|--|
Path 
|order_number|string|y| |order number which need to delete|
Query - no requirements
|__|__|__|__|__|
Body - no requirements
|__|__|__|__|__|

Template:
http://url.com/orders/{order_number}


<u>**POST method**</u> can be used for filters. In this case, the request body describes the filtering parameters.

В REST API path не выделяется как параметр, но для OpenAPI cуществует следующие типы параметров:
- **Header parameters** (параметры заголовка) - Custom headers that are expected as part of the request.
- **Path parameters** (параметры path) - Used together with Path Templating, where the parameter value is actually part of the operation's URL. This does not include the host or base path of the API.
- **Query parameters** (параметры строки запроса) - Query parameters are optional key-value pairs that appear to the right of the ? in a URL. 
- **Body parameters** (параметры тела запроса) -  The payload that's appended to the HTTP request. Since there can only be one payload, there can only be one body parameter. Body parameters and Form parameters cannot exist together for the same operation
- **Form parameters** - This is the only parameter type that can be used to send files, thus supporting the file type.


# Headers
1. General Headers (Основные заголовки) — должны включаться в любое сообщение клиента и сервера.
2. Request Headers (Заголовки запроса) — используются только в запросах клиента.
3. Response Headers (Заголовки ответа) — только для ответов от сервера.
4. Entity Headers (Заголовки сущности) — сопровождают каждую сущность сообщения.