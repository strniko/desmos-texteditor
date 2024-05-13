## Modular Setup Tutorial
### Custom fonts:
To add a new font set up the following variables as described.

$f_{f}$ is the main font variable. Set it up using a list of whatever letter symbols you want. In this example I used the parametric equations generated by [Jared Hughes's Tampermonkey extension](https://github.com/jared-hughes/svgToDesmos) (thanks). The index of the icon in the list should correspond to the ASCII or UNIcode UTF-8 decimal character codepoint. The list should immediately be indexed by $f_{fn}$. The resulting symbol then gets multiplied with the size factor $f_{fs}$, before adding the displacement point $f_{fd}$.

$$f_{f} = [\text{your symbol list}][f_{fn}]\times f_{fs} + f_{fd}$$

Define the standard variables as follows.

$$f_{fn} = 1$$

$$f_{fs} = 1$$

$$f_{fd} = (0,0)$$

Choose and initialise a font hitbox, describing the size of your letter symbols. Your hitbox $f_{fh}$ should be a list of the most bottom-left and top-right points that in this version are equal for every letter (monospace).

$$f_{fh} = (0,0), (1,1)$$
