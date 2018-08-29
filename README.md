# [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]

> Fork of [conventional-changelog](https://github.com/ajoslin/conventional-changelog) [angular](https://github.com/angular/angular) preset without hidden commit types

## Angular Convention

Angular's [commit message guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit).

### Examples

Appears under "Features" header, pencil subheader:

```
feat(pencil): add 'graphiteWidth' option
```

Appears under "Bug Fixes" header, graphite subheader, with a link to issue #28:

```
fix(graphite): stop graphite breaking when width < 0.1

Closes #28
```

Appears under "Performance Improvements" header, and under "Breaking Changes" with the breaking change explanation:

```
perf(pencil): remove graphiteWidth option

BREAKING CHANGE: The graphiteWidth option has been removed. The default graphite width of 10mm is always used for performance reason.
```

The following commit and commit `667ecc1` do not appear in the changelog if they are under the same release. If not, the revert commit appears under the "Reverts" header.

```
revert: feat(pencil): add 'graphiteWidth' option

This reverts commit 667ecc1654a317a13331b17617d973392f415f02.
```

### Commit Message Format

A commit message consists of a **header**, **body** and **footer**.  The header has a **type**, **scope** and **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

### Revert

If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type

Prefixes are `feat`, `fix`, `perf`, `build`, `ci`, `docs` ,`style`, `refactor`, and `test`.

Details regarding these types can be found in the official [Angular Contributing Guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type)

### Scope

The scope could be anything specifying place of the commit change. For example `$location`,
`$browser`, `$compile`, `$rootScope`, `ngHref`, `ngClick`, `ngView`, etc...

### Subject

The subject contains succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

A detailed explanation can be found in this [document][commit-message-format].

[npm-image]: https://flat.badgen.net/npm/v/conventional-changelog-angular-all-2
[npm-url]: https://npmjs.org/package/conventional-changelog-angular-all-2

[travis-image]: https://flat.badgen.net/travis/wopian/conventional-changelog-angular-all-2
[travis-url]: https://travis-ci.org/wopian/conventional-changelog-angular-all-2

[daviddm-image]: https://flat.badgen.net/david/dep/zeit/pkg
[daviddm-url]: https://david-dm.org/wopian/conventional-changelog-angular-all-2
