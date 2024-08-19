# Удаление пользовательского поля

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания
- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры

{% endnote %}

{% endif %}

{% note info "onCrmCompanyUserFieldDelete" %}

**Scope**: [`crm`](../../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Событие `onCrmCompanyUserFieldDelete` вызывается при удалении пользовательского поля.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **id**
[`unknown`](../../../../data-types.md) | идентификатор пользовательского поля. ||
|| **entityId**
[`unknown`](../../../../data-types.md) | символьный идентификатор сущности, для которой создано поле ||
|| **fieldName**
[`unknown`](../../../../data-types.md) | имя созданного пользовательского поля ||
|#