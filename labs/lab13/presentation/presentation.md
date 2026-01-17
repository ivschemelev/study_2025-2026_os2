---
## Front matter
lang: ru-RU
title: Отчёт по лабораторной работе №13
subtitle: Фильтр пакетов
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

Получить навыки настройки пакетного фильтра в Linux.

# Ход выполнения работы

## Определение зоны по умолчанию и доступных служб

![Определение зоны и просмотр служб/сервисов](Screenshot_1.png){ width=85% }

## Просмотр конфигурации активной зоны

![Вывод параметров зоны (list-all)](Screenshot_2.png){ width=85% }

## Сравнение list-all и list-all для зоны public

![Вывод list-all для public](Screenshot_3.png){ width=85% }

## Добавление сервиса vnc-server (runtime)

![Добавление vnc-server и проверка наличия](Screenshot_4.png){ width=85% }

## Перезапуск firewalld и сброс runtime-конфигурации

![После restart vnc-server отсутствует](Screenshot_5.png){ width=85% }

## Добавление vnc-server в permanent

![Добавление vnc-server с ключом permanent](Screenshot_6.png){ width=85% }

## Применение permanent-настроек через reload

![После reload vnc-server активен](Screenshot_7.png){ width=85% }

## Добавление порта 2022/tcp в permanent

![Добавление порта 2022/tcp и проверка](Screenshot_8.png){ width=85% }

## Запуск GUI и выбор режима Permanent

![Интерфейс firewall-config и выбор Permanent](Screenshot_9.png){ width=85% }

## Включение служб и добавление порта 2022/udp

![Добавление порта 2022/udp в GUI](Screenshot_10.png){ width=85% }

## Применение изменений в runtime через reload

![После reload изменения применены](Screenshot_11.png){ width=85% }

## Добавление служб imap, pop3, smtp через GUI

![Отметка служб imap/pop3/smtp в зоне public](Screenshot_12.png){ width=85% }

## Добавление telnet и итоговая проверка конфигурации

![Итоговая конфигурация с telnet и другими службами](Screenshot_13.png){ width=85% }

# Итоги работы

## Заключение

Отработаны способы управления firewalld через firewall-cmd и firewall-config.
Проверено различие между runtime и permanent-конфигурациями и порядок применения
изменений (reload). Настроен доступ к службам и портам, обеспечена постоянная
активация конфигурации после перезагрузки системы.
