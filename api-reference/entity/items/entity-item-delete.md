# Удаление элемента хранилища

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "entity.item.delete" %}

**Scope**: [`entity`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `entity.item.delete` удаляет элемент хранилища. Пользователь должен обладать хотя бы правами на запись (**W**) в хранилище.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **ENTITY^*^**
[`string`](../../data-types.md) | Обязательный. Строковый идентификатор хранилища. ||
|| **ID^*^**
[`integer`](../../data-types.md) | Обязательный. Идентификатор элемента. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

## Пример

Вызов

```js
BX24.callMethod(
    'entity.item.delete',
    {
        ENTITY: 'menu_new',
        ID: 842
    }
);
```

Запрос

```http
https://my.bitrix24.ru/rest/entity.item.delete.json?ENTITY=menu_new&ID=842&auth=340bf57f35ee95e0debf98399632999c
```

{% include [Сноска о примерах](../../../_includes/examples.md) %}

## Ответ в случае успеха

> 200 OK
```json
{"result":true}
```