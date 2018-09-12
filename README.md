# Lex and Syntactic Analyzer

Lexical and Syntactic analyzer for Compie Design Course

## Grammar (Backus Naur Form)

```
<fuente> ::= [<bloque_funcion>] <principal>

<bloque_funcion> ::= {<funcion>}

<principal> ::= principal '(' ')' [<declaraciones>]
                [<operaciones>] '}'

<funcion> ::= <tipo_dato> <id> '(' [<argumentos>] ')'
                '{' [<declaraciones>] [<expresiones>]
                <regresa> '}'

// <operaciones> ::= <expresiones>

<expresiones> ::= <id> '=' <expresion> ';'
              ::= <declaracion_si> | <declaracion_mientras>
<expresion> ::= <aritmetica> | <logica> | <relacionales> | <id> | !<id>

<logica> ::= <id> '&' <id> ';'
         ::= <id> '|' <id> ';'

<asignacion> ::= <id>

<relacionales> ::= <relacional> <operador> <relacional>

<operador> ::= '<'| '>' | '=='

<relacional> ::= <num><relacional> | <id>

<aritmetica> ::= <termino> + <aritmetica> | <termino> - <aritmetica> | <termino>

<termino> ::= <factor> * <termino> | <factor> / <termino> | <factor>

<factor> ::= '(' <aritmetica> ')'

<declaracion_si> ::= si '(' <id> ')' '{' [<expresiones>]'}'

<declaracion_mientras> ::= mientras '(' id ')' '{' [<expresiones>] '}'

<num> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9

<abecedario> ::= a | b | c | d | e | f | g | h | i | j | k | l | m | n | o | p | q | r | s | t | u | v | w | x | y | z

<id> ::= { <abecedario>}
         [ <num> ]

<argumentos> ::= <tipo_dato> <id> [',']

<regresa> ::= <id> ';'

<declaraciones> ::= <tipo_dato> <id> ';'
```
