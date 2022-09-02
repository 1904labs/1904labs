# 1904labs

1904labs Public Assets

This repository contains assets to embed in emails and websites that may need to be revisioned

All files here are available for read-only use and no promises are given that they won't change.

## Building the transparent SVG images

When we get another year of Top Workplace, the easiest thing to do is to just copy and edit the SVG from the previous year and change the last digit in the couple of places needed. 

There are two SVG versions. The main one has a `fill="#fff"` (white) on the background `rect` and the bottom text is in #000 (black). The other SVG (with suffix of -Transparent) has a `fill="none"` (transparent) on the background `rect` so the entire badge is transparent and the bottom text is emitted in the same color as the left-badge text with `fill=#001450` on the `.st8` CSS class in the SVG.

When generating the SVG's versions as PNG files, we generate 3 variants of each of the white or transparent background This means that for `TopWorkPlace_2018-2022.svg` we manually generate three files using a [website](https://www.svgtopng.me/) because it allows you to set all the right attributes trivially.

The three sizes are for big images with no suffix (e.g. `TopWorkPlace_2018-2022.png`) is generated at *1920x1100* (wXh) using no background color and no forcing of transparent [see](doc/1920x1100-White.png) for settings example. We also generate a banner size (e.g. `TopWorkPlace_2018-2022-Banner.png`) at *325x202* (wXh) and finally at a really small banner used in the email signature block (e.g. `TopWorkPlace_2018-2022-Banner-Small.png`) at *188x102* (wXh).

For the transparent versions we need to set a forced color for browsers that ignore the alpha channel [see](doc/1920x1100-Transparent.png) for settings (and an explainer on why) and put `-Transparent` in the name.
