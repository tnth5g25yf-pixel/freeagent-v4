# assets folder

This folder contains starter artwork for the Expo app. Two SVG files were added as starter artwork:

- assets/icon.svg — 1024×1024 square icon (ideal source for app icons)
- assets/splash.svg — 2732×2732 splash artwork (large, high-resolution)

Current PNG placeholders (assets/icon.png and assets/splash.png) are small placeholders. To use the SVGs as actual PNG assets for Expo you should convert them to PNG at the recommended sizes and overwrite the PNG files.

Recommended conversion commands (choose one):

1) Using Inkscape (cross-platform):

   inkscape assets/icon.svg --export-filename=assets/icon.png -w 1024 -h 1024
   inkscape assets/splash.svg --export-filename=assets/splash.png -w 2732 -h 2732

2) Using rsvg-convert (Linux / libRSVG):

   rsvg-convert -w 1024 -h 1024 -o assets/icon.png assets/icon.svg
   rsvg-convert -w 2732 -h 2732 -o assets/splash.png assets/splash.svg

3) Using ImageMagick (may rasterize fonts differently):

   magick convert -background none -resize 1024x1024 assets/icon.svg assets/icon.png
   magick convert -background none -resize 2732x2732 assets/splash.svg assets/splash.png

4) Using a Node.js tool like sharp (script example):

   npx sharp assets/icon.svg -resize 1024 1024 -png -o assets/icon.png
   npx sharp assets/splash.svg -resize 2732 2732 -png -o assets/splash.png

After converting, commit the PNG files:

   git add assets/icon.png assets/splash.png
   git commit -m "Replace placeholder PNGs with starter artwork"
   git push

If you want, I can convert the SVGs into PNGs for you and push the resulting PNGs to the repo now — tell me which tool/size you prefer (recommended sizes: icon 1024×1024, splash 2732×2732) and I'll generate and push them.
