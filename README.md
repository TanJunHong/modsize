# modsize.py

A tool used to change the image height/width property of an image. Currently only png files are supported.
<br>Code only works in Linux environment. Modified from original repo to work on Python 3

## Usage

```bash
./modsize.py --help
usage: modsize.py [-h] [--width WIDTH] [--height HEIGHT] file output

positional arguments:
  file                  Filepath to image
  output                Filepath to image

optional arguments:
  -h, --help            show this help message and exit
  --width WIDTH, -sw WIDTH
                        New width of image
  --height HEIGHT, -sh HEIGHT
                        New height of image
```

## Install

* pip install -r requirements.txt
* [pngcsum](http://schaik.com/png/pngcsum.html) (Already included)

## Examples

Image file from X-MAS CTF 2018

*Challenge image*

```bash
$ eog examples/xmasoriginal.png
```
![original challenge image](examples/xmasoriginal.png)


```bash
$ ./modsize.py --height 6000 "examples/celeb.png" out.png
$ eog out.png
```
![example image of modsize](examples/xmasflag.png)

## Known issues

* Modifying the width of an .png file will make the image file unable to be opened: "bad adaptive filter value". Not sure if this is something I can fix
