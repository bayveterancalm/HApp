# Установка HAPP на Windows

HAPP — имя этого репозитория и Windows-сборки Zapret/WinDivert. Включает стратегии запуска, служебные инструменты, IPSet и диагностику сетевого доступа к поддерживаемым ресурсам.

## Перед началом

- Скачивайте архив только со страницы [Releases](https://github.com/Stuccozenupgrade/happ/releases/latest).
- Сверьте файлы с `Files/SHA256SUMS.txt`, если выполняете проверку целостности.
- Ознакомьтесь с предупреждением README о WinDivert и реакциях антивирусов. Не отключайте защиту без проверки источника файлов.
- Для DNS-настроек подготовьте Secure DNS в браузере или Windows 11, как описано в README.

## Установка

1. Откройте [последний релиз](https://github.com/Stuccozenupgrade/happ/releases/latest) и скачайте приложенный архив `happ.zip`.
2. В свойствах файла Windows при необходимости снимите блокировку скачанного архива. Для некоторых архиваторов этот шаг не требуется.
3. Распакуйте файлы в каталог, путь к которому не содержит кириллицу и специальные символы.
4. Откройте README и ознакомьтесь с назначением `general.bat` и `service.bat`.
5. Сначала запустите подходящую стратегию вручную через один из `general*.bat`, проверяя результат. Не включайте постоянную службу, пока не убедились, что выбранная конфигурация подходит.
6. Для системных операций используйте права администратора и только те функции `service.bat`, назначение которых понятно.

## Secure DNS

README рекомендует включить Secure DNS. В Chrome это настройка безопасного DNS; в Firefox — DNS over HTTPS. В Windows 11 есть системная настройка DNS over HTTPS для поддерживаемых конфигураций. Доступность зависит от поставщика DNS и сети.

## Telegram и Discord

- Для Telegram Web README описывает функцию `Update Hosts File` в `service.bat`.
- Для голосового подключения Discord README предлагает проверить hosts, Secure DNS, кэш клиента и стратегии.
- Для Telegram Desktop README направляет к отдельному проекту [tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy). Не считать его встроенным компонентом этого архива.

## После установки

Проверьте сайты и приложения по отдельности. Запишите, какая стратегия работает, и не включайте `IPSet any` постоянно: README предупреждает о возможных проблемах с доступностью других сайтов.

## Ссылки

- [Релизы](https://github.com/Stuccozenupgrade/happ/releases/latest)
- [Issues](https://github.com/Stuccozenupgrade/happ/issues)
- [Discussions](https://github.com/Stuccozenupgrade/happ/discussions)
- [Исходный Zapret](https://github.com/bol-van/zapret)
