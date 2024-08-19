# Встраивание в виде пользовательских типов полей

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания

{% endnote %}

{% endif %}

{% note info "Пользовательские поля" %}

**Scope**: в зависимости от [`места встройки`](../../scopes/permissions.md) **Права на выполнение**: `для всех`.

{% endnote %}


Приложения, имеющие доступ к скоупу **placement** могут регистрировать свои типы пользовательских полей.

На данный момент облачные порталы поддерживают работу таких полей в новой и старой карточке сущностей **CRM**. Приложения могут создавать пользовательские поля стандартных типов и тех, которые зарегистрированы этим приложением. Администраторы портала могут создавать поля любых зарегистрированных типов, включая типы полей, зарегистрированных приложениями. При регистрации типа приложение указывает адрес обработчика, который будет открываться в фрейме по месту вывода поля, и дальнейшая работа практически ничем не отличается от работы обычной встройки.



| Метод | Описание | С версии |
|-------|----------|----------|
| [userfieldtype.add](./userfieldtype-add.md) | Регистрация нового типа пользовательских полей. | |
| [userfieldtype.list](./userfieldtype-list.md) | Получение списка зарегистрированных приложением типов пользовательских полей. | |
| [userfieldtype.update](./userfieldtype-update.md) | Изменение настроек зарегистрированного приложением типа пользовательских полей. | |
| [userfieldtype.delete](./userfieldtype-delete.md) | Удаление зарегистрированного приложением типа пользовательских полей. | |

## Дополнительно

1. Подробнее о встройке в виде пользовательских типах полей, читайте в [учебном курсе](https://dev.1c-bitrix.ru/learning/course/index.php?COURSE_ID=99&LESSON_ID=8633)

2. Вы зарегистрировали новый тип пользовательских полей. Если при попытке создать поле с новым типом:

- [userfieldtype.list](./userfieldtype-list.md) возвращает ваш новый тип пользовательского поля
- и, тем не менее, у вас возникает ошибка: `Error! 400: ERROR_CORE: Указан неверный пользовательский тип. (400)`

, то это значит, что [приложение](*приложение) не установлено полностью. Вызовите метод [app.info](../../common/system/app-info.md) и убедитесь что в результате вернулось `INSTALLED = true`. Если приложение с интерфейсом, то для завершения установки необходимо на странице приложения выполнить js код:

```javascript
BX24.init(function(){
    BX24.installFinish();
});
```

[*приложение]: Под локальными приложениями понимаются приложения, которые описываются и добавляются непосредственно на конкретный Битрикс24.
