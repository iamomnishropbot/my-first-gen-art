# my-first-gen-art ✨🌌

Origin point for my generative art journey. Using code to create neon flows, abstract chaos, and vibrant noise landscapes. Randomness + algorithms = art.

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&size=34&duration=4500&pause=600&color=FF00FF&center=true&vCenter=true&width=600&lines=Generative+Art+Origins;Neon+Chaos+Unleashed;Code+as+Brush;Randomness+as+Muse;Let's+Paint+the+Future!;🎨💾⚡" alt="neon typing" />
</p>

## What's Here Now
One starter sketch: a Perlin noise field rendered in glowing neon pinks, purples, and cyans. Organic waves and clouds with a cyber glow.

## Inspirational Vibes
These capture the kind of neon, flowing energy I'm chasing:

<grok-card data-id="8324ad" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="7b8837" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="6f8607" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="64cf8b" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>



<grok-card data-id="338184" data-type="image_card" data-plain-type="render_searched_image"  data-arg-size="LARGE" ></grok-card>


## The Starter Sketch
```python
import numpy as np
import matplotlib.pyplot as plt
from noise import pnoise2

width, height = 800, 600
scale = 100.0          # Smaller = bigger waves
octaves = 6            # Detail level
persistence = 0.5
lacunarity = 2.0

img = np.zeros((height, width, 3))

for y in range(height):
    for x in range(width):
        nx = x / scale
        ny = y / scale
        value = pnoise2(nx, ny, octaves=octaves, persistence=persistence, lacunarity=lacunarity, repeatx=width/scale, repeaty=height/scale)
        
        # Map to neon pink-purple-cyan glow
        r = int(100 + abs(value) * 155)   # Pink/red glow
        g = int(50 + value * 100)         # Subtle green/cyan
        b = int(150 + abs(value) * 100)   # Strong blue/cyan neon
        
        img[y, x] = [r/255, g/255, b/255]

plt.figure(figsize=(10, 7.5))
plt.imshow(img)
plt.axis('off')
plt.savefig('my-first-neon-cloud.png', bbox_inches='tight', dpi=200)
plt.show()

- Commit changes (message: "Finalize README with visuals and starter sketch")

### Step 3: Add the Python File
- Repo page > Add file > Create new file
- File name: `basic-noise-field.py`
- Paste just the Python code block from above (imports to plt.show())
- Commit message: "Add first generative sketch: neon Perlin noise field"
- Commit new file

### Step 4: Add a Preview Image
- Pick one of the images I rendered above (right-click > Save image as on the ones you like best from the previews).
- Name it something like `my-first-neon-cloud.png`
- Repo page > Add file > Upload files > drag/drop the PNG
- Commit message: "Add example output preview from neon noise sketch"

### Step 5: Pin to Profile
- Go to github.com/iamomnishropbot
- Find "Pinned" section > Customize your pins
- Search/add `my-first-gen-art`
- Save


