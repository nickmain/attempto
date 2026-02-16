---
title: Measurement Nouns
---
Measurement nouns (e.g. "kg", "m", "°C") are represented by only one kind of entry:

``` prolog
mn_sg(SingularForm, LogicalSymbol).
mn_pl(PluralForm, LogicalSymbol).
```

It is recommended to define measurement nouns in the form of measurement symbols (i.e. "m" instead of "meter"). In this case, the singular and plural forms should usually be the same. Some concrete examples:

``` prolog
mn_sg(kg, kg).
mn_pl(kg, kg).

mn_sg(m, m).
mn_pl(m, m).

mn_sg('°C', '°C').
mn_pl('°C', '°C').
```

It is recommended to use the singular form also as the logical symbol. Furthermore, it is recommended to define a singular form for each plural form, and vice versa.