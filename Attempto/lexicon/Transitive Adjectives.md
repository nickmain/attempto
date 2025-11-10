Transitive adjectives (e.g. "valid-for", "fond-of", "pessimistic-about") are represented by three different kinds of entries, defining the positive form, the comparative form, and the superlative form respectively:

``` prolog
adj_tr(PositiveForm, LogicalSymbol, Preposition).
adj_tr_comp(ComparativeForm, LogicalSymbol, Preposition).
adj_tr_sup(SuperlativeForm, LogicalSymbol, Preposition).
```

Transitive adjectives should consist of an adjective and a preposition that is hyphenated to the adjective. Again, for regular comparative and superlative forms (starting with "more" or "most"), only the positive form needs to be defined. Preposition is the preposition part of the word, e.g. "for" in the case of "valid-for", "of" in the case of "fond-of", and "about" in the case of "pessimistic-about". It is only used for the comparative form in sentences where the preposition can occur on its own, like in "Mary is more fond-of Bill than **of** John". Some concrete examples:

``` prolog
adj_tr('valid-for', 'valid-for', for).

adj_tr('fond-of', 'fond-of', of).
adj_tr_comp('fonder-of', 'fond-of', of).
adj_tr_sup('fondest-of', 'fond-of', of).

adj_tr('pessimistic-about', 'pessimistic-about', about).
```

It is recommended to use the positive form also as the logical symbol. Furthermore, it is recommended to define a positive form for each comparative or superlative form.