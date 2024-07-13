---
title: Proper Names
---
Proper names come in two versions: one for those that require a preceeding definite article (e.g. "the Nile", "the United-Nations") and one for those that stand by itself (e.g. "John", "Nokia"). Proper names can also be declared in both of those categories (e.g. "(the) Mona-Lisa").

``` prolog
pn_sg(WordForm, LogicalSymbol, Gender).
pn_pl(WordForm, LogicalSymbol, Gender).
pndef_sg(WordForm, LogicalSymbol, Gender).
pndef_pl(WordForm, LogicalSymbol, Gender).
```

Gender has the same meaning as for countable nouns. Some concrete examples:

``` prolog
pn_sg('John', 'John', masc).

pn_sg('Nokia', 'Nokia', neutr).

pndef_sg('Nile', 'Nile', neutr).

pndef_pl('United-Nations', 'United-Nations', neutr).

pn_sg('Mona-Lisa', 'Mona-Lisa', neutr).
pndef_sg('Mona-Lisa', 'Mona-Lisa', neutr).
```

It is not allowed to declare the same proper name as singular and plural at the same time. It is recommended to use the word form also as the logical symbol.