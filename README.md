# git-disable-autocrlf-action
Disable Git Auto CR/LF Conversion

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
