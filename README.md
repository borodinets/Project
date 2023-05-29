# Проф. задание для Junior .NET-разработчик 


# Приложение учета домашней бухгалтерии



Данное приложение предназначено для учета доходов и расходов в домашней бухгалтерии. Пользователь может добавлять записи о своих доходах и расходах, указывая категорию, сумму и дату операции. 



## Функциональность

- создать источник доходов и расходов (Профиль)

- Добавление записей о доходах и расходах:
  - Пользователь может указать категорию, сумму и дату операции для каждой записи, а также оставть комментарий.
- Просмотр ежемесячной статистики:
  - Пользователь может просмотреть список доходов и расходов за определенный месяц.
  - Статистика представлена в виде списка, где для каждой операции указана категория, сумма и дата.
- В меню можно увидеть историю операций и общий доход
- Также данное приложение созданно для учёта семейного буджета и в нём можно создать и запись несколько членов семьи; учитывать его доходы и расходы . видить его вклад отделно 

## Технические детали

- Язык программирования:С#
- База данных:MSSQL Server
- Структура базы данных:
  - Таблица "Acc" для хранения : ID, Имя и сумма.



код для создания стола 





  CREATE TABLE [dbo].[Acc] 

(
  
    [Id]     INT     IDENTITY (1,1)   NOT NULL,

    [Name]   NCHAR(30) NULL,

    [Amount] NCHAR(20)        NULL, 

    PRIMARY KEY CLUSTERED ([Id] ASC)
    
);

В конфиге прописать 

<connectionStrings>
		<add name="Database1" connectionString="ваш путь к базе" />
	</connectionStrings>



## Зависимости
 Используются пакеты
- LiveCharts
- LiveCharts.Wpf
- MaterialDesignColors
- MaterialDesignThemes
- Microsoft.Xaml.Behaviors.Wpf
- Newtonsoft.Json


## Примеры использования

имеется 4 вкладки 
  1. Главное меню ; видны статистика , истроия , общяя сумма.
  2. Профиль; Создание уч. записи (можно удалить )
  3. Доходы .создать новую запись о доходе и просмотреть все остальные операции (можно редактировать или удалить)
  4. Расходы .создать новую запись о расходе и просмотреть все остальные операции (можно редактировать или удалить)
