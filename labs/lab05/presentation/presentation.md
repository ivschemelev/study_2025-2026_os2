---
lang: ru-RU
title: Лабораторная работа №5
subtitle: Управление системными службами systemd
author:
  - Щемелев Илья Владимирович
institute:
  - Российский университет дружбы народов, Москва, Россия

## Параметры презентации
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

Получить практические навыки управления системными службами и целями операционной системы с использованием системы инициализации systemd.

# Ход выполнения работы

## Проверка наличия службы vsftpd

![Проверка статуса службы vsftpd](Screenshot_1.png){ width=85% }

## Запуск службы vsftpd

![Запуск и проверка состояния службы vsftpd](Screenshot_2.png){ width=85% }

## Управление автозапуском vsftpd

![Включение и отключение автозапуска службы vsftpd](Screenshot_3.png){ width=85% }

## Повторное включение vsftpd в автозапуск

![Служба vsftpd в автозапуске](Screenshot_4.png){ width=85% }

## Анализ зависимостей vsftpd

![Зависимости и обратные зависимости vsftpd](Screenshot_5.png){ width=85% }


## Проверка статуса firewalld и iptables

![Состояние firewalld и iptables](Screenshot_6.png){ width=85% }

## Анализ юнита firewalld

![Файл firewalld.service](Screenshot_7.png){ width=85% }

## Анализ юнита iptables

![Файл iptables.service](Screenshot_8.png){ width=85% }

## Маскирование службы iptables

![Маскирование iptables](Screenshot_9.png){ width=85% }

## Поиск изолируемых целей

![Список изолируемых целей systemd](Screenshot_10.png){ width=85% }

## Переход в режим восстановления

![Режим rescue.target](Screenshot_11.png){ width=85% }

## Установка текстового режима загрузки

![Установка multi-user.target](Screenshot_12.png){ width=85% }

## Возврат графического режима загрузки

![Установка graphical.target](Screenshot_13.png){ width=85% }

# Итоги работы

## Заключение

В ходе лабораторной работы были изучены механизмы управления системными службами и целями systemd. Освоены приёмы установки, запуска, настройки автозапуска сервисов, анализа зависимостей и разрешения конфликтов между службами. Полученные навыки позволяют эффективно управлять режимами работы и состоянием операционной системы.
