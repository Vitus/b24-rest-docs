# Получение списка полей

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры (на других языках)
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "crm.lead.userfield.list" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `crm.lead.userfield.list` возвращает список пользовательских полей лидов по фильтру.

#|
|| **Параметр** | **Описание** ||
|| **order** | Поля сортировки. ||
|| **filter** | Поля фильтра. ||
|#

## Пример

```js
BX24.callMethod(
    "crm.lead.userfield.list",
    {
        order: { "SORT": "ASC" },
        filter: { "MANDATORY": "N" }
    },
    function(result)
    {
        if(result.error())
            console.error(result.error());
        else
        {
            console.dir(result.data());             
            if(result.more())
                result.next();                        
        }
    }
);
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}