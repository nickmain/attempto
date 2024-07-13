Prepositions (e.g. "in", "for", "during") are represented by only one kind of entry:

``` prolog
prep(WordForm, LogicalSymbol).
```

Prepositions have only one word form. Some concrete examples:

``` prolog
prep(in, in).

prep(for, for).

prep(during, during).
```

It is recommended to use the word form also as the logical symbol.