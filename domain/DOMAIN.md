# DOMAIN

## What is the "domain"? What is a "model"?

- Domain modeling is the modeling of a domain of interest. Not a canonical, overarching domain but a subset
you are interested in. E.g. a seat can have numbers in a context that mandates assigned seating e.g. flight bookings
but not in another which does not e.g. watching a music concert; the domains differ even though they are dealing with
the same object i.e. seat. The domains differ because the contexts differ.
- why have a model?
- why prefer Value Objects?
- how does good OOP mirror FP (or vice-versa)?
  - immutability
  - sensible data structures underpinning immutable objects
  - sacrifice performance by default
- how is good OOP different from FP?
  - prefer fine-grained abstraction pushed to "leaf nodes" of the object hierarchy
  - avoid highly generic constructs

- [tbd - domain-v-model.jpg]

## Objects capture *lifetimes*

- nouns to capture ephemeral/lifetime ideas: session (other examples?)
- the lifecycle of an object is more important than mirroring the real world

## Non-standard domains

- the web server itself can be a domain
- a scheduler object(s)
- Try: push as much of your code into the "domain" as possible
  - pure
  - immutable
  - small & value-based
  - in clojure, this is capturing more *data* and less behaviour

## Domain through API

- REST v CRUD
- Representational State Transfer - why?
- HTTP verb hacks
- immutability behind the scenes w mutable APIs
- DTOs
