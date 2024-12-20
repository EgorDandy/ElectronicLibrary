# Диаграмма вариантов использования

![Диаграмма вариантов использования](https://github.com/EgorDandy/ElectronicLibrary/blob/master/image/UseCase.PNG) 
  
# Глоссарий

| Термин | Определение |
|:--|:--|
| Пользователь | Человек, использующий приложение |
| Зарегистрированный пользователь | Пользователь, ранее зарегистрировавшийся в приложении |
  
# Поток событий 

# Содержание
1 [Актёры](#1)  
2 [Варианты использования](#2)  
2.1 [Войти в аккаунт](#3)  
2.2 [Зарегистрироваться](#4)    
2.3 [Просмотр и поиск событий](#5)  
2.4 [Выйти из аккаунта](#6)  
2.5 [Редактировать событие](#7)  
2.6 [Удалить событие](#8)  
2.7 [Добавить событие](#9)     
2.8 [Выделить событие](#10)                                                    
2.9 [Убрать выделенное событие](#11)




# 1 Актёры<a name = '1'></a>

| Актёр | Описание |
|:--|:--|
| Пользователь | Человек, использующий приложение |
| Зарегистрированный пользователь | Пользователь, который зарегистрировался в приложении |

<a name="use_case"/>

# 2 Варианты использования<a name = '2'></a>

<a name="sign_in_to_your_account"/>

## 2.1 Войти в аккаунт<a name = '3'></a>

**Описание.** Вариант использования "Войти в аккаунт" позволяет пользователю войти в учётную запись.  
**Предусловия.** Окно входа в профиль открывается автоматически при запуске приложения.                                      
**Основной поток.**
1. Приложение отображает окно входа в аккаунт;
2. Пользователь вводит данные;
3. Пользователь подтверждает ввод;
4. Приложение запоминает имя пользователя и загружает его данные;
5. Приложение скрывает окно входа в аккаунт;
6. Вариант использования завершается.

**Дополнительная информация.** Пользователь имеет возможность отменить действие. В случае отмены выполняется альтернативный поток А1.

**Альтернативный поток А1.**
1. Приложение скрывает окно входа в аккаунт;
2. Вариант использования завершается досрочно.

<a name="sign_up"/>

## 2.2 Зарегистрироваться<a name = '4'></a>

**Описание.** Вариант использования "Зарегистрироваться" позволяет пользователю создать свой аккаунт в приложении.  
**Предусловия.** Анонимный пользователь захотел зарегистрироваться в приложении, выбрав пункт меню "Регистрация".  
**Основной поток.**
1. Приложение отображает окно регистрации, в котором запрашивает у пользователя ввод данных;
2. Пользователь вводит данные;
3. Пользователь подтверждает ввод;
4. Приложение проверяет введённое имя на совпадение с именами уже зарегистрированных пользователей. Если совпадение выявлено, выполняется альтернативный поток А2;
5. Приложение создает аккаунт пользователя;
6. Приложение скрывает окно регистрации;
7. Вариант использования завершается.

**Альтернативный поток А2.**
1. Приложение сообщает пользователю, что пользователь с таким именем уже существует;
2. Приложение запрашивает у пользователя ввод другого имени;
3. Возврат к п.2 основного потока.

<a name="sign_in_as_visitor"/>

## 2.3 Просмотр и поиск событий<a name = '5'></a>

**Описание.** Любой пользователь может просматривать и искать события в окне поиска.  
**Предусловия.** Пользователь нажал на кнопку "Поиск".  
**Основной поток.**
1. Приложение отображает окно поиска;
2. Пользователь вводит данные в поле ввода;
3. Приложение выполняет поиск по введенным данным и переходик к результату поиска;
4. Вариант использования завершается.

**Дополнительная информация.** Пользователь имеет возможность отменить действие до подтверждения ввода. В случае отмены выполняется альтернативный поток А3.

**Альтернативный поток А3.**
1. Приложение скрывает окно поиска;
2. Вариант использования завершается досрочно.

<a name="view_film_list"/>

## 2.4 Выйти из аккаунта<a name = '6'></a>

**Описание.** Вариант использования "Выйти из аккаунта" позволяет зарегистрированному пользователю выйти из аккаунта.  
**Предусловия.** Зарегистрированный пользователь нажал на кнопку "Выход".  
**Основной поток.**
1. Приложение сбрасывает настройки под пользователя и возвращается к окну входа в аккаунт;
2. Вариант использования завершается.

<a name="find_film_in_list"/>

## 2.6 Удалить событие<a name = '8'></a>

**Описание.** Вариант использования "Удалить событие" позволяет зарегистрированному пользователю удалить своё событие.  
**Предусловия.** Пользователь выполнил действие "Свайп влево" для своего события.  
**Основной поток.**
1. Приложение удаляет событие из общего списка;
2. Вариант использования завершается.

<a name="view_film_info"/>

## 2.7 Добавить событие<a name = '9'></a>

**Описание.** Вариант использования "Добавить событие" позволяет зарегистрированному пользователю создать событие.  
**Предусловия.** Пользователь нажал на кнопку добавления книги.  
**Основной поток.**
1. Вариант использования начинается, когда пользователь нажимает на кнопку добавления книги;
2. Приложение переходит в файловый менеджер для выбора файла;
3. Файловый менеджер закрывается после пользовательского выбора;
4. Приложение выводит окно для ввода автора и названия;
5. Пользователь подтверждает ввод;
6. Приложение добавляет событие;
7. Вариант использования завершается.

<a name="10"/>

## 2.8 Выделить событие<a name = '10'></a>

**Описание.** Вариант использования "Выделить событие" позволяет зарегистрированному пользователю выделить важное событие среди других событий.  
**Предусловия.** Зарегистрированный пользователь нажал на кнопку избранного или сделал "Свайп вправо" для события.  
**Основной поток.**
1. Пользователь нажимает на иконку избранного или делает "Свайп вправо" для одного из событий для добавления его в отдельный список событий;
2. Приложение вносит событие в список избранных событий и обновляет информацию;
3. Вариант использования завершается.

<a name="11"/>

## 2.9 Убрать выделеное событие<a name = '11'></a>

**Описание.** Вариант использования "Убрать выделенное событие" позволяет зарегистрированному пользователю убрать из отдельного списка ранее выделенное событие.  
**Предусловия.** Зарегистрированный пользователь нажал на кнопку избранного или сделал "Свайп вправо" для своего события.  
**Основной поток.**
1. Пользователь нажимает на иконку избранного или делает "Свайп вправо" для одного из событий для удаления из списка избранных событий;
2. Приложение убирает событие из списка избранных событий и обновляет информацию;
3. Вариант использования завершается.
