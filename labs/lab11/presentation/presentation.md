---
## Front matter
lang: ru-RU
title: "Лабораторная работа №11"
subtitle: "Управление загрузкой системы (GRUB2)"
author:
  - "Щемелев Илья Владимирович"

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
Получить навыки работы с загрузчиком системы **GRUB2** в ОС **Rocky Linux**: изменение параметров загрузки, запуск в специальных режимах systemd и восстановление доступа (сброс пароля root).

# Ход выполнения

## Редактирование /etc/default/grub

![Редактирование файла /etc/default/grub](Screenshot_1.png){ width=85% }

## Генерация новой конфигурации GRUB2

![Генерация конфигурации GRUB2](Screenshot_2.png){ width=85% }

## Проверка меню загрузчика после перезагрузки

![Меню загрузчика GRUB](Screenshot_3.png){ width=85% }

## Редактирование параметров записи загрузки

![Редактирование параметров загрузки ядра](Screenshot_4.png){ width=85% }

## Проверка окружения rescue.target

![Список загруженных модулей systemd](Screenshot_5.png){ width=85% }

## Переход в emergency.target через параметры ядра

![Загрузка в режиме emergency.target](Screenshot_6.png){ width=85% }

## Проверка минимального набора модулей

![Минимальный набор загруженных модулей](Screenshot_7.png){ width=85% }

## Остановка загрузки на этапе initramfs (rd.break)

![Загрузка в режиме rd.break](Screenshot_8.png){ width=85% }

## Действия в окружении восстановления

![Установлен новый пароль](Screenshot_9.png){ width=85% }

# Итоги работы

## Заключение

В работе изучены практические приёмы управления загрузчиком **GRUB2** в **Rocky Linux**: изменение параметров меню загрузки, запуск системы в режимах **rescue** и **emergency**, а также восстановление доступа путём сброса пароля **root** с учётом требований **SELinux**.
