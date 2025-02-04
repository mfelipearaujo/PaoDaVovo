# Pão da Vovó API

-   [Pão da Vovó API](#pao-da-vovo-api)
    -   [Create Breakfast](#create-breakfast)
        -   [Create Breakfast Request](#create-breakfast-request)
        -   [Create Breakfast Response](#create-breakfast-response)
    -   [Get Breakfast](#get-breakfast)
        -   [Get Breakfast Request](#get-breakfast-request)
        -   [Get Breakfast Response](#get-breakfast-response)
    -   [Update Breakfast](#update-breakfast)
        -   [Update Breakfast Request](#update-breakfast-request)
        -   [Update Breakfast Response](#update-breakfast-response)
    -   [Delete Breakfast](#delete-breakfast)
        -   [Delete Breakfast Request](#delete-breakfast-request)
        -   [Delete Breakfast Response](#delete-breakfast-response)

## Create Breakfast

### Create Breakfast Request

```js
POST / breakfasts
```

```json
{
    "name": "Café da manhã",
    "description": "Junte-se a nós para um delicioso café da manhã...",
    "startDateTime": "2024-04-08T08:00:00",
    "endDateTime": "2024-04-08T11:00:00",
    "savory": ["Tapioca", "Misto quente", "Omelete de frango", "Ovos mexidos"],
    "sweet": ["Salada de frutas"]
}
```

### Create Breakfast Response

```js
201 Created
```

```yml
Location: {{host}}/Breakfasts/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Café da manhã",
    "description": "Junte-se a nós para um delicioso café da manhã...",
    "startDateTime": "2024-04-08T08:00:00",
    "endDateTime": "2024-04-08T11:00:00",
    "lastModifiedDateTime": "2024-04-06T12:00:00",
    "savory": ["Tapioca", "Misto quente", "Omelete de frango", "Ovos mexidos"],
    "sweet": ["Salada de frutas"]
}
```

## Get Breakfast

### Get Breakfast Request

```js
GET /breakfasts/{{id}}
```

### Get Breakfast Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Café da manhã",
    "description": "Junte-se a nós para um delicioso café da manhã...",
    "startDateTime": "2024-04-08T08:00:00",
    "endDateTime": "2024-04-08T11:00:00",
    "lastModifiedDateTime": "2024-04-06T12:00:00",
    "savory": ["Tapioca", "Misto quente", "Omelete de frango", "Ovos mexidos"],
    "sweet": ["Salada de frutas"]
}
```

## Update Breakfast

### Update Breakfast Request

```js
PUT /breakfasts/{{id}}
```

```json
{
    "name": "Café da manhã",
    "description": "Junte-se a nós para um delicioso café da manhã...",
    "startDateTime": "2024-04-08T08:00:00",
    "endDateTime": "2024-04-08T11:00:00",
    "savory": ["Tapioca", "Misto quente", "Omelete de frango", "Ovos mexidos"],
    "sweet": ["Salada de frutas"]
}
```

### Update Breakfast Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Breakfasts/{{id}}
```

## Delete Breakfast

### Delete Breakfast Request

```js
DELETE /breakfasts/{{id}}
```

### Delete Breakfast Response

```js
204 No Content
```
