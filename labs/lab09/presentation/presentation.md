---
## Front matter
lang: ru-RU
title: Лабораторная работа №9
subtitle: Управление SELinux
author:
  - Щемелев Илья Владимирович
institute:
  - Российский университет дружбы народов, Москва, Россия

## Formatting pdf
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

## Формулировка цели

Получить навыки работы с контекстом безопасности и политиками SELinux.


# Ход выполнения работы

## Перевод в Permissive (setenforce 0)

![Переход в режим Permissive](Screenshot_1.png){ width=85% }

## Отключение SELinux в конфигурации

![Отключение SELinux в /etc/sysconfig/selinux](Screenshot_2.png){ width=85% }

## Проверка Disabled и реакция на setenforce

![SELinux отключён и не переключается без перезагрузки](Screenshot_3.png){ width=85% }

## Возврат SELINUX=enforcing

![Возврат SELinux в enforcing через конфигурацию](Screenshot_4.png){ width=85% }

## Проверка enforcing после перезагрузки

![SELinux в режиме enforcing](Screenshot_5.png){ width=85% }

## Контекст /etc/hosts и восстановление меток

![Восстановление контекста /etc/hosts (restorecon)](Screenshot_6.png){ width=90% }

## Сообщения перемаркировки при загрузке

![Автоматическая перемаркировка файловой системы (autorelabel)](Screenshot_7.png){ width=90% }

## Изменение DocumentRoot и правил доступа

![Правка /etc/httpd/conf/httpd.conf: DocumentRoot /web](Screenshot_8.png){ width=85% }

## Страница по умолчанию до настройки SELinux

![Тестовая страница Rocky Linux по умолчанию](Screenshot_9.png){ width=85% }

## Назначение контекста httpd_sys_content_t и restorecon

![semanage fcontext и restorecon для /web](Screenshot_10.png){ width=90% }

## Проверка через lynx: пользовательская страница

![Welcome to my web-server](Screenshot_11.png){ width=90% }

## Проверка и включение ftpd_anon_write

![Управление boolean ftpd_anon_write](Screenshot_12.png){ width=90% }

# Итоги работы

## Заключение

Выполнено управление режимами SELinux (Enforcing/Permissive/Disabled), подтверждена невозможность переключения из Disabled без перезагрузки. Отработано восстановление контекстов безопасности с помощью restorecon и массовая перемаркировка через `/.autorelabel`. Настроен доступ httpd к нестандартному каталогу `/web` путём назначения корректного типа контекста `httpd_sys_content_t`. Изучены и изменены boolean-переключатели SELinux на примере `ftpd_anon_write` (временное и постоянное включение).
