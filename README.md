# my-first-gen-art ✨🌌

The origin repo for my generative art adventures. Where random seeds turn into neon dreams, flowing particles, and colorful chaos. Blending code & creativity one sketch at a time.

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=34&duration=4500&pause=600&color=FF00FF&center=true&vCenter=true&width=600&lines=Generative+Art+Origins;Neon+Chaos+Unleashed;Code+as+Brush;Randomness+as+Muse;Let's+Paint+the+Future!;🎨💾⚡" alt="neon typing" />
</p>

## What's Inside (So Far)
- Simple sketches to generate abstract visuals
- Neon palettes, noise fields, particles, fractals incoming...
- Python + p5.js experiments (browser-friendly previews coming)

## Inspirational Vibes
These are the kinds of generative magic that fuel me:

<grok-card data-id="36ba93" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="48a38d" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="c616d8" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="ee5117" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="ed6e77" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>


More to come — my own outputs will replace these placeholders soon!

## Quick Start (Python Example)
Install deps if needed: `pip install numpy matplotlib noise` (or use Google Colab for zero setup).

Create `basic-noise-field.py`:

```python
import numpy as np
import matplotlib.pyplot as plt
from noise import pnoise2

width, height = 800, 600
scale = 100.0
octaves = 6
persistence = 0.5
lacunarity = 2.0

img = np.zeros((height, width, 3))

for y in range(height):
    for x in range(width):
        nx = x / scale
        ny = y / scale
        value = pnoise2(nx, ny, octaves=octaves, persistence=persistence, lacunarity=lacunarity, repeatx=width/scale, repeaty=height/scale)
        # Neon vibe mapping
        hue = (value + 1) * 180  # purple-pink-cyan range
        saturation = 80 + value * 20
        brightness = 70 + abs(value) * 30
        # Simple RGB approx for neon
        r = int(brightness * (1 if hue < 120 else 0) + saturation if 180 < hue < 300 else 0)
        g = int(brightness * (1 if 60 < hue < 180 else 0))
        b = int(brightness * (1 if hue > 240 or hue < 60 else 0))
        img[y, x] = [r/255, g/255, b/255]  # Normalize

plt.figure(figsize=(10, 7.5))
plt.imshow(img)
plt.axis('off')
plt.savefig('neon-noise-field.png', bbox_inches='tight', dpi=300)
plt.show()
