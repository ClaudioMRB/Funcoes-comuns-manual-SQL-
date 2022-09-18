# Fun-es-comuns-manual-SQL-
UPPER, LOWER, CAST, ROUND, DAY, MONTH, YEAR, EXTRACT, CONCAT, CASE, REPLACE, CHAR_LENGTH E MD5

[MySQL UPPER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_upper.asp) 	    	[MySQL MONTH() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_month.asp)

[MySQL LOWER() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_lower.asp) 	    	[MySQL YEAR() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_year.asp)

[MySQL CAST() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_cast.asp) 	            [MySQL EXTRACT() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_extract.asp)

[MySQL ROUND() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_round.asp)             [SQL CASE Expression (w3schools.com)](https://www.w3schools.com/sql/sql_case.asp)

[MySQL DAY() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_day.asp)                    [MySQL REPLACE() Function (w3schools.com)](https://www.w3schools.com/sql/func_mysql_replace.asp)

[Função MySQL CHAR_LENGTH() (w3schools.com)](https://www.w3schools.com/sql/func_mysql_char_length.asp)

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



# --------------Função MySQL CONCAT()---------------

[❮ Anterior](https://www.w3schools.com/sql/func_mysql_character_length.asp)[funções mysql ❮](https://www.w3schools.com/sql/sql_ref_mysql.asp)[Próxima ❯](https://www.w3schools.com/sql/func_mysql_concat_ws.asp)

### Exemplo

Adicione várias strings juntas:

SELECT CONCAT("SQL ", "Tutorial ", "is ", "fun!") AS ConcatenatedString;

------

## Definição e Uso

A função CONCAT() adiciona duas ou mais expressões juntas.

**Nota:** Veja também a função [CONCAT_WS().](https://www.w3schools.com/sql/func_mysql_concat_ws.asp)



## Sintaxe

CONCAT(*expression1*, *expression2*, *expression3*,...)

## Valores dos parâmetros

| Parameter                                     | Description                                                  |
| :-------------------------------------------- | :----------------------------------------------------------- |
| *expression1, expression2, expression3, etc.* | Required. The expressions to add together.**Note:** If any of the expressions is a NULL value, it returns NULL |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Adicione três colunas em uma coluna "Endereço":

SELECT CONCAT(Address, " ", PostalCode, " ", City) AS Address
FROM Customers;

**Exemplo 2**

**SELECT** *, **CONCAT** (**EXTRACT**(**MONTH FROM** date), '/', **EXTRACT**(**YEAR FROM** date)) **AS** mes_ano **FROM** tb_sale

## -----------------A Expressão DE CASE SQL------------------------

A expressão passa por condições e retorna um valor quando a primeira condição é atendida (como uma declaração se-então-então-outra). Assim, uma vez que uma condição é verdadeira, ele vai parar de ler e retornar o resultado. Se nenhuma condição for verdadeira, ele devolve o valor na cláusula. `CASE``ELSE`

Se não houver parte e nenhuma condição for verdadeira, ela retorna NULL.`ELSE`

## Sintaxe case

CASE
  WHEN *condition1* THEN *result1*
  WHEN *condition2* THEN *result2*
  WHEN *conditionN* THEN *resultN*
  ELSE *result*
END;

------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "OrderDetails" no banco de dados de amostras northwind:

| OrderDetailID | OrderID | ProductID | Quantity |
| :------------ | :------ | :-------- | :------- |
| 1             | 10248   | 11        | 12       |
| 2             | 10248   | 42        | 10       |
| 3             | 10248   | 72        | 5        |
| 4             | 10249   | 14        | 9        |
| 5             | 10249   | 51        | 40       |

------

## Exemplos de casos SQL

O SQL a seguir passa por condições e retorna um valor quando a primeira condição é atendida:

### Exemplo

SELECT OrderID, Quantity,
CASE
  WHEN Quantity > 30 THEN 'The quantity is greater than 30'
  WHEN Quantity = 30 THEN 'The quantity is 30'
  ELSE 'The quantity is under 30'
END AS QuantityText
FROM OrderDetails;

[Experimente você mesmo »](https://www.w3schools.com/sql/trymysql.asp?filename=trysql_case)

O SQL seguinte ordenará aos clientes pela City. No entanto, se a cidade é NULL, então peça por País:

### Exemplo

SELECT CustomerName, City, Country
FROM Customers
ORDER BY
(CASE
  WHEN City IS NULL THEN Country
  ELSE City
END);

**EXEMPLO 2**

**SELECT **

**CASE** 

​         **WHEN** condition_1 **THEN** result_1

​         **WHEN** condition_2 **THEN** result_2  **FROM** tb_sale

​         [**WHEN** ...]

​         [**ELSE** else_result]

**END**

**FROM** tb_sale



**EXEMPLO 3**

**SELECT **

**CASE** 

​         **WHEN** Preco < 500 **THEN** 'Barato'

​        **ELSE** 'Caro'

**END AS** classificacao

**FROM** tb_sale



**EXEMPLO 4**

**SELECT ** *,

**CASE** 

​         **WHEN** **EXTRACT**(**MONTH FROM** date) >=10 **THEN** **CONCAT** (**EXTRACT**(**MONTH FROM** date), '/', **EXTRACT**(**YEAR FROM** date))

​        **ELSE** **CONCAT** ( '0', **EXTRACT**(**MONTH FROM** date), '/', **EXTRACT**(**YEAR FROM** date))

**END AS** mes_ano

**FROM** tb_sale



# --------------MySQL REPLACE() Function------------



### Exemplo

Substitua "SQL" por "HTML":

SELECT REPLACE("SQL Tutorial", "SQL", "HTML");

------

## Definição e Uso

A função REPLACE() substitui todas as ocorrências de um substring dentro de uma string, por um novo substring.

**Nota:** Esta função executa uma substituição sensível a maiústos.

## Sintaxe

REPLACE(*string*, *from_string*, *new_string*)

## Valores dos parâmetros

| Parameter     | Description                             |
| :------------ | :-------------------------------------- |
| *string*      | Required. The original string           |
| *from_string* | Required. The substring to be replaced  |
| *new_string*  | Required. The new replacement substring |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Substitua "X" por "M":

SELECT REPLACE("XYZ FGH XYZ", "X", "M");

### Exemplo

Substitua "X" por "m":

SELECT REPLACE("XYZ FGH XYZ", "X", "m");

### Exemplo

Substitua "x" por "m":

SELECT REPLACE("XYZ FGH XYZ", "x", "m");



# -------------Função MySQL CHAR_LENGTH()-------



### Exemplo

Retorne o comprimento da sequência:

SELECT CHAR_LENGTH("SQL Tutorial") AS LengthOfString;

------

## Definição e Uso

A função CHAR_LENGTH() retorna o comprimento de uma string (em caracteres).

**Nota:** Esta função é igual à função [CHARACTER_LENGTH().](https://www.w3schools.com/sql/func_mysql_character_length.asp)

## Sintaxe

CHAR_LENGTH(*string*)

## Valores dos parâmetros

| Parameter | Description                                  |
| :-------- | :------------------------------------------- |
| *string*  | Required. The string to count the length for |

## Detalhes técnicos

| Funciona em: | De MySQL 4.0 |
| :----------- | ------------ |
|              |              |

------

## Mais exemplos

### Exemplo

Retorne o comprimento do texto na coluna "CustomerName":

**SELECT CHAR_LENGTH**(CustomerName) **AS** LengthOfName
**FROM** Customers;

**SELECT** id, name, **CHAR_LENGTH**(name) **FROM** tb_seller



# ------------------------SQL MD5()---------------------------

Em SQL, a função MD5() é usada para criptografar uma sequência de caracteres em um inteiro hexadecimal de 32 caracteres. Esta sequência de retorno pode ser particularmente útil para ser usada como uma chave hash.

**Nota:** a função MD5() usa o algoritmo RSA (ver "RSA Data Security, Inc. MD5 Message-Digest Algorithm").

## Sintaxe

A função é usada em uma consulta SQL da seguinte forma:

```
SELECT MD5('test');
```

Tal consulta retornará a seguinte sequência:

```
098f6bcd4621d373cade4e832627b4f6
```

Este exemplo concreto mostra o valor do uso do MD5() para criar uma chave hash.

## Exemplo

Para entender como essa função funciona, veremos alguns exemplos possíveis de cenários onde a função será útil. Esses **exemplos são puramente fictícios** e não representam uma maneira de proceder para garantir uma aplicação. Por exemplo, existem lojas de dados que podem potencialmente encontrar uma string da cifra MD5(). Portanto, **essa função não é uma função de criptografia segura para armazenar senhas "de forma limpa".**

### Crie uma chave para um usuário

Vamos imaginar um aplicativo que tenha contas de usuário. Ao se registrar, o usuário deve validar seu endereço de e-mail clicando em um link que se parece com este:

```
http://www.example.com/valider-email.php?utilisateur=345
```

Usar esse método é perigoso porque qualquer pessoa pode apenas alterar o ID manualmente para validar contas de usuário. Ou seja, com um nível tão baixo de segurança, você pode facilmente tentar todas as combinações possíveis substituindo o "345" da URL para validar contas que não são suas.

Para melhorar um pouco a segurança, é possível gerar uma chave hash para cada usuário e validar o endereço de e-mail somente se a URL VISITADA contiver os seguintes 2 parâmetros: o identificador e a chave **hash correta** (ou seja, a chave hash que corresponde ao identificador).

```
http://www.example.com/valider-email.php?utilisateur=345&hashage=098f6bcd4621d373cade4e832627b4f6
```

Dessa forma, pessoas mal-intencionadas não serão capazes de executar tarefas críticas em contas que não se encaixam nelas.

Gerar uma chave hash única é relativamente simples. É possível, por exemplo, usar como tecla de entrada uma combinação do identificador + a data + a hora + qualquer palavra. Assim, será muito complicado para um hacker tentar encontrar a combinação certa para validar um e-mail. Aqui está o exemplo concreto:

```
UPDATE utilisateur
SET hashage = MD5('345_2013-10-04 22:16:45_moutarde')
WHERE id = 345
```

Esta consulta adicionará uma chave hash ao usuário com ID 345.

### Atualize uma senha para MD5

Apenas para os propósitos deste tutorial, consideraremos que uma senha de um aplicativo é armazenada usando a função MD5(). Nessas circunstâncias, é possível atualizar uma senha usando uma consulta SQL semelhante à consulta abaixo:

```
UPDATE utilisateur
SET password = MD5('nouveau_mot_de_passe')
WHERE id = 39;
```

**Lembrete:** tal método não se protege bem de ataques de computador.

### Verifique o nome de usuário e a senha de um usuário

Este novo exemplo novamente usa o exemplo onde a senha é salva através da função MD5(). Se o usuário desejar fazer login usando seu login e senha, o aplicativo poderá verificar a combinação correta usando a consulta abaixo:

```
SELECT id
FROM utilisateur
WHERE login = 'alphonse' AND password = MD5('secret');
```

O resultado desta consulta é simples:

- Se essa solicitação retornar um identificador, será o nome de usuário do usuário que tiver a combinação correta de login e senha
- Se a consulta não retornar nenhum resultado, significa que o login ou senha não corresponde a nenhuma combinação existente na tabela de usuário

### Melhore um pouco a segurança com um prefixo e/ou sufixo

Como explicado, os exemplos apresentados acima são puramente fictícios e não são recomendados para uma aplicação segura. Existem lojas de dados que permitem que você procure uma chave em potencial a partir de seu hash MD5. Para armazenar uma senha é preferível usar a função [SHA1().](https://sql.sh/fonctions/sha1)

No entanto, ainda é possível usar a função MD() combinando um prefixo e sufixo com a chave de entrada usada pela função. Isso torna a criptografia um pouco mais complexa para que seja mais difícil adivinhar a chave inicial. O prefixo e o sufixo não devem ser divulgados para manter boa segurança.

Em nosso exemplo, imaginaremos que o prefixo será a corda do personagem "GIRAFA" enquanto o sufixo será "TENNIS".

**Solicitação para atualizar senha:**

```
UPDATE utilisateur
SET password = MD5('GIRAFEnouveau_mot_de_passeTENNIS')
WHERE id = 39;
```

**Solicitação para verificar login + senha:**

```
SELECT id
FROM utilisateur
WHERE login = 'alphonse' AND password = MD5('GIRAFEsecretTENNIS');
```

Este método é preferível e melhora um pouco a segurança de um aplicativo.



**exemplo 1**

SELECT *, MD5(name) FROM tb_seller

**EXEMPLO 2**

SELECT MD5('minhasenha@@')
