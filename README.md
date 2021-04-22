# Magic Chocolate solver

Solve the magic chocolate puzzle.  This is an illusion that makes it appear as though one can create extra pieces of chocolate just by re-arranging them.

The original illusion is shown in the video *Le carré de chocolat en trop! The Infinite Chocolate!* by "moteurelec90" on YouTube.  You can watch the video at the link https://youtu.be/yWXM65MV8lU

The solution program given here generates five diagrams that show precisely how the chocolate pieces are moved.  By examining these diagrams, it should become clear where the "extra" piece of chocolate comes from.

## Building the solution

The program is a PostScript program that generates five pages, each with dimensions 8.5" x 11" (US Letter size).  You should be able to run it with any PostScript interpreter.

To use GhostScript, you can use the following invocation:

```
gs
  -sDEVICE=pngalpha
  -sOutputFile=chocolate_%02d.png
  -r72
  -dNOPAUSE
  -dBATCH
  -sPAPERSIZE=letter
  chocolate.ps
```

This will interpret the solution program `chocolate.ps` and use it to generate five PNG files containing the diagrams.
