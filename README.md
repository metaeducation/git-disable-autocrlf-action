# git-disable-autocrlf-action

GitHub CI checkout on Windows auto translates LF to CR/LF in files:

<https://github.com/actions/checkout/issues/135>

The long view on this--which causes the least problems cross-platform--is to and prohibit CR/LF in source by default.

<http://blog.hostilefork.com/death-to-carriage-return/>

While this is a trivial GitHub action, putting the behavior into an action means that this README.md can point to the rationale behind it, so that every usage site doesn't have to document it.

## Usage

Add this action to your workflow to disable Git's automatic CRLF conversion:

```yaml
- uses: metaeducation/git-disable-autocrlf-action@v1
```

## What it does

This action configures Git to:
- Disable automatic line ending conversion (`core.autocrlf false`)
- Set the end-of-line character to LF (`core.eol lf`)

This is useful when you want to ensure consistent line endings across different operating systems and prevent Git from automatically converting line endings.
