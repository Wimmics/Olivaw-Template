# domains folder

This folder is meant to contain the `domains` that the ontology project will develop for. Each of these domains should contain some `motivating scenarios`.

During an iteration, a `motivating scenario` is written. It explains a situation and adresses questions in natural language named `competency questions` that cannot be described by the ontology, while it should. The current iteration should then determine which minimal set of terms named `glossary of terms` are needed to be added in order to implement the `competency questions` using SparQL.

These terms are then developped in a ontology fragment named `modelet` and this modelet is populated in a `dataset`. Finally the competency questions are then implemented in SparQL, showing that the situation can now be described with these new terms.

The `motivating scenarios` are sorted here by `domain` types.

Check here the domain named [domain-template](./domain-template/), its related [template motivating scenario](./domain-template/scenario-template/). This scenario has a [scenario definition](./domain-template/scenario-template/README.md), a [modelet](./domain-template/scenario-template/onto.ttl), a [dataset](./domain-template/scenario-template/dataset.ttl) and a [competency question implementation](./domain-template/scenario-template/q1.rq).