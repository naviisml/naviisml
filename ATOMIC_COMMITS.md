# Atomic Commits

Atomic commits, in short, are what they sound like: atomic. I feel like thereβs basically three features a commit needs to have to be atomic:

1. Every commit pretains to one fix or feature
2. Don't break the build on any commit
3. Purpose is clear from commit message and description _(See [Commit Message Structure](#commit-message-structure))_

## Why?

- Code reviews are more efficient, because each commit only focuses on **one** single change.
- Bug fixes can be tested more easily since only relevant changes are grouped together.
- Commits can be rolled back without leaving the system in an inconsistent state.

## Emoji Prefixing

- The use of emoji allows the developer to foresee how the commit changes the code.
- Associating a single emoji with the type of commit helps the developer make more focused changes.
- Adopting this style guide supports consistency and uniformity, resulting in cleaner repositories, prettier git logs and happier devs! βοΈ + π = β€οΈ

## Commit Message Structure

`[ Emoji ]` + `[ Title ]` + `[ Description ]`

`[ Emoji ]` is defined as one of the following items below:

| Emoji | Description |
|:-----:| ----------- |
|  π   | The commit introduces a bug fix, which ideally references the commit where the bug was introduced. |
|  π   | The commit introduces an emergency bug fix. |
|  π¨   | The commit refactors existing code, without changing its functionality. |
|  π   | The commit introduces a new style or style change, which must not affect the logic of any existing code. |
|  β οΈ   | The commit introduces a breaking feature. |
|  π,π   | The commit introduces a non-breaking feature. |
|  π   | The commit merges two branches. |
| π β | The commit resolves a merge conflict. |
|  βͺ   | The commit reverts an existing change. |
|  βοΈ   | The commit improves an existing feature or otherwise existing code. |
|  β»οΈ   | The commit removes unneeded or dead code. |
|  β   | The commit introduces one or more unit tests. |
|  π¨   | The commit introduces, modifies or removes assets such as images. |
|  π   | The commit introduces, modifies or removes localization such as translation files. |
|  π   | The commit introduces documentation for code, instructions to compile, install or run code inside of the current repository. It may also be used for adding, changing or removing Markdown documents. |
|  βοΈ   | The commit resolves a spelling mistake, such as a typo or grammatical error (within the changes of the commit, not the message itself). |
|  π   | The commit manages dependencies such as package.json files (adding, changing or removing). |
|  π   | The commit creates a new deployment. |
|  π¦   | The commit version tags a deployment.|
|  π   | The initial commit. |

`[ Title ]` is a brief but descriptive title written in the imperative present tense. The `[ Title ]` must **not** end with a period as it is not a sentence, but a command. Each commit directs the repository to perform an action.

`[ Description ]` is optional text following the `[ Title ]`, which adds additional information about the changes the commit is introducing. It should only be included when the `[ Title ]` cannot fully describe the intent of the commit. The `[ Description ]` is typically included for critical or complex code, such as security patches.

The `[ Description ]` must begin with a new line to separate itself from the `[ Title ]`. This text should be grouped into small paragraphs, which are also separated by new lines. For improved context, links to external content or references are also encouraged to be included in the `[ Description ]`.

The `[ Title ]` and `[ Description ]` may also contain additional emojis to enhance the clarity and brevity of a commit message.

Example of a well formatted commit message: `π Fix race condition introduced in 9e4d83a`

## Pro Tip

Sign your commits using your PGP key to verify you are the real author. Learn more about signed commits [here](https://help.github.com/articles/signing-commits-using-gpg).
