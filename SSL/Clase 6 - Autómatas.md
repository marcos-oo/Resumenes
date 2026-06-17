- Las gramáticas son los generadores de las palabras los lenguajes. Genera.
- Las expresiones regulares representa el lenguaje definido por una gramática. Representa.
- Un autómata verifica si una palabra pertenece a un lenguaje. Reconoce.
Los LF son LR si pueden ser reconocidos por un Autómata Finito.
## Que es un autómata?
Un autómata es un mecanismo abstracto que permite reconocer lenguajes formales.
- Tiene reglas simples
- No tiene memoria
- Salida binaria (pertenece o no pertenece).
## Autómata según jerarquía de Chomsky

| Gramática Formal: | Lenguaje Formal generado: | Autómata que lo reconoce: |
| ----------------- | ------------------------- | ------------------------- |
| GR                | LR                        | Autómata Finito           |
| GIC               | LIC                       | Autómata Finito con Pila  |
| GSC               | LSC                       | Autómata de Turing        |
| GI                | LI                        | Autómata de Turing        |
De la misma forma que en la jerarquía, un Autómata Finito con Pila contiene al Autómata Finito y un Autómata de Turing contiene al Autómata Finito con Pila.

## Autómatas finitos
- El AF recorre los caracteres de la cadena.
- Cada carácter procesado causa un cambio de estado.
- Si al terminar se encuentra en un Estado Final es que ha reconocido la cadena.
- Un AF puede tener varios estados finales.
- Existe también otro estado especial, el Estado Inicial, y es único.