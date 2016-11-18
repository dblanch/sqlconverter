# sqlconverter

converts oracle sql and plsql to postgres sql and plpgsql

# Challenges

I've been working with ora2pg from Giles Darold. Though it works pretty well with most objects, it doesn't works very well with procedures and functions.

The problem is that the aproach taken, using regular expressions, is not enough when facing the rough parts. You need a real parser, and a real translator. 

So i'm going to develop a translator for:

* Oracle outer joins, this is with table1.id =+ table2.table1_id have to be translated to LEFT JOIN syntax.

* Oracle functions and packages to postgresql counterpart.

* Functions with nested expressions, included functions.

* Application embedded SQL 
