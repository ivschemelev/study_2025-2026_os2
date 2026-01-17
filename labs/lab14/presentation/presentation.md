---
## Front matter
lang: ru-RU
title: Лабораторная работа №14
subtitle: Партиции, файловые системы, монтирование
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

Получить навыки создания разделов на диске и файловых систем, а также навыки монтирования файловых систем в Linux.

# Ход выполнения работы

## Исходное состояние дисков

![Просмотр списка дисков и текущей разметки](Screenshot_1.png){ width=85% }

## Запуск fdisk и просмотр справки

![Запуск fdisk и список команд](Screenshot_2.png){ width=85% }

## Создание основного MBR-раздела

![Создание первичного раздела на /dev/sdb](Screenshot_3.png){ width=85% }

## Сравнение fdisk и /proc/partitions

![Проверка таблицы разделов и /proc/partitions](Screenshot_4.png){ width=85% }

## Логические разделы в MBR

![Создание расширенного и логического разделов](Screenshot_5.png){ width=85% }

## Проверка созданных разделов MBR

![Проверка структуры разделов на /dev/sdb](Screenshot_6.png){ width=85% }

## Создание swap в MBR

![Создание и назначение типа swap-раздела](Screenshot_7.png){ width=85% }

## Активация swap и проверка

![Подготовка swap и проверка через free](Screenshot_8.png){ width=85% }

## Проверка диска под GPT

![Проверка таблиц разделов на /dev/sdc](Screenshot_9.png){ width=85% }

## Создание GPT-раздела через gdisk

![Создание раздела GPT и запись изменений](Screenshot_10.png){ width=85% }

## Проверка GPT-разметки

![Проверка GPT и protective MBR](Screenshot_11.png){ width=85% }

## Форматирование XFS и метка

![Создание XFS и установка метки xfsdisk](Screenshot_12.png){ width=85% }

## Форматирование EXT4 и параметры

![Создание EXT4, метка ext4disk и опции монтирования](Screenshot_13.png){ width=85% }

## Ручное монтирование и отмонтирование

![Монтирование /dev/sdb5 в /mnt/tmp и проверка](Screenshot_14.png){ width=85% }

## Определение UUID устройств

![Получение UUID и параметров через blkid](Screenshot_15.png){ width=85% }

## Настройка /etc/fstab для XFS

![Добавление записи в /etc/fstab для /mnt/data](Screenshot_16.png){ width=85% }

## Проверка mount -a и df -h

![Проверка автоматического монтирования](Screenshot_17.png){ width=85% }

# Самостоятельная работа

## Добавление разделов на GPT-диске

![Создание дополнительных GPT-разделов и partprobe](Screenshot_18.png){ width=85% }

## EXT4 для /dev/sdc2 и swap для /dev/sdc3

![Форматирование ext4 и создание swap](Screenshot_19.png){ width=85% }

## UUID для новых разделов

![Проверка UUID разделов /dev/sdc2 и /dev/sdc3](Screenshot_20.png){ width=85% }

## /etc/fstab для /mnt/data-ext и swap

![Добавление записей ext4 и swap в /etc/fstab](Screenshot_21.png){ width=85% }

## Проверка после перезагрузки

![Проверка mount, free и df -h после перезагрузки](Screenshot_22.png){ width=85% }

# Итоги работы

## Заключение

Выполнена разметка дисков в схемах MBR и GPT, созданы разделы под Linux и swap, сформированы файловые системы XFS и EXT4 с метками и параметрами. Настроены ручное и автоматическое монтирование через /etc/fstab, выполнена проверка работоспособности конфигурации и подтверждена корректность настройки после перезагрузки.
