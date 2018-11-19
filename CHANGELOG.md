# Sublime Glulx Changelog

This is the CHANGELOG for the Alpha version of [Sublime Glulx].

# 2018/11/19 (2)

- Add "Glulx-Dracula" color scheme.
- Glux Syntax v0.1.1:
    + Add literal characters context.

# 2018/11/19 (1)

First working draft of the package:

- Glux Syntax v0.1.0 (Glulx v3.1.2):
    + comments
    + Glulx opcodes mnemonics
    + glulxe-assemble directives
    + labels
    + numbers (decimal, hex, float)
    + string escape sequences
    + strings
- Syntax test files.
- Settings file:
    + UTF-8 encoding.
- Indentation rules:
    + Increase indentation if a line:
        * ends with a label
        * contains the `.function` directive


<!-----------------------------------------------------------------------------
                               REFERENCE LINKS                                
------------------------------------------------------------------------------>

[Sublime Glulx]: https://github.com/tajmone/sublime-glulx "Sublime Glulx repository on GitHub"


<!-- EOF -->