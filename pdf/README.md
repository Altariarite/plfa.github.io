This directory contains the files needed for building a pdf version of the book. Notice the structure is important here: the makefile and latex commands are written based on relative paths.

First, run `stack build && stack exec site rebuild` to generate acknowledgements.md under `_site`, which is needed by the pdf (Only need to this once). Then, running `make pdf` from the parent directory should be sufficient to compile the book. The book will be generated in this folder as `plfa.pdf`.

```make
all                      # Build plfa.pdf (can also run from the parent as "make pdf")
plfa-sample.pdf          # Build a shrinked version of the book for testing
all_tex                  # generate all tex version of lagda files under tex/
```