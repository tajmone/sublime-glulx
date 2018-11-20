# Sublime Glulx TODOs

Annotated list of pending tasks and features wishlist.


-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [Glulx Syntax](#glulx-syntax)
    - [Syntax Elements](#syntax-elements)
- [Build System](#build-system)
- [Color Scheme](#color-scheme)

<!-- /MarkdownTOC -->

-----

# Glulx Syntax

## Syntax Elements

Elements which still need to be implemented:

- [x] __Character literal__ — as a single quote string, supports escapes.
- [ ] __Local variable__.
- [ ] __Local variable index__.
- [ ] __Named constant__.
    + [ ] __Built-in constants__ — `_RAMSTART`, `_EXTSTART`, and `_ENDMEM`.
- [ ] __`opcode` mnemonic__.


# Build System

Simple cross-platform [build systems] invoking the `glulx-assemble` binary (expected to be on the system PATH):

- [x] __Assemble__.
- [x] __Assemble and Run__.
- [x] __Assemble and Dump Debug__.
- [x] __Assemble with All Debug Options__.


# Color Scheme

- [ ] Create an _ad hoc_ color scheme for the Glulx syntax.
    + [x] "Glulx Dracula" (_WIP_)


<!-----------------------------------------------------------------------------
                               REFERENCE LINKS                                
------------------------------------------------------------------------------>

[build systems]: https://www.sublimetext.com/docs/3/build_systems.html

<!-- EOF -->