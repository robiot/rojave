# rojave
A Macos inspired openbox theme

## How to install?
```bash
cd ~/.themes
git clone --depth 1 https://github.com/robiot/rojave.git
```

## Pathing openbox
You may notice the title is not fully centered, this can be fixed by changing one line in the openbox souce code.

```bash
git clone --depth 1 https://github.com/danakj/openbox.git
cd openbox

# Now open up a text editor in openbox/framerender.c
# Go to the function framerender_label (around line 351)
# In the RrPaint function call, change self->label_width to self->width
# The line should now look like this: RrPaint(a, self->label, self->width, ob_rr_theme->label_height);
./configure --prefix=/usr \
    --with-x \
    --enable-startup-notification \
    --sysconfdir=/etc \
    --libexecdir=/usr/lib/openbox

# Build it
make
# Install it
sudo make install
```
