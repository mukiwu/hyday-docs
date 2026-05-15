---
locale: en
category: concepts
slug: entities
source: src/content/docs/en/concepts/entities.tsx
---
> *Entities mark specific**people, events, places, and things**. The difference from tags: tags categorize abstract topics, while entities track concrete subjects.*

## How Do You Create an Entity Tag?

Type`@`in the editor to open the entity menu. Pick an existing entity or create a new one on the spot:

```
``
```

## Entities vs. Tags

TraitTag (#)Entity (@)**Core use**Categorize abstract topicsTrack concrete subjects**Examples**`#work`,`#health``@Alice`,`@Deep Work`**Explore value**See topic-level trendsRoll up everything about that subject**Time horizon**Usually long-runningOften has a clear lifecycle or stage of involvement

## Good Candidates for Entities

- **People**: for example`@Alice`,`@Boss`
- **Places**: for example`@Kyoto`,`@Taipei 101`
- **Books and media**: for example`@Deep Work`,`@The Crown`
- **Products and tools**: for example`@Hyday`,`@Notion`.

## Entity Exploration

Click any entity tag to open the**entity drawer**and dig in:

- Every note and journal snippet that mentions the entity.
- **Related entities**: which other entities most often co-occur with this one (for example,`@Alice`showing up frequently with`@Bob`suggests they're a close working pair).
- **Timeline**: the first appearance and the most recent mention of this entity.

> **ℹ️ Info**
> For people, use real names or familiar nicknames. For places, use specific names. For books or videos, use the full title — avoid vague names like`@That Book`.Note that Hyday doesn't do fuzzy matching automatically, so`@Alice`and`@alice`count as two distinct entities.

## Working Together With Tags

```
`-(14:30) Started [[Q3 Roadmap]] meeting with @Alice #work`
```

This single line contains a time anchor (LifeLog), an entity (Alice), a backlink (Q3 Roadmap), and a tag (work). Hyday picks up all four signals and cross-indexes them to build out the full knowledge lineage.
