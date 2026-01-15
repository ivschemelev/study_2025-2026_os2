---
## Front matter
lang: ru-RU
title: Лабораторная работа №2
subtitle: Управление пользователями и группами
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

Получить представление о работе с учётными записями пользователей и группами пользователей в операционной системе типа Linux.

# Ход выполнения работы

## Определение текущего пользователя и переключение на root

![Определение текущего пользователя и вывод id, переключение su](Screenshot_1.png){ width=85% }

## Просмотр /etc/sudoers в безопасном режиме

![Открытие файла /etc/sudoers через visudo](Screenshot_2.png){ width=85% }

## Правило для группы wheel в sudoers

![Строка %wheel ALL=(ALL) ALL в /etc/sudoers](Screenshot_3.png){ width=85% }

## Создание пользователей alice и bob

![Проверка id alice, установка пароля и создание пользователя bob](Screenshot_4.png){ width=85% }

## Настройка параметров создания пользователей

![Изменение параметров в /etc/login.defs](Screenshot_5.png){ width=85% }

## Настройка редактора по умолчанию в /etc/skel

![Добавление переменной EDITOR в /etc/skel/.bashrc](Screenshot_6.png){ width=85% }

## Шаблон домашнего каталога и создание carol

![Создание каталогов в /etc/skel и проверка домашнего каталога carol](Screenshot_7.png){ width=85% }

## Анализ /etc/shadow и политика пароля carol

![Просмотр записи carol в /etc/shadow и изменение срока действия пароля](Screenshot_8.png){ width=85% }

## Создание групп и назначение пользователей

![Создание групп main/third, usermod и проверка id пользователей](Screenshot_9.png){ width=85% }

# Итоги работы

## Заключение

В ходе лабораторной работы выполнены переключение учётных записей и анализ UID/GID, изучены принципы предоставления прав через sudo и группа wheel. Созданы пользователи и группы, изменены параметры их создания с использованием /etc/login.defs и /etc/skel, а также рассмотрены механизмы хранения данных в /etc/passwd, /etc/shadow и /etc/group. Отработано управление политикой паролей и назначение пользователей в дополнительные группы.
