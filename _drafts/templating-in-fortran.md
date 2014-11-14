---
layout: default
title: Templating in Fortran
---

Templating
----------

Without templating, supporting `double`/`single` precision versions of a
function requires two separate implementations of that function, differing
only in the `real` types of some of their variables. Unfortunately Fortran
does not support templates.
