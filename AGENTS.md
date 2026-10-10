# dbcontext

> Repository: `botopink/dbcontext` (`git@github.com:botopink/dbcontext.git`) · in the meta checkout: `repository/dbcontext/`

The persistence layer over erika (decision 398) — botopink's JPA: `#[dbcontext.entity(…)]` (it
records erika's `QueryTable`), `DbContext` (erika's `QueryContext`, over a `Driver` behavior),
`#[dbcontext.repository]` on a `behavior`, `#[dbcontext.sql "…"]` (erika's grammar) and
`#[dbcontext.nativeQuery(…)]` (the driver's SQL), rows decoded into the declared answer by column
name. It depends on erika and std and names no framework (113): rakun-data supplies the drivers,
the container registration and the transactions. Filled by `specs/1.0.12-beta/04-rakun/143-dbcontext`;
until its steps land this repository holds only its scaffold. One consumer today (rakun-data): the
maintainer's exception to 115, stated in 398.

## Hooks

Every clone runs the shared pre-commit gate:

```sh
git config core.hooksPath scripts/git-hooks
```

`scripts/git-hooks/pre-commit` and `scripts/git-hooks/lib/runner-standalone.sh` are byte-identical
across the library repositories (the meta repository's CI check 4); edit them in one place and copy.
