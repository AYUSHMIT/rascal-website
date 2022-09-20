---
title: Details
---

.Synopsis

Explicitly order the subconcepts of the current concept.

.Syntax

```
---
details:
  - Detail~1~
  -  Detail~2~
  -  ...

---
```

.Types

.Function

.Description

To fully describe a concept, subconcepts (or details) are needed.
When the `details` meta-data header is empty, subconcepts will be listed
alphabetically in the details section of the generated HTML file.

This alphabetical order can be influenced by explicitly stating concepts in the details meta-data header..
The effect is that the concepts listed there will be shown first, followed by the unmentioned subconcepts
in alphabetical order.

.Examples

In [Concept](/Tutor/Concept) we want to order the details in the order as they appear in the concept description.
Its `Details` meta-data is therefore:

```
---
title: Concept
details:
  - Name
  - Details
  - Syntax
  - Types
  - Function
  - Synopsis
  - Description
  - Examples
  - Benefits
  - Pitfalls
  - Questions

---
```

.Benefits

.Pitfalls


