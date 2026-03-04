# Database W3Schools

Non sono associato a W3Schools, ma ci tengo a ringraziarli pubblicamente. Questo è il loro sito web:
https://www.w3schools.com

Offrono eccellenti tutorial sullo sviluppo web. 

In ogni caso, questa repository contiene il database che utilizzano per il loro tutorial SQL:
https://www.w3schools.com/sql/default.asp

Puoi visualizzare le tabelle del database e i relativi dati sul lato destro eseguendo questo esempio:
https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all

Tuttavia, non è presente un link diretto per scaricare il database, quindi ho deciso di generare il codice SQL corrispondente. Spero che lo troverai utile: è ottimo avere questo database in locale per eseguire query, test, fare pratica o per scopi didattici. Buon divertimento!

Lo script SQL si trova in questo file: [w3schools.sql](w3schools.sql).

---

## Struttura del Database

Quando il file SQL viene eseguito, crea un database chiamato **w3schools** con le seguenti tabelle:

* `categories`
* `customers`
* `employees`
* `orders`
* `order_details`
* `products`
* `shippers`
* `suppliers`

Il file si occupa inoltre di inserire tutti i record corrispondenti in ogni tabella.



### Personalizzazione
Puoi cambiare il nome del database in qualsiasi momento modificando queste due righe di codice all'inizio del file:

```sql
CREATE DATABASE IF NOT EXISTS `w3schools`;
USE `w3schools`;
```
