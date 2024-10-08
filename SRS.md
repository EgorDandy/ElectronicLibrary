# Требования к проекту
---

# Содержание
1 [Введение](#intro)  
1.1 [Назначение](#appointment)  
1.2 [Бизнес-требования](#business_requirements)  
1.2.1 [Исходные данные](#initial_data)  
1.2.2 [Возможности бизнеса](#business_opportunities)  
1.2.3 [Границы проекта](#project_boundary)  
1.3 [Аналоги](#analogues)  
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)    
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)   
3.2 [Нефункциональные требования](#non-functional_requirements)  

<a name="intro"/>

# 1 Введение

<a name="appointment"/>

## 1.1 Назначение
В этом документе описаны функциональные и нефункциональные требования к мобильному приложению «LibNet» для ОС Android. 

<a name="business_requirements"/>

## 1.2 Бизнес-требования

<a name="initial_data"/>

### 1.2.1 Исходные данные
Многие люди любят с головой погружаться в вымышленные миры и в этом им помогают книги. У каждого есть свои предпочтения — от классических произведений до зарубежной фантастики. Иногда читатели увлекаются целой коллекцией книг или могут зацикливаться на произведениях одного автора. В этом случае пользователи обращаются к интернету, где могут найти множество ресурсов.

Однако не всегда есть возможность почитать книги в интернете. В такие моменты было бы очень удобным открыть какое-нибудь приложение на своём устройстве с уже скачанными книгами, быстро найти желаемую и погрузиться в приключения любимых героев. Именно для таких случаев и нужно наше приложение.

<a name="business_opportunities"/>

### 1.2.2 Возможности бизнеса
Приложение библиотеки предоставляет удобный интерфейс для любителей почитать. Во-первых, книги можно искать и скачивать прямо в самом приложении, что позволяет через одно приложение искать, скачивать и читать любимые произведения. Во-вторых, скачанные книги будут легко доступны в одном месте, что позволит не отрываться от чтения даже при отсутствии подключения к сети интернет, например в долгих поездках.

<a name="project_boundary"/>

### 1.2.3 Границы проекта
Приложение LibNet будет искать книги по сети интернет и не будет иметь собственную базу с книгами, если книги нет нигде в интернете для скачивания, то и приложении её скачать будет нельзя.

<a name="analogues"/>

## 1.3 Аналоги
Аналогами являются такие приложения как PocketBook Reader, Moon+Reader.

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы
Продукт будет взаимодействовать с несколькими внешними системами:

•	Firebase Authentication для авторизации и хранения данных пользователей.

•	Lib Database для локального хранения книг и информации о них.


<a name="user_interface"/>

## 2.2 Интерфейс пользователя
Окно загрузки приложения.  

![Окно загрузки приложения](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Loading.PNG)  

Окно регистрации нового пользователя.  

![Окно регистрации нового пользователя](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Registration.PNG)

Окно входа для зарегистрированного пользователя.  

![Окно входа для зарегистрированного пользователя](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Sign.PNG)

Окно моя библиотека. 

![Моя библиотека](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/MyLibrary.PNG)

Окно избранное. 

![Окно избранное](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Favorites.PNG)

Окно мой аккаунт. 

![Окно мой аккаунт](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Account.PNG)

Окно поиск. 

![Поиск](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Search.PNG)

Окно меню

![Меню](https://github.com/EgorDandy/ElectronicLibrary/blob/master/mockups/Menu.PNG)

<a name="user_specifications"></a>
### **2.3 Характеристики пользователей:**

Читатели - люди, желающее насладится интересными произведениями. Уровень опыта — разный, от новичков до заядлых читателей. Возрастная группа варьируется от молодых людей до пенсионеров. Они ценят удобство поиска и предлагаемый ассортимент.

<a name="assumptions_and_dependencies"></a>
### **2.4 Предположения и зависимости:**

•	Пользователям необходимо скачивать книги, чтобы у них точно была возможность прочитать их в любое время.

•	Приложение будет работать только на устройствах с Android 6.0 и выше.

<a name="system_requirements"></a>
## **3. Системные требования**

<a name="functional_requirements"></a>
### **3.1 Функциональные требования:**

•   Приложение должно позволять пользователям искать, читать, скачивать и удалять книги.
	
•	Приложение должно позволять пользователям отбирать наиболее интересные книги и помечать их, для удобного и быстрого доступа.
	
•	Авторизация должна быть обязательной для отбора списка книг конкретного пользователя.

<a name="non-functional_requirements"></a>
### **3.2 Нефункциональные требования:**

•	Надёжность: Приложение должно быть устойчивым к потерям соединения с интернетом, с возможностью локального хранения данных и последующей синхронизации.

•	Безопасность: Данные пользователей должны быть защищены, а авторизация — проводиться через надёжную систему (например, Firebase Authentication).

•	Производительность: Приложение должно загружаться и работать плавно на большинстве современных устройств.

•	Удобство использования: Интерфейс должен быть интуитивно понятным, особенно для пользователей с базовыми техническими навыками.
