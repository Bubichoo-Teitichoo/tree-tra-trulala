# Terrible Tree

A modern approach to the old tree command. This was born out of pure boredom
and transformed into a useful tool that replaced the plain `tree` command as well
as `ls` on Windows.

## Usage

Here are a few examples how to run this application

```shell
# ls equivalent
treett --depth 1
```

```shell
# maximum depth, only directories
treett --dirs
```

```shell
# maximum depth of 4, only directories
treett --dirs --depth 4
```

```shell
# maximum depth of 4, only python files
treett --depth 4 -f *.py
```

### Replace `ls` and/or `tree` in Windows PowerShell

Open your PowerShell profile ...

```powershell
nvim $profile
```

... and add the following lines to it

```powershell

function ls_alias {
    treett --depth 1
}

Set-Alias -Name ls -Value ls_alias -Option AllScope
Set-Alias -Name tree -Value treett -Option AllScope
```
