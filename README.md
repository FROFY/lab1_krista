# lab1_krista

Кукушкин Илья, Смирнов Денис

@startuml
!theme vibrant
skinparam actorStyle awesome
actor "Читатель" as Reader
actor "Писатель" as Writer
actor "Редактор" as Editor

rectangle Write {
usecase "Написание статьи" as WriteBookW
usecase "Просмотр статьи" as ReadBookW
usecase "Поиск статьи" as FindBookW
usecase "Настройка рекомендаций" as SetRecW
usecase "Настройка дизайна" as SetDesignW
usecase "Создание аккаунта" as CreateAccW
}

rectangle Read {
usecase "Просмотр статьи" as ReadBookR
usecase "Поиск статьи" as FindBookR
usecase "Комментирование статьи" as CommentBookR
usecase "Добавление в избранное" as AddToFavouriteR
usecase "Настройка рекомендаций" as SetRecR
usecase "Настройка дизайна" as SetDesignR
usecase "Создание аккаунта" as CreateAccR
}

rectangle Edit {
usecase "Внесение изменений в сайт" as EditSiteE
usecase "Просмотр статьи" as ReadBookE
usecase "Поиск статьи" as FindBookE
usecase "Управление правами доступа" as PrivacyE
usecase "Комментирование статьи" as CommentBookE
}

Reader -right-> Read
Writer -right-> Write
Editor -left-> Edit

@enduml
