---
id: 1720953199-keyboard-layout
aliases:
  - keyboard layout
tags: []
---

# keyboard layout

[A guide to alt keyboard layouts (why, how, which one?)](https://getreuer.info/posts/keyboards/alt-layouts/index.html#magic-sturdy)

currently using glove 80 for majoy usage 
keyman for mac built-in usage

https://bit.ly/keyboard-layouts-doc

# My current setting

turnoff `combo_sticky_1shot_shift_left` for tmux

```
#ifndef HOMEY_HOLDING_TIME
#define HOMEY_HOLDING_TIME 120
#endif
#ifndef HOMEY_STREAK_DECAY
#define HOMEY_STREAK_DECAY 150
#endif
#ifndef INDEX_HOLDING_TIME
#define INDEX_HOLDING_TIME 120
#endif
#ifndef INDEX_STREAK_DECAY
#define INDEX_STREAK_DECAY 100
#endif
#ifndef PLAIN_HOLDING_TIME
#define PLAIN_HOLDING_TIME 120
#endif
#ifndef PLAIN_STREAK_DECAY
#define PLAIN_STREAK_DECAY 150
#endif
#ifndef SPACE_HOLDING_TIME
#define SPACE_HOLDING_TIME 120
#endif
#ifndef SPACE_STREAK_DECAY
#define SPACE_STREAK_DECAY 130
#endif
```

---
created: 2024-07-14T18:34:02 (UTC +08:00)
tags: []
source: https://getreuer.info/posts/keyboards/alt-layouts/index.html#magic-sturdy
author: Pascal Getreuer, 2022-05-15 (updated 2024-07-01)
---

# A guide to alt keyboard layouts (why, how, which one?)

> ## Excerpt
> ← More about keyboards

---
-   **Check that you can type your computer password in the new layout**… otherwise you might get locked out.
    
-   **Use proper touch typing form when practicing.** Keyboard layouts are designed assuming which finger presses which keys. This determines which key pairs create SFBs. If your typing form is nonstandard, this changes (likely dramatically for the worse) the layout’s frequency of SFBs. Learning a new layout is an opportunity to brush up your form. See also: [Should I learn how to touch type?](https://getreuer.info/posts/keyboards/alt-layouts/index.html#magic-sturdy../faqs/index.html#should-i-learn-how-to-touch-type)
    
-   **Be careful about rearranging keys in a layout** for the same reason. Shifting a row or swapping some keys arbitrarily is likely to ruin the layout. If you’re really tempted to do this, use a tool like the [colemak mods analyzer](https://colemakmods.github.io/mod-dh/analyze.html) or [Oxey’s layout playground](https://o-x-e-y.github.io/layouts/playground/index.html) to check how metrics are affected.



---
created: 2024-07-14T22:17:51 (UTC +08:00)
tags: []
source: https://getreuer.info/posts/keyboards/tour/index.html
author: Pascal Getreuer, 2022-10-09 (updated 2024-05-02)
---

# Tour of split ergo keyboards

> ## Excerpt
> ← More about keyboards
[Keyboard FAQs](https://getreuer.info/posts/keyboards/faqs/index.html#home-row-mods-are-hard-to-use)
- basically contains lot of useful info

---
### Tips to get a good keyboard

Ergonomic keyboards differ in placement of the thumb buttons as well as in the stagger and splay or the columns. You can use [Splitkbcompare](https://jhelvy.shinyapps.io/splitkbcompare/) to make 1:1 prints for many popular keyboards to test how they fit your hands.

Keyboards often use cheap AVR microcontrollers, like the Pro Micro and Elite-C boards with the ATmega32U4 microcontroller. While they are enough to get running, AVR microcontrollers have a stingy amount of flash space, and you’ll need to be sparing in which firmware features to enable in order to fit in that space (see [Squeezing the most out of AVR](https://docs.qmk.fm/squeezing_avr)). If you have an option to use a better microcontroller, I’d recommend it.


keyboard manager like karabiner :
[kmonad/kmonad: An advanced keyboard manager](https://github.com/kmonad/kmonad)
[jtroo/kanata: Improve keyboard comfort and usability with advanced customization](https://github.com/jtroo/kanata)
- this one i think it is better
[Keyboard FAQs](https://getreuer.info/posts/keyboards/faqs/index.html#home-row-mods-are-hard-to-use)

---

[jtroo/kanata: Improve keyboard comfort and usability with advanced customization](https://github.com/jtroo/kanata)

- fixed conflic btw keypress and home row mod at the same time

---

# mac home row mode

[🌱 A Good Way to Get Home Row Mods on a Mac | Havn](https://havn.blog/2024/03/03/a-good-way.html)

[How to configure Home Row Mods with KMonad on macOS](https://gist.github.com/amiorin/4c74f63fe599a1dcbd0933628df1aac9)

I am working on a [keyboard layout](https://github.com/argenkiwi/kenkyo) and I would also like to know what the recommended implementation of home row modifiers is using Karabiner. I attempted to achieve this using [Goku](https://github.com/yqrashawn/GokuRakuJoudo) but I have not succeded so far. [Kanata](https://github.com/jtroo/kanata) (and Kmonad) do seem to achieve this a lot more easily.

I used karabiner.ts to recreate a better configuration.
My home row now works pretty well, and I add a chord modificator too a s to enable the arrows with the letters jkli

Here is my configuration:
https://github.com/emadb/karabiner-config/blob/main/karabiner.json

In case some of you are interested here it is the typescript definition:

layer(['caps_lock', 'return_or_enter'], 'mod-layer').manipulators([
    map('a').to('left_shift'),
    map('s').to('left_control'),
    map('d').to('left_option'),
    map('f').to('left_command'),
    
    map('quote').to('right_shift'),
    map(';').to('right_control'),
    map('l').to('right_option'),
    map('k').to('right_command'),
  ]),

  duoLayer('a', 's').manipulators([
    map('i').to('up_arrow'), 
    map('j').to('left_arrow'), 
    map('k').to('down_arrow'), 
    map('l').to('right_arrow'),
  ])


---

# updating from previous edition:

Hi, how do I update to v37 while making sure that some changes I made to v36 are carried over? do I need to re-do them again after cloning v37?


1. Use the JSON export facility (via "Advanced Settings" > "Enable local config" then go back to "Edit" and click "Download") in the Glove80 Layout Editor to get a locally editable version of any keymap. Then you can easily copy/paste entire layers from my keymaps and adapt them to your liking. Finally, you can import your locally modified JSON file back into the editor via the "Upload" button.

2. or Okay, how about this: save your current CBD snippet to the keymap.dtsi file in the repository (overwriting it). Now you can run git diff to see what changes you've actually made so far. 💡✨  Then git stash your changes, regenerate the keymap.dtsi file via rake command, and finally git stash apply to replay your changes back on top. 
 
3. I would try using the "Copy select layers to editing layout" button in the Layout Editor:
    Open my v34 release keymap
    Click the "Clone to Edit" button
    Open your v33 based keymap
    Click the "Copy select layers to editing layout" button
    Choose the base layer (and any other layers you want to copy)
    Click the "Edit layout" tab at the top
    The layers you copied in step 5 will now be at the bottom of your layers tower 🗼 so drag & drop them back to the top (or wherever you want)

    Alternatively, you can manually diff the JSON exports and merge the arrays yourself.



---
kanata (Cross platform karabiner)

[Moosy Research - Homerow Mods explained](https://sites.google.com/view/keyboards/layout/homerow-mods-explained)

Keychron:   basic HRM using VIA (Visual Input Editor for Arm)
Both ZMK and QMK support Homerow Mods (HRM).  See my short video of howto configure HRM in Via for my Keychron K11 Pro keyboard.
In the via app paste these commands into ANY (under special):

MT(MOD_LGUI,KC_A) 
MT(MOD_LALT,KC_S) 
MT(MOD_LCTL,KC_D) 
MT(MOD_LSFT,KC_F)
MT(MOD_RSFT,KC_J)
MT(MOD_RCTL,KC_K)
MT(MOD_RALT,KC_L)
MT(MOD_RGUI,KC_SCLN)

Kinesis Freestyle Edge:  Basic HRM using  FS Pro SmartSet App
Manually edit your layout1.txt file and simply add the following lines. Avoid using the Kinesis SmartSet App GUI, as it does not allow you to perform this action in the main layer.

[a]>[a][t&h250][lwin]
[s]>[s][t&h250][lalt]
[d]>[d][t&h250][lctrl]
[f]>[f][t&h250][lshft]
[j]>[j][t&h250][rshft]
[k]>[k][t&h250][lctrl]
[l]>[l][t&h250][lalt]
[colon]>[colon][t&h250][lwin]


Glove80:   Advanced HRM
This is part of TailorKey and thanks to Sanaku we have Bilateral HRM in TailorKey.
 

All other : Operating system level (e.g. your Windows laptop)
Without a mechanical keyboard (on OS level) can be done with kmonad or Kanata
Miryoku has a port for kmonad, here

Below is a config file for Kanata with support for bilateral combinations.  It's really easy to setup:
1. Goto https://github.com/jtroo/kanata/releases - scroll down and download the window executable.

2. create a config file kanata.cfg in the same directory as the executable

3. from terminal run kanata.exe     alternative:  kanata.exe --cfg c:\test2.kbd --debug

You can tune the green values based on your typing speed.  Try double them if you have issues.


EXAMPLE 1:  Simple homerow mods for kanata

(defcfg
  process-unmapped-keys yes
)
(defsrc
  a   s   d   f   j   k   l   ;
)
(defvar
  tap-time 200
  hold-time 150
)
(defalias
  a (tap-hold $tap-time $hold-time a lmet)
  s (tap-hold $tap-time $hold-time s lalt)
  d (tap-hold $tap-time $hold-time d lctl)
  f (tap-hold $tap-time $hold-time f lsft)
  j (tap-hold $tap-time $hold-time j rsft)
  k (tap-hold $tap-time $hold-time k rctl)
  l (tap-hold $tap-time $hold-time l ralt)
  ; (tap-hold $tap-time $hold-time ; rmet)
)
(deflayer base
  @a  @s  @d  @f  @j  @k  @l  @;
)

EXAMPLE 2:  Advanced homerow mods for kanata (Bilateral)

(defcfg
  process-unmapped-keys yes
)
(defsrc
  a   s   d   f   j   k   l   ;
)
(defvar
  tap-time 200
  hold-time 150

  left-hand-keys (
    q w e r t
    a s d f g
    z x c v b
  )
  right-hand-keys (
    y u i o p
    h j k l ;
    n m , . /
  )
)
(deflayer base
  @a  @s  @d  @f  @j  @k  @l  @;
)

(deflayer nomods
  a   s   d   f   j   k   l   ;
)
(deffakekeys
  to-base (layer-switch base)
)
(defalias
  tap (multi
    (layer-switch nomods)
    (on-idle-fakekey to-base tap 20)
  )

  a (tap-hold-release-keys $tap-time $hold-time (multi a @tap) lmet $left-hand-keys)
  s (tap-hold-release-keys $tap-time $hold-time (multi s @tap) lalt $left-hand-keys)
  d (tap-hold-release-keys $tap-time $hold-time (multi d @tap) lctl $left-hand-keys)
  f (tap-hold-release-keys $tap-time $hold-time (multi f @tap) lsft $left-hand-keys)
  j (tap-hold-release-keys $tap-time $hold-time (multi j @tap) rsft $right-hand-keys)
  k (tap-hold-release-keys $tap-time $hold-time (multi k @tap) rctl $right-hand-keys)
  l (tap-hold-release-keys $tap-time $hold-time (multi l @tap) ralt $right-hand-keys)
  ; (tap-hold-release-keys $tap-time $hold-time (multi ; @tap) rmet $right-hand-keys)
)

key:  homerow modifiers homerow mods home row mod kinesis freestyle pro kinesis freestyle edge keychron moergo mo-ergo glove80 glove Miryoku 

EXAMPLE 3:  Advanced homerow mods for kanata with cursor layer and tumb cluster for laptop

(defcfg
  process-unmapped-keys yes
 )


(defsrc
  grv  1    2    3    4    5    6    7    8    9    0    -    =    bspc
  tab  q    w    e    r    t    y    u    i    o    p    [    ]    \
  caps a    s    d    f    g    h    j    k    l    ;    '    ret
  lsft z    x    c    v    b    n    m    ,    .    /    rsft
  lctl lmet lalt           spc            ralt rmet rctl
)


(defvar
  tap-time 300     ;; Used for Homerow Modifiers
  hold-time 400    ;; Used for Homerow Modifiers

  left-hand-keys (
    q w e r t
    a s d f g
    z x c v b
  )
  right-hand-keys (
    y u i o p
    h j k l ;
    n m , . /
  )
)

(deflayer base
  grv  1    2    3    4    5    6    7    8    9    0    -    =    bspc
  tab  q    w    e    r    t    y    u    i    o    p    [    ]    \
  @caps @a    @s    @d    @f    g    h    @j    @k    @l    @;    '    ret
  lsft z    x    c    v    b    n    m    ,    .    /    @rsft
  lctl @lmet @lalt           spc            @ralt rmet rctl
)
 

(deflayer nomods
  grv  1    2    3    4    5    6    7    8    9    0    -    =    bspc
  tab  q    w    e    r    t    y    u    i    o    p    [    ]    \
  caps a    s    d    f    g    h    j    k    l    ;    '    ret
  lsft z    x    c    v    b    n    m    ,    .    /    rsft
  lctl lmet lalt           spc            ralt rmet rctl
)


(deflayer cursor
  @grv      1       2        3        del     ins     ins     del     8      9       0      -    =    bspc
  A-tab     @ssft   C-y      C-z      bks     C-x     C-x     bks     C-z    C-y     @ssft   [    ]    \
  caps      a       s        d        f       C-c     C-c     left    up     down    rght   '    ret
  lsft      C-f     @sword   @sline   C-a     C-v     C-v     home    pgup   pgdn    end    rsft
  lctl lmet lalt           spc            ralt rmet rctl
)


(deffakekeys
  to-base (layer-switch base)
)


(defalias
  2curs(layer-while-held cursor)               ;; Helper to cursor layer (used in for Left Alt)
  caps (tap-hold 200 200 esc caps)             ;; Caps Lock:   Tap = Escape       Hold = Caps 
  lmet (tap-hold 200 200 del lmet)             ;; Windows Key: Tap = Delete       Hold = Windows Key
  lalt (tap-hold 200 200 bks @2curs)           ;; Left Alt:    Tap = Backspace    Hold = Cursor Layer
  ralt (tap-hold 200 200 ret ralt)             ;; Right Alt:   Tap = Return       Hold = Right Alt  
  rsft (tap-dance 200 (rsft(caps-word 2000)))  ;; Right Shift: Tap = Right Shift  Double = Caps word 


  ;; ** Cursor Layer specials
  ssft (one-shot-release-pcancel 2000 lsft)    ;; Sticky shift
  sline (macro home S-(end))                   ;; Select line
  sword (macro C-(left)S-C-(rght))             ;; Select word
  ;; xline (macro S-(end))                     ;; Extend line (not in use)
  ;; xword (macro S-C-(rght))                  ;; Extend word (not in use)
  grv (macro S-i spc a m spc S-(h a p p y) spc m y S-f r S-i e S-n d spc (unicode 🙃)  )   ;; sample macro  
   
   
  tap (multi
    (layer-switch nomods)
    (on-idle-fakekey to-base tap 20)
  )

  ;; ** Homerow Modifiers
  a (tap-hold-release-keys $tap-time $hold-time (multi a @tap) lmet $left-hand-keys)
  s (tap-hold-release-keys $tap-time $hold-time (multi s @tap) lalt $left-hand-keys)
  d (tap-hold-release-keys $tap-time $hold-time (multi d @tap) lctl $left-hand-keys)
  f (tap-hold-release-keys $tap-time $hold-time (multi f @tap) lsft $left-hand-keys)
  j (tap-hold-release-keys $tap-time $hold-time (multi j @tap) rsft $right-hand-keys)
  k (tap-hold-release-keys $tap-time $hold-time (multi k @tap) rctl $right-hand-keys)
  l (tap-hold-release-keys $tap-time $hold-time (multi l @tap) ralt $right-hand-keys)
  ; (tap-hold-release-keys $tap-time $hold-time (multi ; @tap) rmet $right-hand-keys)
)


---

[A guide to home row mods](https://precondition.github.io/home-row-mods#home-row-mods-order)

