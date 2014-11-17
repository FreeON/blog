---
title: Templating in Fortran
---

# {{ page.date | date_to_string }} - {{ page.title }}

Without templating, supporting `double`/`single` precision versions of a
function requires two separate implementations of that function, differing
only in the `real` types of some of their variables. Unfortunately Fortran
does not support templates. For spammpack we went a sort of C-style
pre-preprocessor driven path. Instead of using the Fortran preprocessor or
`cpp` explicitly, we employ CMake's `configure_file` command to produce two
versions of the module files.
