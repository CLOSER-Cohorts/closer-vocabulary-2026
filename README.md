# CLOSER Vocabulary

The documents are available as web pages at: https://closer-cohorts.github.io/closer-vocabulary-2026/

## Relationship between Vocabulary and Variables

``` mermaid

flowchart LR

 L1[Level 1 Concept] --> L2[Level 2 Concept]
 IV[Concorded instance Variable] --> CV
 CV[Conceptual Variable] -->L1
 CV[Conceptual Variable] -->L2
 IV --> KWP[Unique Key Words]
 KWP --> KWPG[Key Word Groups]
 KWPG --> ELSST

 ELSST -.-> L2
 Question --> IV
 KWP -.-> CV

```

The above diagram illustrates the uses to which the vocabulary will be used and actioned upon.

Concepts (we will use the terms Topic in public facing materisal) are designed as a Discovery mechanisms, broadly assigning questions and variables to a group which is comprehensible and appropriate for the majority of users.

There are two levels of concepts, and items are assigned to the best available. Some exceptions will be made in the case of items that exist in for instance standardised scales, where although the individual items could be assigned to Level 2, all items are assigned to a Level 1 concept.

Even with @120 concepts, the large number of items are difficult to navigate and compare, as they arise from a set of discretely similar but different questions which necessitate concordance, grouping together variables that are equivalent as conceptual variables.

The mechanism to achieve this within a study which has good data management would be to utilise the naming conventions to align the variables into discrete groups / conceptual variables. Being separate studies, the naming convention breaks down when comparing across studies.

Unique words within a questions can be utilised as a way to automate this comparison against an existing Conceptual Variable.

ELSST although voluminous, does not have the level of granularity to support each Conceptual Variable, but subsets of Key words could be mapped to ELSST.

## Migrating to the new vocabulary

In many cases the new vocabulary is a one-to-one match with the previous iteration, or collapsing many into a new one. This is a simple mapping exercise.
Where new vocabulary items are split into a new more granular vocabulary item, we can utilise the key word groups to allocate them to the new vocabulary item.

## Further changes to the vocabulary

Should new terms emerge, through user feedback, new data items etc necessitating a new vocabulary topic, the key word / concordances can be utilised to update the items to the new terms.





