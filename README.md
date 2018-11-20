# Sublime Glulx

    Sublime Glulx v0.1.1 (2018-11-20) | Glulx v3.1.2 | glulx-assemble

- https://github.com/tajmone/sublime-glulx

[Sublime Text 3] syntax definition for [Glulx] VM Assembly, as implemented in [Gren Drake]'s [glulx-assemble]:

- https://www.eblong.com/zarf/glulx/
- https://github.com/GrenDrake/glulx-assemble


-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [Introduction](#introduction)
- [Project Status](#project-status)
- [Syntax Features](#syntax-features)
    - [Build Systems](#build-systems)
        - [Assemble](#assemble)
        - [Assemble and Run](#assemble-and-run)
        - [Assemble and Dump Debug](#assemble-and-dump-debug)
        - [Assemble with All Debug Options](#assemble-with-all-debug-options)
    - ["Glulx Dracula" Color Scheme](#glulx-dracula-color-scheme)
- [Setup Instructions](#setup-instructions)
    - [Installing via Git](#installing-via-git)
    - [Package Customization](#package-customization)
- [License](#license)

<!-- /MarkdownTOC -->

-----

# Introduction

[Glulx] is a 32 bit Virtual Machine for Interactive Fiction (text adventures), created by Andrew Plotkin (aka Zarf) in 1999.

[Glulx-assemble] is an assembler for creating Glulx program files, created by Gren Drake, created in September 2018.

Since glulx-assemble is still a young tool in the making, its syntax might change in the future; therefore, this package should be considered experimental until glulx-assemble reaches a stable release.

That said, I wanted to create a draft package to start working with Glulx source files in Sublime Text, and decided to share it publicly in the hope it might be of use to others, and that feedback from others might help me develop a better tool.

# Project Status

Although in early Alpha stage, this package is already usable; but some syntax elements still need to be implemented. Furthermore, syntax scopes are still in experimental stage and might be changed at any time during the Alpha stage, for I haven't yet worked out which scopes make more sense for some elements.


# Syntax Features

This package automatically associates the "`.ga`" file extension to the Glulx syntax.


## Build Systems

Sublime Glulx ships with some simple [build systems] allowing different options. All the build systems assume that the glulx-assemble binary file is available on the system Path.

### Assemble

The default build system (<kbd>Ctrl</kbd>+<kbd>B</kbd>). It will assemble the current Glulx source file ("`*.ga`") by imparting the following shell command:

    glulx-assemble <filename>.ga <filename>.ulx

where `<filename>.ga` is the current source file.

### Assemble and Run

Same as above, but opens the compiled "`*.ulx`" storyfile after assembling. Imparts the following shell command:

    glulx-assemble <filename>.ga <filename>.ulx && <filename>.ulx

In order to open the compiled file, the "`*.ulx`" extension needs to be associated to a Glulx interpetrer on the local machine (e.g. [Glulxe] or [Windows Git]).

### Assemble and Dump Debug

Assembles the current Glulx source file with `-dump-debug` option and open the generated "`out_debug.txt`" report file in Sublime Text via the [subl] command line tool.

    glulx-assemble -dump-debug <filename>.ga <filename>.ulx && subl out_debug.txt

In order for this buid command to work, Sublime Text's [subl] command line tool must be available on the system Path.

### Assemble with All Debug Options

Assembles the current Glulx source file with every debug option enabled (`-dump-labels`, `-dump-patches`, `-dump-pretokens`, `-dump-tokens` and `-dump-debug`):


    glulx-assemble -dump-labels -dump-patches -dump-pretokens -dump-tokens -dump-debug <filename>.ga <filename>.ulx

After running this build variant, the following debug report files will be created in the source file folder:

- `out_debug.txt`
- `out_labels.txt`
- `out_patches.txt`
- `out_pretokens.txt`
- `out_tokens.txt`


## "Glulx Dracula" Color Scheme

The package ships with an _ad hoc_ color scheme created for the the Glulx syntax (pretty much useless with other syntaxes, at least for now).


This scheme is based on the [Dracula Theme] palette, with some features and settings taken from the [Dracula for Sublime Text] package, both by Zeno Rocha and Copyright &copy; by Dracula Theme, released under MIT License (the full license can be found in the [color scheme source]):

![Glulx Dracula screenshot][screenshot Glulx Dracula]

To enable the Dracula color scheme for Glulx files, open/create your Glulx User settings file (see: [Package Customization]) and add to it:

```json
{
    "color_scheme": "Packages/Glulx/Glulx-Dracula.sublime-color-scheme",
}
```


# Setup Instructions

## Installing via Git

Currently this package has to be installed (and updated) manually via Git, as described below. In the future (once the package has reached maturity) I'll submit it to the official [Package Control] channel, so that it will be possible to install it via Sublime Text's native package manager and not have to worry about updating it. For the time being, here are the manual setup instructions.

Create a "`Glulx`" folder inside "`<data_path>/Packages/`", open a shell inside "`<data_path>/Packages/Glulx/`" and type:

```
git clone https://github.com/tajmone/sublime-glulx .
```

Don't forget the "`.`" after the repository URL! it's needed in order to clone the repository contents directly into the current folder, without creating a "`sublime-glulx`" container folder.

## Package Customization

The User settings file for Glulx should be created in:

`<data_path>/Packages/User/Glulx.sublime-settings`

You can also access it by opening a "*.ga" Glulx file in Sublime Text and then going to the menu "__Preferences__ > __Settings – Syntax Specific__", and Sublime Text will either open the existing Glulx setting file (if it exists) or create a new empty settings file for you.

The package default settings file contains some commented-out settings examples which you can copy and paste to your User Glulx settings and uncomment them according to need:

- [`Glulx.sublime-settings`][Glulx.sublime-settings]


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

<!-- Sublime Text -->

[Package Control]: https://packagecontrol.io/ "Visit Package Control website"
[Sublime Text 3]: https://www.sublimetext.com/ "Visit Sublime Text website"
[build systems]: https://www.sublimetext.com/docs/3/build_systems.html
[subl]: https://www.sublimetext.com/docs/3/osx_command_line.html "Read Sublime Text documentation on subl CLI tool"

<!-- Glulx -->

[Glulx]: https://www.eblong.com/zarf/glulx/ "Visit Glulx homepage"
[Glulx specs]: https://www.eblong.com/zarf/glulx/glulx-spec.html/ "View the Glulx Specs"
[Gren Drake]: https://github.com/GrenDrake "View Gren Drake's GitHub profile"

<!-- Glulx-assemble -->

[glulx-assemble]: https://github.com/GrenDrake/glulx-assemble "Visit glulx-assemble repository on GitHub"

<!-- IF Miscellanea -->

[Glulxe]: http://www.ifarchive.org/indexes/if-archiveXprogrammingXglulxXinterpretersXglulxe.html "Glulxe downloads page at IF Archive"
[Windows Git]: http://www.ifarchive.org/indexes/if-archiveXprogrammingXglulxXinterpretersXgit.html "Windows Git downloads page at IF Archive"

<!-- Dracula Theme -->

[Dracula Theme]: https://draculatheme.com/ "Visit the Dracula Theme website"
[Dracula for Sublime Text]: https://github.com/dracula/sublime "Visit the Dracula for Sublime Text repository"
[color scheme source]: ./Glulx-Dracula.sublime-color-scheme "View source file"

<!-- Screenshots -->

[screenshot Glulx Dracula]: ./screenshots/Glulx-Dracula.png "Screenshot of 'Glulx Dracula' color scheme"

<!-- Project Files -->

[Glulx.sublime-settings]: ./Glulx.sublime-settings "View source file"

<!-- Cross References -->

[Package Customization]: #package-customization "Read the section on Package Customization"

<!-- EOF -->
