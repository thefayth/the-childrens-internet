# Workflow Diagrams

## Workflow Overview

![Workflow overview](../assets/diagrams/workflow-overview.svg)

Source Mermaid:

```mermaid
graph LR
  Families[Families and children] --> Microsite[Public microsite]
  Schools[Schools and libraries] --> Microsite
  Microsite --> Demo[Interactive demo]
  Microsite --> Pitch[Pitch mode]
  Microsite --> System[Safety system story]
  Demo --> Review[Public review and discussion]
  Pitch --> Review
  System --> Review
  Review --> WordPress[FaithCheltenham.com project page]
  Review --> GitHub[Protected GitHub surface]
```

## Public / Private Boundary

![Public private boundary](../assets/diagrams/public-private-boundary.svg)

Source Mermaid:

```mermaid
flowchart TB
  Public[Public surface] --> Readme[README and docs]
  Public --> Visuals[Approved visuals]
  Public --> WP[WordPress draft]
  Private[Private engine] --> Source[Source code]
  Private --> Ops[Deploy systems and credentials]
  Private --> Workflows[Prompts, agents, receipts]
  Private --> Product[Future backend and child-safety operations]
  Gate[Review boundary] -. keeps private materials out .- Public
  Gate -. protects .- Private
```
