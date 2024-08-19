# Изменение комментария

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- отсутствуют примеры (должно быть три примера - curl, js, php)
- отсутствует ответ в случае ошибки
- отсутствует ответ в случае успеха
- добавить описание, что можно проверять право на изменение специальным методом

{% endnote %}

{% endif %}

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% note info "task.commentitem.update" %}

**Scope**: [`task`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `task.commentitem.update` обновляет данные комментария. Требуется обязательная авторизация через oauth и получение auth кода.

## Параметры

#|
|| **Параметр** / **Тип** | **Описание** ||
|| **TASKID^*^**
[`unknown`](../../data-types.md) | Идентификатор задачи. ||
|| **ITEMID^*^**
[`unknown`](../../data-types.md) | Идентификатор комментария. ||
|| **FIELDS^*^**
[`unknown`](../../data-types.md) | Массив полей данных по комментарию (`POST_MESSAGE` — обязательное поле). ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

{% note info %}

Соблюдение порядка следования параметров в запросе обязательно. При его нарушении запрос будет выполнен с ошибками.

{% endnote %}

## Пример

```js
// Обновить комментарий с ID=1205, задав текст "HI"

BX24.callMethod(
    'task.commentitem.update',
    [13, 1205, {'POST_MESSAGE': 'HI'}],
    function(result){
        console.info(result.data());
        console.log(result);
    }
);
```
{% include [Сноска о примерах](../../../_includes/examples.md) %}