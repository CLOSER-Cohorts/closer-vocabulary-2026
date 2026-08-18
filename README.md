# CLOSER Vocabulary

The documents are available as web pages at: https://closer-cohorts.github.io/closer-vocabulary-2026/

## Current use of Vocabulary

We use the term in the diagrams below of Concept L1 and L2, for the user these are presented as Topics.

``` mermaid

flowchart LR

 L1[Discovery Level 1 Concept] --> L2[Discovery Level 2 Concept]
 IV[instance Variable] --> L1
 IV[instance Variable] --> L2
 Question --> L1
 Question --> L2

```

## Relationship between Vocabulary, Concepts, Variables etc

In addition to these relationship, further relationships will be added

``` mermaid

flowchart LR

 IV[instance Variable] --> L1
 IV[instance Variable] --> L2
 Question --> L1
 Question --> L2
 L1[Discovery Level 1 Concept] --> L2[Discovery Level 2 Concept]
 IV[instance Variable] --> CV
 CV[Conceptual Variable] -->L1
 CV[Conceptual Variable] -->L2
 IV --> KWP[Unique Key Words]
 KWP --> KWPG[Key Word Groups?]
 KWPG --> ELSST
 ELSST -.-> L1
 ELSST -.-> L2
 Question --> KWP
 KWP -.-> CV

```

The above diagram illustrates the uses to which the vocabulary will be used and actioned upon.

Concepts (we will use the terms Topic in public facing materisal) are designed as a Discovery mechanisms, broadly assigning questions and variables to a group which is comprehensible and appropriate for the majority of users.

There are two levels of concepts, and items are assigned to the best available. Some exceptions will be made in the case of items that exist in for instance standardised scales, where although the individual items could be assigned to Level 2, all items are assigned to a Level 1 concept.

Even with @120 concepts, the large number of items are difficult to navigate and compare, as they arise from a set of discretely similar but different questions which necessitate concordance, grouping together variables that are equivalent as conceptual variables.

The mechanism to achieve this within a study which has good data management would be to utilise the naming conventions to align the variables into discrete groups / conceptual variables. Being separate studies, the naming convention breaks down when comparing across studies.

Unique words within a questions can be utilised as a way to automate this comparison against an existing Conceptual Variable.

### Mapping to ELSST

ELSST although voluminous, does not have the level of granularity to support each Conceptual Variable, but subsets of Key words could be mapped to ELSST, where ELSSST terms exist.

## Migrating to the new vocabulary

In many cases the new vocabulary is a one-to-one match with the previous iteration, or collapsing many into a new one. This is a simple mapping exercise.
Where new vocabulary items are split into a new more granular vocabulary item, we can utilise the key word groups to allocate them to the new vocabulary item.

## Further changes to the vocabulary

Should new terms emerge, through user feedback, new data items etc necessitating a new vocabulary topic, the key word / concordances can be utilised to update the items to the new terms.

## Known issues

Where variables do not have questions associated with them, such as Derived Variables, not available mapping, a remedial solution will be required!

## DDI Implementation

From a practical point of View, we will need to maintain both the Discovery Concepts / Topic vocabulary and the underlying conceptual metadata that supports concordance and mapping to ELSST.

### Mapping between Conceptual Variable and Key Words

There are two main options:

1. Maintain a separate Concept system that references the Vocabulary using BroaderReference

``` mermaid

flowchart TD
 CV[Conceptual Variable]  -- "Broader" --> Concepts[Discovery Concepts L1 & L2] 
 CV -- "Narrower" --> KWP[Unique Key Words Concept]
 KWP -- "Broader" --> KWPG[Key Word Groups Concept]
 KWPG --> ELSST[ELSST Term]

```

2. Maintain a single Concept system using NarrowerReference in Concept to Conceptual Variable

``` mermaid

flowchart TD

 Concepts[Discovery Concepts L1 & L2]  -- "Narrower" --> CV[Conceptual Variable]
 CV -- "Narrower" --> KWP[Unique Key Words Concept]
 KWP -- "Broader" --> KWPG[Key Word Groups Concept]
 KWPG --> ELSST[ELSST Term]

```
The flatter, may be problematic a it will likely overload users if we cannot exclude it from rendering on the portal, the second, may take more maintenance

