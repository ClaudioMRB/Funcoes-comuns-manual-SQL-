# Fun-es-comuns-manual-SQL-
UPPER, LOWER, CAST, ROUND, DAY, MONTH, YEAR, EXTRACT, CONCAT, CASE, REPLACE, CHAR_LENGTH E MD5

[MySQL UPPER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_upper.asp) 			[MySQL MONTH() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_month.asp)

[MySQL LOWER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_lower.asp) 		[MySQL YEAR() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_year.asp)

[MySQL CAST() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_cast.asp) 	        [MySQL EXTRACT() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_extract.asp)

[MySQL ROUND() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_round.asp)

[MySQL DAY() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_day.asp)



# ------------------Função MySQL UPPER()--------------

### Exemplo

Converta o texto em maiúsculos:

SELECT UPPER("SQL Tutorial is FUN!");



Busca nomes na tabela independente se está escrito em letras maiúsculas ou minúsculas.

(forçar uma comparação com maiúsculo)

**select** id, **UPPER**(name) from** nome_tabela

**SELECT** id, name **FROM** nome_tabela **WHERE UPPER**(name) **LIKE** 'MAR%'

  

------

## Definição e Uso

A função UPPER() converte uma sequência em maiúsculo superior.

**Nota:** Esta função é igual à função [UCASE().](https://www.w3schools.com/sql/func_mysql_ucase.asp)

## Sintaxe

UPPER(*text*)

## Valores dos parâmetros

| Parameter | Description                     |
| :-------- | :------------------------------ |
| *text*    | Required. The string to convert |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Converta o texto em "CustomerName" em maiúsculo:

SELECT UPPER(CustomerName) AS UppercaseCustomerName
FROM Customers;



# ------------Função MySQL LOWER()-------------------

### Exemplo

Converta o texto em minúscula:

SELECT LOWER("SQL Tutorial is FUN!");



Busca nomes na tabela independente se está escrito em letras maiúsculas ou minúsculas.

(forçar uma comparação com minúsculo)

**select** id, **LOWER**(name) from** nome_tabela

**SELECT** id, name **FROM** nome_tabela **WHERE LOWER**(name) **LIKE** 'mar%'

------

## Definição e Uso

A função LOWER() converte uma sequência em minúscula.

**Nota:** A função [LCASE()](https://www.w3schools.com/sql/func_mysql_lcase.asp) é igual à função LOWER().

## Sintaxe

LOWER(*text*)

## Valores dos parâmetros

| Parameter | Description                     |
| :-------- | :------------------------------ |
| *text*    | Required. The string to convert |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Converta o texto em "CustomerName" para minúscula:

SELECT LOWER(CustomerName) AS LowercaseCustomerName
FROM Customers;



# -------------Função MySQL CAST()---------------------

### Exemplo

Converta um valor em um datatype DATA:

SELECT CAST("2017-08-29" AS DATE);

 **EXEMPLO 2**

**SELECT** coluna, coluna, **ROUND** (**CAST** (coluna **AS** numeric), decimal), quantity from nome_tabela



------

## Definição e Uso

A função CAST() converte um valor (de qualquer tipo) no tipo de dados especificado.

**Ponta:** Veja também a função [CONVERT().](https://www.w3schools.com/sql/func_mysql_convert.asp)

## Sintaxe

CAST(*value* AS *datatype*)

## Valores dos parâmetros

## Detalhes técnicos

| Parameter  | Description                                                  |
| :--------- | :----------------------------------------------------------- |
| *value*    | Required. The value to convert                               |
| *datatype* | Required. The datatype to convert to. Can be one of the following: |

| datatype (Value) | Description                                                  |
| :--------------- | :----------------------------------------------------------- |
| DATE             | Converts *value* to DATE. Format: "YYYY-MM-DD"               |
| DATETIME         | Converts *value* to DATETIME. Format: "YYYY-MM-DD HH:MM:SS"  |
| DECIMAL          | Converts *value* to DECIMAL. Use the optional M and D parameters to specify the maximum number of digits (M) and the number of digits following the decimal point (D). |
| TIME             | Converts *value* to TIME. Format: "HH:MM:SS"                 |
| CHAR             | Converts *value* to CHAR (a fixed length string)             |
| NCHAR            | Converts *value* to NCHAR (like CHAR, but produces a string with the national character set) |
| SIGNED           | Converts *value* to SIGNED (a signed 64-bit integer)         |

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Converta um valor em um tipo de dados CHAR:

SELECT CAST(150 AS CHAR);

### Exemplo

Converta um valor em um datatype TIME:

SELECT CAST("14:06:10" AS TIME);

### Exemplo

Converta um valor em um tipo de dados ASSINADO:

SELECT CAST(5-10 AS SIGNED);



# -----------Função MySQL ROUND()-------------------

### Exemplo

Arredondar o número para 2 casas decimais:

**SELECT ROUND**(135.375, 2);

RESULTADO: 135,38

**ou**

**SELECT** coluna, coluna, **ROUND** (coluna, decimal), quantity from nome_tabela

------

## Definição e Uso

A função ROUND() gira em torno de um número para um número especificado de casas decimais.

**Nota:** Veja também as funções [FLOOR()](https://www.w3schools.com/sql/func_mysql_floor.asp), [CEIL()](https://www.w3schools.com/sql/func_mysql_ceil.asp), [CEILING()](https://www.w3schools.com/sql/func_mysql_ceiling.asp)e [TRUNCATE().](https://www.w3schools.com/sql/func_mysql_truncate.asp)

## Sintaxe

ROUND(*number*, *decimals*)

## Valores dos parâmetros

| Parameter  | Description                                                  |
| :--------- | :----------------------------------------------------------- |
| *number*   | Required. The number to be rounded                           |
| *decimals* | Optional. The number of decimal places to round *number* to. If omitted, it returns the integer (no decimals) |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Arredondar o número para 0 casas decimais:

SELECT ROUND(345.156, 0);

### Exemplo

Rodada da coluna Preço (para 1 decimal) na tabela "Produtos":

SELECT ProductName, Price, ROUND(Price, 1) AS RoundedPrice
FROM Products;



# --------------Função MySQL DAY ()---------------------

### Exemplo

Retorne o dia do mês para uma data:

SELECT DAY("2017-06-15");



**EXEMPLO 2**

extrair o dia da data registrada.

**SELECT** id, date, price,**CAST** ( **EXTRACT** (**DAY FROM** date) **AS** int) **AS** novo_nome_da_coluna **FROM** tb_sale;

**CAST**(Parâmetro), numeric_types)

------

## Definição e Uso

A função DAY() retorna o dia do mês para uma determinada data (número de 1 a 31).

**Nota:** Esta função é igual à função [DAYOFMONTH().](https://www.w3schools.com/sql/func_mysql_dayofmonth.asp)

## Sintaxe

DAY(*date*)

## Valores dos parâmetros

| Parameter | Description                                |
| :-------- | :----------------------------------------- |
| *date*    | Required. The date to extract the day from |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Retorne o dia do mês para uma data:

SELECT DAY("2017-06-15 09:34:21");

### Exemplo

Retorne o dia do mês para a data atual do sistema:

SELECT DAY(CURDATE());



# -----------------Função MySQL MONTH ()------------

### Exemplo

Devolva a parte do mês de uma data:

SELECT MONTH("2017-06-15");



**EXEMPLO 2**

extrair o mês da data registrada.

**SELECT** id, date, price,**CAST** ( **EXTRACT** (**MONTH FROM** date) **AS** int) **AS** novo_nome_da_coluna **FROM** tb_sale;

**CAST**(Parâmetro), numeric_types)

------

## Definição e Uso

A função MONTH() retorna a parte do mês para uma determinada data (número de 1 a 12).

## Sintaxe

MONTH(*date*)

## Valores dos parâmetros

| Parameter | Description                                              |
| :-------- | :------------------------------------------------------- |
| *date*    | Required. The date or datetime to extract the month from |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Devolva a parte do mês de uma data:

SELECT MONTH("2017-06-15 09:34:21");

### Exemplo

Devolva a parte do mês da data atual do sistema:

SELECT MONTH(CURDATE());



# -------------Função MySQL YEAR()---------------------

### Exemplo

Devolva a parte do ano de uma data:

SELECT YEAR("2017-06-15");



**EXEMPLO 2**

extrair o ano da data registrada.

**SELECT** id, date, price,**CAST** ( **EXTRACT** (**YEAR FROM** date) **AS** int) **AS** novo_nome_da_coluna **FROM** tb_sale;

**CAST**(Parâmetro), numeric_types)

------

## Definição e Uso

A função year() retorna a parte do ano para uma determinada data (número de 1000 a 9999).

## Sintaxe

YEAR(*date*)

## Valores dos parâmetros

| Parameter | Description                                          |
| :-------- | :--------------------------------------------------- |
| *date*    | Required. The date/datetime to extract the year from |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Devolva a parte do ano de uma data:

SELECT YEAR("2017-06-15 09:34:21");

### Exemplo

Retorne a parte do ano da data atual do sistema:

SELECT YEAR(CURDATE());



# ---------------Função mysql extract()-----------------

### Exemplo

Extrair o mês de uma data:

SELECT EXTRACT(MONTH FROM "2017-06-15");



**EXEMPLO 2**

vai exibir apenas os registros onde o dia do ano seja igual a 18.

**SELECT** id, date, price,**CAST** ( **EXTRACT** (**DAY FROM** date) **AS** int) **AS** novo_nome_da_coluna **FROM** tb_sale **WHERE EXTRACT** ( **DAY FROM** date ) = 18 ;

**SELECT** id, date, price,**CAST** ( **EXTRACT** (**DAY FROM** date) **AS** int) **AS** novo_nome_da_coluna **FROM** tb_sale **WHERE EXTRACT** ( **YEAR FROM** date ) = 2022 **AND EXTRACT** ( **MONTH FROM** date ) = 5 ;



**CAST**(Parâmetro), numeric_types)

------

## Definição e Uso

A função EXTRA() extrai uma parte de uma determinada data.

## Sintaxe

EXTRACT(*part* FROM *date*)

## Valores dos parâmetros

| Parameter | Description                                                 |
| :-------- | :---------------------------------------------------------- |
| *part*    | Required. The part to extract. Can be one of the following: |

-  MICROSECOND

- SECOND

- MINUTE

- HOUR

- DAY

- WEEK

- MONTH

- QUARTER

- YEAR

- SECOND_MICROSECOND

- MINUTE_MICROSECOND

- MINUTE_SECOND

- HOUR_MICROSECOND

- HOUR_SECOND

- HOUR_MINUTE

- DAY_MICROSECOND

- DAY_SECOND

- DAY_MINUTE

- DAY_HOUR

- YEAR_MONTH

  

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Extrair a semana de uma data:

SELECT EXTRACT(WEEK FROM "2017-06-15");

### Exemplo

Extrair o minuto de um horário de encontro:

SELECT EXTRACT(MINUTE FROM "2017-06-15 09:34:21");

### Exemplo

Extrair o ano e o mês de uma data:

SELECT EXTRACT(YEAR_MONTH FROM "2017-06-15 09:34:21");
