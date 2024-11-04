# Диаграмма вариантов использования

![Диаграмма вариантов использования](https://github.com/alwayswnnasleep/ZedkaShop/blob/master/docs/Diagrams/images/UseCase.png) 
  
# Глоссарий

| Термин | Определение |
|:--|:--|
| Пользователь | Человек, использующий приложение |
| Зарегистрированный пользователь | Пользователь, ранее зарегистрировавшийся в приложении |
| Посетитель | Пользователь, использующий приложение без авторизации |  
  
# Поток событий 

# Содержание

1. [Актёры](#actors)

2. [Варианты использования](#use_case)

   2.1 [Войти в аккаунт](#sign_in_to_your_account)

   2.2 [Зарегистрироваться](#sign_up)

   2.3 [Просмотр и поиск товара](#see_products)

   2.4 [Выйти из аккаунта](#signout)

   2.5 [Редактировать товар](#edit_product)

   2.6 [Удалить товар](#delete_product)

   2.7 [Добавить товар](#add_product)

   2.8 [Добавить товар в корзину](#add_to_cart)

   2.9 [Просмотреть историю покупок](#see_history_buy)

   2.10 [Просмотреть историю просмотров](#see_history_view)

   2.11 [Купить товар](#purchase_product)

<a name="actors"/>

# 1 Актёры

| Актёр | Описание |
|:--|:--|
| Пользователь | Человек, использующий приложение |
| Посетитель | Пользователь, который использует приложение без регистрации в нём |
| Зарегистрированный пользователь | Пользователь, который зарегистрировался в приложении |

<a name="use_case"/>

# 2 Варианты использования

<a name="sign_in_to_your_account"/>

## 2.1 Войти в аккаунт

**Описание.** Вариант использования "Войти в аккаунт" позволяет пользователю войти в учётную запись.  
**Предусловия.** Пользователь выбрал способ "Вход" для входа в приложение.  
**Основной поток.**
1. Приложение отображает окно входа в аккаунт;
2. Пользователь вводит данные;
3. Пользователь подтверждает ввод;
4. Приложение запоминает имя пользователя и загружает его данные;
5. Приложение скрывает окно входа в аккаунт;
6. Вариант использования завершается.

<a name="sign_up"/>

## 2.2 Зарегистрироваться

**Описание.** Вариант использования "Зарегистрироваться" позволяет пользователю создать свой аккаунт в приложении.  
**Предусловия.** Анонимный пользователь захотел зарегистрироваться в приложении, выбрав пункт меню "Регистрация".  
**Основной поток.**
1. Приложение отображает окно регистрации, в котором запрашивает у пользователя ввод данных;
2. Пользователь вводит данные;
3. Пользователь подтверждает ввод;
4. Приложение проверяет введённое имя на совпадение с именами уже зарегистрированных пользователей. Если совпадение выявлено, выполняется альтернативный поток А1;
5. Приложение создает аккаунт пользователя в базе данных;
6. Приложение скрывает окно регистрации;
7. Вариант использования завершается.

**Альтернативный поток А1.**
1. Приложение сообщает пользователю, что пользователь с таким именем уже существует;
2. Приложение запрашивает у пользователя ввод другого имени;
3. Возврат к п.2 основного потока.

<a name="see_products"/>

## 2.3 Просмотр и поиск товаров

**Описание.** Любой пользователь может просматривать и искать товары в окне поиска.  
**Предусловия.** Пользователь нажал на кнопку "Поиск".  
**Основной поток.**
1. Приложение отображает окно поиска;
2. Пользователь вводит данные в поле ввода.
3. Приложение выполняет поиск по введенным данным и переходик к результату.
4. Вариант использования завершается.

**Дополнительная информация.** Пользователь имеет возможность отменить действие до подтверждения ввода. В случае отмены выполняется альтернативный поток А2.

**Альтернативный поток А2.**
1. Приложение скрывает окно поиска;
2. Вариант использования завершается досрочно.

<a name="signout"/>

## 2.4 Выйти из аккаунта

**Описание.** Вариант использования "Выйти из аккаунта" позволяет зарегистрированному пользователю выйти из аккаунта.  
**Предусловия.** Зарегистрированный пользователь нажал на кнопку "Выход".  
**Основной поток.**
1. Приложение сбрасывает настройки под пользователя и переводит его в разряд анонимных пользователей;
2. Вариант использования завершается.

<a name="edit_product"/>

## 2.5 Редактировать товар

**Описание.** Вариант использования "Редактировать товар" позволяет зарегистрированному пользователю отредактировать созданные им события.  
**Предусловия.** Пользователь нажал на кнопку "Редактровать" для своего события.  
**Основной поток.**
1. Приложение выводит окно редактирования товара;
2. Пользователь изменяет необходимые данные;
3. Пользователь подтверждает ввод;
4. Приложение обновляет данные о товаре;
5. Вариант использования завершается.

<a name="delete_product"/>

## 2.6 Удалить товар

**Описание.** Вариант использования "Удалить товар" позволяет зарегистрированному пользователю удалить своё событие.  
**Предусловия.** Пользователь нажал кнопку "Удалить" для своего товара.  
**Основной поток.**
1. Приложение удаляет товар из списка и базы данных;
2. Вариант использования завершается.

<a name="add_product"/>

## 2.7 Добавить товар

**Описание.** Вариант использования "Просмотреть информацию о товаре" отображает полную информацию о товаре.  
**Предусловия.** Пользователь нажал на товар коротким нажатием.  
**Основной поток.**
1. Вариант использования начинается, когда пользователь выбирает товар в листе коротким нажатием;
2. Приложение получает название выбранного листе;
3. Приложение отображает информацию о фильме;
4. Вариант использования завершается.

**Описание.** Вариант использования "Добавить товар" позволяет зарегистрированному пользователю создать товар.  
**Предусловия.** Пользователь нажал на кнопку "Добавить товар".  
**Основной поток.**
1. Приложение отображает окно добавления товара, в котором запрашивает у пользователя ввод данных;
2. Пользователь вводит данные;
3. Пользователь подтверждает ввод;
4. Приложение проверяет введённые данные на совпадение с существующими событиями. Если совпадение выявлено, выполняется альтернативный поток А3;
5. Приложение создает товар и отображает его на странице товаров;
6. Приложение скрывает окно добавления товара;
7. Вариант использования завершается.

**Альтернативный поток А3.**
1. Приложение сообщает пользователю, что такое товар уже существует;
2. Приложение запрашивает у пользователя ввод других данных;
3. Возврат к п.2 основного потока.

<a name="add_to_cart"/>

## 2.8 Добавить товар в корзину

**Описание.** Вариант использования "Добавить товар в корзину" позволяет зарегистрированному пользователю добавить товар в корзину.  
**Предусловия.** Пользователь нажал на кнопку "Добавить товар в корзину".  
**Основной поток.**
1. Приложение отображает иконку добавления товара в корзину
2. Пользователь нажимает на иконку;
3. Приложение добавляет товар в корзину и отображает его на странице корзины пользователя;
4. Вариант использования завершается.

**Альтернативный поток А4.**
1. Приложение сообщает пользователю, что такое товар уже добавлен в корзину;
2. Возврат к п.1 основного потока.

<a name="see_history_buy"/>

## 2.9 Просмотр истории покупок

**Описание.** Вариант использования "Просмотр истории покупок" позволяет зарегистрированному пользователю просмотреть список всех совершенных покупок.
**Предусловия.** Пользователь вошел в свою учетную запись и совершил покупку.
**Основной поток.**
1. Пользователь переходит на страницу "История покупок";
2. Приложение запрашивает и загружает данные о покупках пользователя;
3. Приложение отображает список всех совершенных покупок с деталями (дата, сумма, товары);
4. Пользователь может выбрать конкретную покупку для просмотра дополнительных деталей;
5. Вариант использования завершается.

**Альтернативный поток А5**
1. Приложение сообщает пользователю, что у него нет совершенных покупок.
2. Приложение предлагает пользователю перейти в магазин для совершения новой покупки.
3. Вариант использования завершается.

<a name="see_history_view"/>

## 2.10 Просмотр истории просмотров

**Описание.** Вариант использования "Просмотр истории просмотров" позволяет зарегистрированному пользователю просмотреть список всех товаров, которые он ранее просматривал.	
**Предусловия.** Пользователь нажал на кнопку "Просмотреть историю" в меню профиля.
**Основной поток.**
1. Пользователь переходит на страницу "История просмотров";
2. Приложение запрашивает и загружает данные о товарах, которые пользователь просматривал;
3. Приложение отображает список всех просмотренных товаров с деталями (название, дата просмотра, изображение);
4. Пользователь может выбрать конкретный товар для просмотра подробной информации;
5. Вариант использования завершается.

**Альтернативный поток А6.**

1. Приложение сообщает пользователю, что у него нет истории просмотров.
2. Приложение предлагает пользователю перейти в магазин для просмотра новых товаров.
3. Вариант использования завершается.

<a name="purchase_product"/>

## 2.11 Купить товар

**Описание.** Вариант использования "Покупка товара" позволяет зарегистрированному пользователю приобрести товар.
**Предусловия.** Пользователь добавил товар в корзину и нажал на кнопку "Оформить заказ".
**Основной поток.**
1. Пользователь переходит на страницу оформления заказа;
2. Приложение отображает список товаров в корзине с деталями (название, цена, количество);
3. Пользователь выбирает способ доставки и оплату;
4. Пользователь подтверждает покупку, нажав кнопку "Подтвердить заказ";
5. Приложение обрабатывает заказ и отображает сообщение о успешной покупке;
6. Вариант использования завершается.

**Альтернативный поток А7.**
1. Приложение сообщает пользователю о возникшей ошибке при обработке заказа (например, недостаточно средств).
2. Пользователь может изменить способ оплаты или вернуться в корзину для редактирования заказа.
3. Вариант использования завершается.