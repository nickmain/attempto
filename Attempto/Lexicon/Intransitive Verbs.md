Intransitive verbs (e.g. "waits", "goes-away", "walks") are represented by two different kinds of entries, defining the third singular form and the infinitive form respectively:

``` prolog
iv_finsg(ThirdSgForm, LogicalSymbol).
iv_infpl(InfForm, LogicalSymbol).
```

The infinitive form should usually be the singular form without the 's' at the end: "wait", "walk". Phrasal particles should be hyphenated to the verb, e.g. "goes-away". Some concrete examples:

``` prolog
iv_finsg(waits, wait).
iv_infpl(wait, wait).

iv_finsg('goes-away', 'go-away').
iv_infpl('go-away', 'go-away').

iv_finsg(walks, walk).
iv_infpl(walk, walk).
```

It is recommended to use the infinitive form also as the logical symbol. Furthermore, it is recommended to define a third singular form for each infinitive form, and vice versa.