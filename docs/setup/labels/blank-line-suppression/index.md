---
sidebar_position: 10
sidebar_label: 'Blank Line Suppression'
---

# Blank Line Suppression Macro

To prevent blank lines when a merge field is blank, you can add a blank line suppression macro by following these steps:

1. Surround your merge fields with the following syntax: `~:  :~`

```
{FirstName} {LastName}
~:{Title}:~
{Email}
```

### Result when Title merge field has a value:
```
Jane Doe
President
j.doe@acme.com
```

### Result when Title merge field does not have a value:
```
Jane Doe
j.doe@acme.com
```