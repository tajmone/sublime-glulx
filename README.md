# Sublime Glulx

- https://github.com/tajmone/sublime-glulx

Syntax definition for [Glulx] VM Assembly as implemented in [glulx-assemble]:

- https://www.eblong.com/zarf/glulx/
- https://github.com/GrenDrake/glulx-assemble


-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [Introduction](#introduction)
- [Project Status](#project-status)
- [Installation](#installation)
- [License](#license)

<!-- /MarkdownTOC -->

-----

# Introduction

[Glulx] is a 32 bit Virtual Machine for Interactive Fiction (text adventures), created by Andrew Plotkin (aka Zarf) in 1999.

[Glulx-assemble] is an assembler for creating Glulx program files, created by Gren Drake, created in September 2018.

Since glulx-assemble it's a young tool still in the making, its syntax might change in the future. Therefore, this package should be considered experimental until glulx-assemble reaches a stable release.

That said, I wanted to create a draft package to start working with Glulx source files in Sublime Text, and decided to share it publicly in the hope it might be of use to others, and that feedback from others might help me develop a better tool.

# Project Status

Although in early Alpha stage, this package is already usable; but some syntax elements still need to be implemented. Furthermore, syntax scopes are still in experimental stage and might be changed at any time during the Alpha stage, for I haven't yet worked out which scopes make more sense for some elements. 

# Installation

Create a "`Glulx`" folder inside "`<data_path>/Packages/`", open a shell inside "`<data_path>/Packages/Glulx/`" and type:

```
git clone https://github.com/tajmone/sublime-glulx .
```

Don't forget the "`.`" after the repository URL! it's needed in order to clone the repository contents directly into the current folder, without creating a "`sublime-glulx`" container folder.


# License

- [`LICENSE`](./LICENSE)

```
MIT License

Copyright (c) 2018 Tristano Ajmone
https://github.com/tajmone/sublime-glulx

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```


<!-----------------------------------------------------------------------------
                               REFERENCE LINKS                                
------------------------------------------------------------------------------>

[glulx-assemble]: https://github.com/GrenDrake/glulx-assemble "Visit glulx-assemble repository on GitHub"
[Glulx]: https://www.eblong.com/zarf/glulx/ "Visit Glulx homepage"
[Glulx specs]: https://www.eblong.com/zarf/glulx/glulx-spec.html/ "View the Glulx Specs"

<!-- EOF -->
