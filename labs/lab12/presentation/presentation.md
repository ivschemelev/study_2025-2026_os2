---
## Front matter
lang: ru-RU
title: Лабораторная работа №12
subtitle: Настройки сети в Linux
author:
  - Щемелев Илья Владимирович

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

Получить навыки настройки сетевых параметров системы.

# Ход выполнения работы

## Сетевые интерфейсы и статистика

![Информация о сетевых интерфейсах](Screenshot_1.png){ width=85% }

## IP-адреса интерфейса

![Назначенные IP-адреса](Screenshot_2.png){ width=85% }

## Проверка сетевой связности

![Проверка доступности сети](Screenshot_3.png){ width=85% }

## Добавление дополнительного IPv4-адреса

![Проверка добавленного адреса](Screenshot_4.png){ width=85% }

## Сравнение ip и ifconfig

![Вывод ifconfig](Screenshot_5.png){ width=85% }

## Прослушиваемые порты

![Прослушиваемые порты](Screenshot_6.png){ width=85% }

## Создание профилей dhcp и static

![Проверка сетевых профилей](Screenshot_7.png){ width=85% }

## Переключение на static

![Активация static-соединения](Screenshot_8.png){ width=85% }

## Возврат к dhcp

![Возврат к DHCP-соединению](Screenshot_9.png){ width=85% }

## Активация static и проверка

![Активация статического соединения и проверка адресов](Screenshot_10.png){ width=85% }

## Проверка параметров через nmtui

![Настройки статического соединения в nmtui](Screenshot_11.png){ width=85% }

## Просмотр DHCP-профиля в nmtui

![Настройки DHCP соединения в nmtui](Screenshot_12.png){ width=85% }

## Параметры в графическом интерфейсе

![Настройки статического соединения в графическом интерфейсе](Screenshot_13.png){ width=85% }

## DHCP в графическом интерфейсе

![Настройки DHCP-соединения в графическом интерфейсе](Screenshot_14.png){ width=85% }

# Итоги работы

## Заключение

Изучены и отработаны приёмы диагностики и настройки сети в RHEL-подобной системе: анализ интерфейсов, маршрутов и IP-адресов, проверка доступности сети, управление профилями NetworkManager, настройка DHCP и статических параметров, а также проверка конфигурации через `nmcli`, `nmtui` и графический интерфейс.
