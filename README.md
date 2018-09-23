# rfcs
Somewhere to start to discuss how a 2d drawing library would work in rust, whether it is necessary, and what it should look like.

The idea is that we replace these questions with statements over time (& expand on them) until we have a plan.

## Requirements

What problem is this library trying to solve? Who would benefit from it?

 - 2d games?
 - desktop UI?
 - webrender?
 - ...?
 
What exactly is the problem in each of these area that needs solving?

## Prior art

Do any of these solve the above problems today? Could they solve them after improvement? If not, can we learn from them?

### Rust

 - [`ggez`]
 - [`piston`]/[`conrod`]
 - [`amethyst`]
 - [`resvg`]
 - ...?
 
## Non-rust with wrapper
 - gtk
 - qt
 - cairo
 - pango
 - what does webrender do?
 - ...?

## Interaction with other functionality

Unix philosophy - solve one problem well and be composable.

 - Windowing
   - [`winit`]
 - Surface creation
   - We probably have to wrap this functionality rather than be composable?
 - Event processing
   - [`winit`]
 - scene graphs
 - fonts
 - what other functionality do we interact/overlap?
 
## Dependencies

I would think we could write something on top of gfx-ll and then be able to run on all the backends it supports.
Do we need anything else? How can we be as fast (& low power) as possible?

[`ggez`]: https://github.com/ggez/ggez
[`resvg`]: https://github.com/RazrFalcon/resvg
[`amethyst`]: https://github.com/amethyst/amethyst
[`winit`]: https://github.com/tomaka/winit
[`piston`]: https://github.com/PistonDevelopers/piston
[`conrod`]: https://github.com/PistonDevelopers/conrod
