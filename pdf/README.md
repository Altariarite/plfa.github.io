This directory contains the files needed for building a pdf version of the book. Notice the structure is important here: the makefile and latex commands are written based on relative paths.

Dependencies (relative to the root):
- all things under `pdf/`
- agda source files under `src/`
- `_site/acknowledgements.md` generated when building the site
- `README.md`

First, run `stack build && stack exec site rebuild` from the parent directory to generate acknowledgements.md under `_site`, which is needed by the pdf (Only need to do this once). 

Then, running `make pdf` from the parent directory should be sufficient to compile the book. The book will be generated in this folder as `plfa.pdf`.

Alternatively, makefile in this directory provide these options:

```make
all                      # Build plfa.pdf (can also run from the parent as "make pdf")
plfa-sample.pdf          # Build a shrinked version of the book for testing
all_tex                  # generate all tex version of lagda files under tex/
```