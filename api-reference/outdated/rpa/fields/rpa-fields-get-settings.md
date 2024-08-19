# Получение полного набора настроек видимости полей на стадии с идентификатором stageId процесса с идентификатором typeId

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}


{% note info "rpa.fields.getSettings" %}

**Scope**: [`rpa`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `rpa.fields.getSettings` вернет полный набор настроек видимости полей на стадии с идентификатором stageId процесса с идентификатором typeId.

#|
|| **Параметр** / **Тип** | **Описание** ||
|| **typeId**^*^ 
[`number`](../../../data-types.md) | Идентификатор процесса. ||
|| **stageId** 
[`number`](../../../data-types.md) | Идентификатор стадии. По умолчанию 0 (общие настройки). ||
|#

{% include [Сноска о параметрах](../../../../_includes/required.md) %}

## Ответ в случае успеха

```json
{
    "fields": {
        "kanban": {
            "id": true,
            "UF_RPA_1_NAME": true
        },
        "create": {
            "UF_RPA_1_NAME": true
        }
    }
}
```