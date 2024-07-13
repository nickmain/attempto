Intransitive adjectives (e.g. "important", "large", "expensive") are represented by three different kinds of entries, defining the positive form, the comparative form, and the superlative form respectively:

``` prolog
adj_itr(PositiveForm, LogicalSymbol).
adj_itr_comp(ComparativeForm, LogicalSymbol).
adj_itr_sup(SuperlativeForm, LogicalSymbol).
```

Again, for regular comparative and superlative forms (starting with "more" or "most"), only the positive form needs to be defined. Some concrete examples:

``` prolog
adj_itr(important, important).

adj_itr(large, large).
adj_itr_comp(larger, large).
adj_itr_sup(largest, large).

adj_itr(expensive, expensive).
```

It is recommended to use the positive form also as the logical symbol. Furthermore, it is recommended to define a positive form for each comparative or superlative form.