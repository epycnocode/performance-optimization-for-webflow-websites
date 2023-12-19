# Performance Optimization for Webflow Websites

**Webflow Speed Demon: Unleash your site's inner Usain Bolt with code tricks!**

Let's ditch the loading spinner and turn your Webflow site into a performance champion! Here are some code-infused tips to supercharge your speed:


Webflow Speed Demon: Unleash your site's inner Usain Bolt with code tricks!
Let's ditch the loading spinner and turn your Webflow site into a performance champion! Here are some code-infused tips to supercharge your speed:

**1. Async Hero:** Don't hold your visitors hostage with heavy scripts. Use async attribute on non-critical scripts like social media plugins. Example:

```
HTML
<script async src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

```

**2. Lazy Loading Lazy Bones:** Images below the fold? Chill, they can wait! Use Webflow's built-in lazy loading or a custom script like this:

```
JavaScript
const images = document.querySelectorAll('img[data-lazy-src]');

images.forEach(image => {
  image.addEventListener('load', () => image.classList.add('loaded'));
  image.src = image.dataset.lazySrc;
});
```

**3. Minify Maestro:** Shrink your CSS and JS like a tiny dancer. Webflow Designer already helps, but tools like UglifyJS can squeeze out even more bytes:

```
uglifyjs my-script.js -o optimized-script.js
```

**4. Preloading Pro:** Tell browsers exactly what they need upfront. Use <link rel="preload"> for critical assets like your main CSS and fonts:
```
HTML
<link rel="preload" href="styles.css" as="style">
<link rel="preload" href="fonts/myfont.woff2" as="font">

```
**5. Font Faceoff:** Limit custom fonts to essential elements. Use ```@font-face``` only for those, leaving generic fonts for the rest:
```
CSS
@font-face {
  font-family: 'MyFancyFont';
  src: url('myfont.woff2') format('woff2');
}

h1 {
  font-family: MyFancyFont;
}
```


# Need help?
Stuck with custom css code? [Contact us](https://epyc.in/).
