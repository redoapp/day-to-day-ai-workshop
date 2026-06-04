---
title: "Dashboard"
date_modified: 2026-06-04
type: index
---

# 📊 Knowledge Base Dashboard

> Live views of the wiki. These tables render once the **Dataview** plugin is installed
> (Settings → Community plugins → Browse → "Dataview"). Until then you'll see the code blocks.
> Tip: set this note as your **Homepage** (Homepage plugin) so it opens on launch.

## Recently updated
```dataview
TABLE WITHOUT ID file.link AS "Page", type, date_modified AS "Updated"
FROM "wiki"
WHERE type != "index"
SORT date_modified DESC
LIMIT 10
```

## Concepts
```dataview
TABLE WITHOUT ID file.link AS "Concept", summary, source_count AS "Sources", confidence
FROM "wiki/concepts"
WHERE type = "concept"
SORT source_count DESC
```

## Entities
```dataview
TABLE WITHOUT ID file.link AS "Entity", summary
FROM "wiki/entities"
WHERE type = "entity"
SORT file.name ASC
```

## Sources
```dataview
TABLE WITHOUT ID file.link AS "Source", authors AS "Author(s)", tags
FROM "wiki/sources"
WHERE type = "source"
SORT date_created DESC
```

## Filed answers & syntheses
```dataview
LIST
FROM "wiki/outputs" OR "wiki/syntheses"
WHERE type = "output" OR type = "synthesis"
SORT date_modified DESC
```

## Needs attention
```dataview
TABLE WITHOUT ID file.link AS "Page", status
FROM "wiki"
WHERE status = "draft" OR status = "review"
SORT status ASC
```

## Raw sources not yet summarised
```dataview
LIST
FROM "raw"
WHERE type = "article" AND status = "raw"
```
*(After `/wiki-ingest`, each raw source should have a matching summary in `wiki/sources/`.)*
