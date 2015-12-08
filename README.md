# iiif-static-mandlebrot

*SEE DEMO AT <http://zimeon.github.io/iiif-static-mandlebrot/>*

IIIF Image API static files for Mandlebrot set, overall image 
size is 100,000 x 100,000 pixels. Static files use a tiling of
512 x 512 pixel tiles.

Repository includes a copy of [OpenSeadragon](https://openseadragon.github.io/)
to allow pan/zoom on the set of static tiles.

Tiles generated with [iiif_static.py](https://github.com/zimeon/iiif/tree/master/demo-static).
There are about 51304 image tiles which took about 25h to generate on a laptop (the 
calculation is in python and not optimized, I assume it could be made much faster).

Total size of tiles is ~431MB which is about 0.04 bytes/pixel of the full image.

The command used to gerenate the tiles was:

```sh
./iiif_static.py --generator --include-osd --write-html=/tmp mandlebrot_100k
```

which wrote files to `/tmp` and created an HTML page `mandlebrot_100k` which was renamed to `index.html` and modified slightly.
