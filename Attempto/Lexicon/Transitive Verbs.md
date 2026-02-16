Transitive verbs (e.g. "knows", "likes", "relates-to") are represented by three different kinds of entries, defining the third singular form, the infinitive form, and the past participle form respectively:

``` prolog
tv_finsg(ThirdSgForm, LogicalSymbol).
tv_infpl(InfForm, LogicalSymbol).
tv_pp(PastPartForm, LogicalSymbol).
```

Phrasal particles and direct prepositions should be hyphenated to the verb, e.g. "relates-to", "lives-in", and "comes-up-with". The past participle is the form that is used for passive voice: "known", "liked", "seen". If it is not defined then passive voice is not possible for the respective verb. Some concrete examples:

``` prolog
tv_finsg(knows, know).
tv_infpl(know, know).
tv_pp(known, know).

tv_finsg(likes, like).
tv_infpl(like, like).
tv_pp(liked, like).

tv_finsg('relates-to', 'relate-to').
tv_infpl('relate-to', 'relate-to').
tv_pp('related-to', 'relate-to').
```

It is recommended to use the infinitive form also as the logical symbol. It is also recommended to define a third singular form for each infinitive form, and vice versa. Furthermore, it is recommended to define third singular and infinitive forms for each past participle form.