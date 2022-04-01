# Java and Maven Strategies

This strategy generates SNAPSHOT versions after each release. Snapshot is created as separate "release" Pull Request, which updates all affected files, but does not create actual release or tag.

Snapshot bumps have `autorelease: snapshot` label.

_TODO add screenshot of snapshot bump_

## `java` Strategy

General-purpose Java strategy, that does not update any files on its own.

Uses `extra-files` to bump versions in actual files. For typical Maven project, use `maven` strategy instead. 

## `maven` Strategy

Updates all nested `pom.xml` files using [`PomXml` updater](pom-xml.md).
