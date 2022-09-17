# Fun-es-comuns-manual-SQL-
UPPER, LOWER, CAST, ROUND, DAY, MONTH, YEAR, EXTRACT, CONCAT, CASE, REPLACE, CHAR_LENGTH E MD5

[MySQL UPPER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_upper.asp)	

[MySQL LOWER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_lower.asp)

[MySQL CAST() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_cast.asp)

[MySQL ROUND() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_round.asp)

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
