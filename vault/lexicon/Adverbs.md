Adverbs (e.g. "fast", "quickly", "intensively") are represented by three different kinds of entries, defining the positive form, the comparative form, and the superlative form respectively:

``` prolog
adv(PositiveForm, LogicalSymbol).
adv_comp(ComparativeForm, LogicalSymbol).
adv_sup(SuperlativeForm, LogicalSymbol).
```

For regular comparative and superlative forms (starting with "more" or "most"), only the positive form needs to be defined. In order to use "more quickly", for example, it is sufficient to define the positive form "quickly". Some concrete examples:

``` prolog
adv(fast, fast).
adv_comp(faster, fast).
adv_sup(fastest, fast).

adv(quickly, quickly).

adv(intensively, intensively).
```

It is recommended to use the positive form also as the logical symbol. Furthermore, it is recommended to define a positive form for each comparative or superlative form.