The following steps were used to convert `grammar.y` and `lex.l` to `*.c` and `*.h` files:
```
yacc -d grammar.y 
mv y.tab.c grammar.c
mv y.tab.h grammar.h

lex lex.l 
mv lex.yy.c lex.c
```
