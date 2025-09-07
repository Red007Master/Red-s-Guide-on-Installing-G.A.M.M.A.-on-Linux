# TMPDIR size:

## TLDR:
So you got something like:
```
RuntimeError: You need at least 12 GiB of space in TMPDIR for this to work.
Please export TMPDIR to a folder with enough space available.
```

Problem is that your `TMPDIR` is smaller that it is required.

`TMPDIR` in most cases is `/tmp` you can check it's size with `df -h /tmp`.

## Solutions:
So you have two options:
1. Increase the size of `/tmp`.
2. Use custom path for your `TMPDIR`.

### 1 Increase the size of `/tmp`. *(Not recommended)*
You need to unmount your `/tmp` and re-mount it.

### 2 Use custom path for your `TMPDIR`. *(Recommended)*
Create folder in user(you) owned folder, for example external drive:
`/media/your-drive/gammatmp`
Where `gammatmp` is folder that you created for `TMPDIR`.

Then run `export TMPDIR=/media/your-drive/gammatmp` if you have spaces or something like this in path use `"`, e.g: `export TMPDIR="/media/your drive/gammatmp"`.

To see if it worked run `echo $TMPDIR` you should get your path back (e.g: `/media/your-drive/gammatmp` or `/media/your drive/gammatmp` in this example).

*Important:* Run `gamma-laucher` in *SAME* terminal in which you did these manipulations.

`export` is temporary and works *ONLY* in terminal in which you used it.