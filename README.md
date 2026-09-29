These use domdiv scripts installed in ~/.local/share/uv/tools/domdiv/
    bin/dominion_cricut_svg
    lib/python3.14/site-packages/domdiv/cutsvg.py

config/domdiv runs the cricut and the dividers with common options:

```
~/.local/share/uv/tools/domdiv/bin/dominion_cricut_svg \
-c $DIR/mropts \
-c $DIR/cutsvg \
--expansions="$@"
```

```
~/.local/share/uv/tools/domdiv/bin/dominion_dividers \
-c $DIR/mropts \
--expansions="$@"
```

Following the README.md we do a `uv tool update domdiv` from the fresh
checkout.  `uv tool install domdiv` was the installation step that got
it to ~/.local/share/uv/tools/domdiv

For Rising Sun I run `config/domdiv "Rising Sun"`

Previously the tab-number defaulted to 1 with `tab-side right`.
somewhere the default changed to tab-number 2, which didn't keep the
tab-side (but chose which to start on).  So I printed a set of dividers
with the alternating tabs.  To reproduce this (for example to get the
cuts files), run:

`config/domdiv "Rising Sun" --tab-number 2`
