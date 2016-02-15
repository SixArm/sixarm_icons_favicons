SixArm.com » Icons » Favicons as 16x16 png files for many popular sites

Do you want favicons added here?

Email us at sixarm@sixarm.com and we'll do our best to add them for you.

## How to fetch a favicon

To fetch the favicon for a domain, by using curl and the typical URL:

    curl -sSSL http://example.com/favicon.ico -o favicon.ico

To fetch the favicon for a domain, by using Google:

    http://www.google.com/s2/favicons?domain=www.google.de


To fetch the favicon for an URL, by using Google:

    http://www.google.com/s2/favicons?domain_url=http%3A%2F%2Fwww.google.de%2F

## How to convert ico to png

To convert the favicon.ico file from the .ico file format to a new .png file format, we use the `convert` command that comes with ImageMagick.

     convert favicon.ico -thumbnail 16x16 -alpha on -background none -flatten favicon.png

## How to create a srcset a.k.a. source set

To convert four file sizes, using our naming conventions:

    convert favicon.ico -thumbnail 16x16 -alpha on -background none -flatten favicon-16x16.png
    convert favicon.ico -thumbnail 32x32 -alpha on -background none -flatten favicon-32x32.png
    convert favicon.ico -thumbnail 48x48 -alpha on -background none -flatten favicon-48x48.png
    convert favicon.ico -thumbnail 64x64 -alpha on -background none -flatten favicon-64x64.png

    ln -sf favicon-16x16.png favicon-16x16-1x.png
    ln -sf favicon-32x32.png favicon-16x16-2x.png
    ln -sf favicon-48x48.png favicon-16x16-3x.png
    ln -sf favicon-64x64.png favicon-16x16-4x.png

## Sprites

To create sprites, we use [glue](https://github.com/jorgebastida/glue).
