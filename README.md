# Микросервис
## который принимает сообщения от брокера сообщений (nats), хранит в кэше + БД и отдает на вебстраницу.
Для отправки - ** (third_party\nats\publisher\main.go) **
Для приема (third_party\nats\subscriber\main.go) сообщения nats streaming сервера. При запуске основного приложения (cmd\wb0\main.go) - все сообщения из базы данных записываются в кэш(реализованный через мапу) и при рендере страниц - данные берутся из кэша. Так же в (third_party\nats\subscriber\main.go) присутствует проверка на валидность данных - путем сверки с моделью.
