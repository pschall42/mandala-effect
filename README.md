# The Mandala Effect
This was a creative coding project I started in late September 2021 using [tiny-artblocks](https://github.com/mattdesl/tiny-artblocks) as a base. This is a snapshot of the latest stable version from late October 2021, after which I shelved the project due to the rising price of ETH.

I may revisit this project again in the future, though I'm thinking of rewriting it in [Purescript](https://www.purescript.org/) if I do since I had to do a lot of tricks to optimize the size of the minified JS, and I want to see if Purescript could automate some of that.

## Viewing
You can view the artwork it generates [here](https://htmlpreview.github.io/?https://github.com/pschall42/mandala-effect/www/index.html). If you see something you like and want to save it, you'll need to find the hash used to generate it by opening up developer tools in your browser and inspecting the web console. You will see a 64 character hexadecimal hash (66 characters counting the `0x` prefix), which you need to copy and add as the `hash` query parameter at the end of the url, which should give you a URL that looks something like this:
[https://htmlpreview.github.io/?https://github.com/pschall42/mandala-effect/www/index.html?hash=0x0ff009594ebae4e28e388dc466db04cce84b1d7219225a7ca9a23539f44b6cc1](https://htmlpreview.github.io/?https://github.com/pschall42/mandala-effect/www/index.html?hash=0x0ff009594ebae4e28e388dc466db04cce84b1d7219225a7ca9a23539f44b6cc1)

## Development
I started the project by looking at some of the [examples](https://p5js.org/examples/) for [p5.js](https://p5js.org/). I wanted to do something that demonstrated emergent complexity, and found the [Wavemaker](https://p5js.org/examples/interaction-wavemaker.html), [Kaleidoscope](https://p5js.org/examples/interaction-kaleidoscope.html), and [Spirograph](https://p5js.org/examples/simulate-spirograph.html) most interesting, so I started with combining several of their concepts.

Once the base was done, I varied the particle shapes, direction, color, speed, and other properties, added a buffering system so that the size and shape of the Mandala was consistent, added a layering system so that draw particles wouldn't cover up animated particles on the canvas, random variation in those layers where they can have a chance to rotate, a color gradiant system so that there was a chance of either the particles or background of changing color, and a color contrast system to try to minimize the chance of having particles blend in with the background.

## About the Name
I noticed early on the animations looked like mandalas, and I thought it would be fun to combine it with the [Mandela effect](https://en.wikipedia.org/wiki/False_memory#Mandela_effect) as a pun.