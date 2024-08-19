# Получить список полей документов

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствует таблица fields
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "documentgenerator.document.getfields" %}

**Scope**: [`documentgenerator`](../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `documentgenerator.document.getfields` возвращает список полей документа с их описанием. Возвращаемые значения абсолютно идентичны методу [documentgenerator.template.getfields()](./templates/document-generator-template-get-fields.md).
