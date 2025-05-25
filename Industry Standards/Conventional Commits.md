## Industry Standard Git Commit Message Convention

The most widely adopted and recommended convention for Git commit messages in the industry is the **Conventional Commits** specification. This format is used by major open-source projects (such as Angular) and is favored for its clarity, structure, and compatibility with automated tools and semantic versioning[^3][^7][^8].

### Commit Message Structure

A typical Conventional Commit message consists of three main parts:

```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

- **Header**: Required. Contains the type, optional scope, and a concise description.
- **Body**: Optional. Provides more detailed context about the change.
- **Footer**: Optional. Includes metadata such as references to issues or notes about breaking changes[^3][^7][^8].


#### Example

```
feat(auth): add OAuth2 login support

Implemented OAuth2 login flow for Google and Facebook.
Updates user session handling and stores tokens securely.

Fixes #123
```


### Common Commit Types

| Type | Description |
| :-- | :-- |
| feat | Introduces a new feature |
| fix | Patches a bug |
| docs | Documentation-only changes |
| style | Changes that do not affect code meaning (formatting, etc.) |
| refactor | Code changes that neither fix a bug nor add a feature |
| perf | Improves performance |
| test | Adds or updates tests |
| chore | Changes to build process, tooling, or auxiliary files |
| build | Build system or external dependency changes |
| ops | Operational, infrastructure, or deployment changes |

[^3][^4][^5][^7][^8]

### Best Practices

- **Subject line**: Limit to 50 characters, use the imperative mood (e.g., "add" not "added"), capitalize the first letter, and do not end with a period[^1][^4][^6][^9].
- **Body**: Wrap at 72 characters, explain the "what" and "why" (not the "how"), and separate from the subject with a blank line[^1][^4][^6][^8].
- **Footer**: Reference issues or breaking changes as needed. Use `BREAKING CHANGE:` in the footer or an exclamation mark in the header for breaking changes[^5][^7][^8].
- **Consistency**: Use the same format across your team or project for readability and automation[^3][^9].


### Why This Convention?

- **Clarity**: Makes it easy for contributors and reviewers to understand the nature and intent of changes.
- **Automation**: Enables tools to generate changelogs, automate versioning, and enforce standards.
- **Traceability**: Helps link commits to issues, pull requests, and documentation for better project management[^3][^7][^8].


### Summary Table

| Element | Rule/Recommendation |
| :-- | :-- |
| Type | Use from the accepted list (feat, fix, etc.) |
| Scope | Optional, specifies affected module/component |
| Subject | 50 chars max, imperative, no period |
| Body | Optional, 72 chars per line, explain what/why |
| Footer | Optional, for issues/breaking changes |

### References

- [Conventional Commits Specification][^7]
- [Best Practices and Examples][^3][^4][^8]
- [AngularJS Commit Guidelines][^1]

**Adopting the Conventional Commits convention is considered the industry standard for clear, maintainable, and automatable Git commit messages.**

<div style="text-align: center">⁂</div>

[^1]: https://www.theserverside.com/video/Follow-these-git-commit-message-guidelines

[^2]: https://dev.to/tuasegun/a-guide-to-writing-industry-standard-git-commit-message-2ohl

[^3]: https://graphite.dev/guides/git-commit-message-best-practices

[^4]: https://gist.github.com/Aditi3/a7a1ddd1ecef73dab548f7955210cfff

[^5]: https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13

[^6]: https://gist.github.com/tonibardina/9290fbc7d605b4f86919426e614fe692

[^7]: https://www.conventionalcommits.org/en/v1.0.0/

[^8]: https://axolo.co/blog/p/git-commit-messages-best-practices-examples

[^9]: https://www.gitkraken.com/learn/git/best-practices/git-commit-message

[^10]: https://www.reddit.com/r/learnprogramming/comments/tk87nv/where_to_find_professional_git_conventions/

