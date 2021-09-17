# Astro Stylesheet Component

A simple component to help abstract the monotony of adding stylesheets to any Astro project.

To use simply:

```bash
npm i astro-ui-stylesheet -D
```

Within your `./src/layouts/*.astro` layout file, apply the following:

```astro
---
import Stylesheet from 'astro-ui-stylesheet'
---
<html>
  <head>
    <Stylesheet 
        attributes:Object | Array<Object> = {
          [
            {
              href:string = "./styles/global.css" || Astro.resolve('./src/components/x.css'), 
              media:string = "screen and (max-width:600px)"
            }
          ]
        }
        sanitize:string =  "all" | "bare"| "forms"| "assets"| "typography"|
                            "reducedMotion"| "sysUI"| "monoUI"
    />
 </head>
</html>
```

This would then populate all the relevant `<link rel='stylesheet' href='' type='text/css' media=''>` required in the head of the Layout file.

#### Credits

This project was largely inspired and assisted by [jonathantneal](https://github.com/jonathantneal) from [csstools/sanitize.css](https://github.com/csstools/sanitize.css)