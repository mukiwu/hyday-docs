---
locale: en
category: concepts
slug: tags
source: src/content/docs/en/concepts/tags.tsx
---
> *Tags are the lightest-weight way to organize and classify notes. Hyday supports both**inline tags**and**frontmatter tags**.*

## Two Ways to Tag

- **Inline tags**: Write`#tag-name`directly in the body. Hyday recognizes it as an inline tag automatically.
- **Frontmatter tags**: Define them in the metadata block at the top of the note:

```
``
```

Either way, all tags get indexed into the same tag system.

## Which Style to Use?

ScenarioRecommendedThe whole note is about one topicFrontmatterOnly one paragraph relates to the topicInline`#tag`You want the tag inline so you can jump while readingInline tagYou want search to find it, without cluttering the visual reading flowFrontmatter

## Tag Exploration

Click any tag to open the**tag explore drawer**, where you can see:

- **Usage history**: Every note that uses the tag, plus a timeline of how heat is distributed.
- **Related tags (co-occurrence)**: Other tags that show up alongside this one most often.

![Tag explore drawer](https://hyday.tw/docs/screenshots/concepts-tags-1.png)

## Further Reading

- [Organize With Tags](https://hyday.tw/docs/guides/organize-with-tags): A practical primer.
- [Explore Topic Lineage](https://hyday.tw/docs/guides/explore-tag-lineage): An advanced guide to applying tags.
