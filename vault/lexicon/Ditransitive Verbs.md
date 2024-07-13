Ditransitive verbs (e.g. "shows", "forgives", "succeeds") are represented by three different kinds of entries, defining the third singular form, the infinitive form, and the past participle form respectively:

``` prolog
dv_finsg(ThirdSgForm, LogicalSymbol, Preposition).
dv_infpl(InfForm, LogicalSymbol, Preposition).
dv_pp(PastPartForm, LogicalSymbol, Preposition).
```

ACE allows two forms of ditransitive verbs:

- Verbs which take two complements neither of which is introduced by a preposition (e.g. "John shows Mary an apple.", "John forgives Mary her shortcomings."). The first complement is considered to be an indirect object, the second a direct object. In this case the preposition argument must be set to the empty atom `''`.
- Verbs which take two complements, second of which is prepositional, i.e. introduced by a preposition (e.g. "John shows an apple to Mary", "John succeeds Mary as the president"). The first complement is considered to be a direct object, the second an indirect object. In this case the preposition argument must contain the preposition, e.g. "to" in the case of "show" and "as" in the case of "succeed".

In case a verb allows both forms (such as the verb "show"), each lexicon entry must be declared twice. Some concrete examples:

``` prolog
dv_finsg(shows, show, '').
dv_infpl(show, show, '').
dv_pp(shown, show, '').
dv_finsg(shows, show, to).
dv_infpl(show, show, to).
dv_pp(shown, show, to).

dv_finsg(forgives, forgive, '').
dv_infpl(forgive, forgive, '').
dv_pp(forgiven, forgive, '').

dv_finsg(succeeds, succeed, as).
dv_infpl(succeed, succeed, as).
dv_pp(succeeded, succeed, as).`
```

It is recommended to use the infinitive form also as the logical symbol. It is also recommended to define a third singular form for each infinitive form, and vice versa. Furthermore, it is recommended to define third singular and infinitive forms for each past participle form.