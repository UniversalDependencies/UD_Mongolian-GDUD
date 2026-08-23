# Summary

UD_Mongolian-GDUD is a treebank of Khalkha Mongolian, the standard variety of Mongolian, based on grammatical example sentences derived from a reference grammar.

# Introduction

The Mongolian GDUD (Grammar-Derived Universal Dependencies) treebank contains 88 sentences of Khalkha Mongolian (ISO 639-3: khk), the standard variety of Mongolian spoken primarily in Mongolia. The data consist of grammatical example sentences drawn from a reference grammar of Mongolian, presented in Latin transliteration and accompanied by English translations.

All sentences are manually annotated with lemmas, universal part-of-speech tags (UPOS), morphological features, and dependency relations, following the Universal Dependencies (UD) guidelines. The annotation prioritizes UD core morphological features and dependency relations. A small number of language-specific dependency subtypes are used to capture distinctions that are syntactically overt in Khalkha Mongolian. In addition, some Mongolian-specific morphological information that does not correspond to any feature in the universal inventory (namely certain aspectual distinctions such as the successive aspect, the quotative particle type, and modality marking) is encoded in the MISC column, in accordance with UD conventions for annotations that are not part of the universal feature inventory.

## Data split

Because the treebank is small (well below the 20K-word threshold), all sentences are provided as test data. Users who wish to train models on it should perform cross-validation.

## Morphological annotation

All UD core features used in the treebank take standard universal values. The features attested in the treebank include: Aspect, Case, Degree, Evident, Mood, NumType, Number, PartType, Person, Polarity, Poss, PronType, Reflex, Tense, VerbForm, and Voice.

The following Mongolian-specific morphological information is encoded in the MISC column rather than FEATS, as it does not correspond to any value in the universal feature inventory:

* `Aspect=Succ` — the successive aspect (marking sequential events)
* `PartType=Quot` — the quotative particle type
* `Modality=Yes` — modal marking on certain finite verb forms

Auxiliary verbs `baj` (progressive/existential) and `bol` (change of state) are analyzed as auxiliaries and tagged AUX.

## Dependency annotation

UD core relations are used throughout the treebank. The following language-specific dependency subtypes are used:

* `acl:relcl` — relative clause modifier
* `nmod:poss` — possessive nominal modifier
* `nsubj:pass` — passive nominal subject
* `obl:agent` — agent of a passive construction

The relation `nsubj:outer` is used in one case where a clause acts as the predicate of another clause.

# Acknowledgments

The Mongolian GDUD treebank was created by Wenchao Li and Haitao Liu, based on grammatical example sentences from a reference grammar of Khalkha Mongolian. The annotation of lemmas, part-of-speech tags, morphological features, and dependency relations was carried out manually following the Universal Dependencies guidelines.

We are especially grateful to Daniel Zeman for his guidance in setting up the treebank repository and for his help with the Universal Dependencies workflow. We also thank the Universal Dependencies community for their support during the preparation and release of this treebank.

# Changelog

* 2026-08-23 v2.19
  * Initial release in Universal Dependencies.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.19
License: CC BY-SA 4.0
Includes text: yes
Parallel: no
Genre: grammar-examples
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Li, Wenchao; Liu, Haitao
Contributing: here
Contact: widelia@zju.edu.cn
===============================================================================
</pre>
