# EditorConfig

Boilerplate for an `.editorconfig` file. Read more about EditorConfig on https://editorconfig.org/.

## Support

Some IDEs have built-in support for EditorConfig. If it has not, you may be required to install a plugin in order for it to work.

## File

Create a file called `.editorconfig` in the project root and copy the following code into it.

```editorconfig
# https://editorconfig.org
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

[*.md]
trim_trailing_whitespace = false
```
