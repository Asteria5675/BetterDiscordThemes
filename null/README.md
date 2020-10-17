This is called a `readme.md` for a reason.

# Intro
Null a discord theme originally created by <a href="https://github.com/Modder4869/BdBrokenStuff/tree/master/Themes/v1">Modder </a>. The original version used `calc` and css variables based around HSL.
Hue based of a color wheel, Saturation for a shade gray (0%) to the full color(100%) from hue, and Lightness is the amount of light the color has 0% for black, 100% for white.
This theme is a rewite of the original to provide the user with a lot of more variables to change the difference in colours or to keep a monotone of a particular color.
A [guide](https://github.com/Asteria5675/BetterDiscordThemes/blob/master/null/README.md/#Visual-Guides) on editing the variables of null.

## Versions
Currently 2 main versions will be supported:
  1. `Null` which will include imports of addons, users may remove the addon imports if desired, which will most likely receive more updates and changes in the furture. 
  This version will preset as dark gray and accent colors. <a href="https://betterdiscord.net/ghdl?id=3407">null download</a>
  2. `Null Clear` a presetup transparent version of null, original file will not include addon imports. However, the theme will preset like `Null` with coloured channels, tooltips, etc. <a href="https://betterdiscord.net/ghdl?id=3408">null clear download</a>
  <br> </br>
  3. `Dark Null` will be setup to mimic the original Discord feel so no accent colours on tooltips, channels, blurple elements, mentions/channels, etc. <a href="https://betterdiscord.net/ghdl?id=3409">dark null download</a>
  <br> </br>
The third version is to appeal to lack of a "just a darker version of Discord nothing else". This version obviously could be made easily from changing things from the first file; however, it'll be ideal to remove the demand of just a dark discord even with a detailed readme.

Note: I'm aware of the idea of themes and the idea of using imports and changing variables and calling them 'themes'. Null is one theme, with different versions already preset to avoid the thousands of simple questions being asked.

### Previews
## Null
![Null](https://github.com/Asteria5675/BetterDiscordThemes/blob/master/SourceCodes/src/Screenshot_296.png)
## Edited
![Edited Dark](https://i.imgur.com/SBK3mea.png)
<img src="https://i.imgur.com/RqK7TRu.png" height="300px" width="300px"/>
<p>These 3 presets I did not save the changed variables/values. Only to showcase that the user can achieve same outcomes if editing the theme file in such manner. </p>

## Dark Null
![Dark Null](https://i.imgur.com/Q1TW7vn.png)

### Main Variables
Main Variables - variables in theme file
```css
  --hue: 217 ;
  --saturation: 0% ;
  --lightness: 15% ;
  --alpha: 1 ;
```
`--hue` is the hue, `--saturation` is saturation(%), `--lightness` is the amount of light(%)
  Hue values are based off a degree of the color wheel so 0 is red, 120 is green, 240 is blue (Note: RGB and Hex can be converted in to hsl)
  Saturation is the shade of gray so 0% is gray while 100% is the full color
  Lightness is the light of the color 0% is black while 100% is white
  
  Saturation should remain under a value of 40% to avoid any visual problems especially lightness being under 20%.
  `--alpha` is the alpha/opacity of the color, only change the value as decimal (ex. 0.25) if you desire a change of transparency

If you desire a brighter colour and or brighter image when using transparency then its adivsed you copy all of `.theme-dark` and the variables (EXCEPT `--text-normal` and `--text-muted`) and paste it at the bottom of the file and rename `.theme-dark` to `.theme-light`. If you do not understand this part then you are better off with another theme

## Addition Variables
these variables are the addition / multiplication to mimic the style of the colour palette of discord original dark theme.
`--hue-addition` is initially set at `0` changing this value will change the hue/color on certain elements, `--saturation-addition` alters certain elements' saturation, `--lightness-addition`  alters certain elements' lightness, `--alpha-addition` used to addon certain element opacity only if altering null for a transparent theme. `--multiplier` is also tied to these variables in certain area if you want to remove the multiplier then set its value to `1`

addition variables can also be a negative intergers (ex `--saturation-addition: -6%;`) to give a darker contrast.

## Accents
accents, tooltips, mentions, etc.
`--accent` is the accent colout that applies to many regions such as pings, notification dots, blurple elements( discord blue). Users may revert the changes back as in file provide defaults to revert all are variables; however, it may be better to alter Dark Null if you desire the least changes of accents.

`--tooltip-background`,  `--blurple`,`--is-mention`, `--is-mention-bg`, `--unread`, and `--guild-selected` all use the variable `--accent` 

```css
--channel-selected: linear-gradient(6deg, var(--channel-gradient-prim),  var(--channel-gradient-sec),  var(--channel-gradient-tri));
```
was setup as background image gradient user may delete the whole gradient and replace it if they desire back to the normal channel modifier ex: 
```css
--channel-selected: var(--background-modifier-selected);
```

## Addons
only pretains to `Null`; however, imports can be added to any themes not just null versions. (Important Note: adding these imports to other themes may not work properly)
Note: imports are placed above all other css in a file

imports are theses: 
```css
@import url('https://asteria5675.github.io/addons/Bigger_Chat_Avatars.css');
```
This addon makes avatars in chat bigger`--avatar-size` and also can make them square`--avatar-roundness: 0;` as well
```css
@import url('https://asteria5675.github.io/addons/null_addons.css');
```
This addon changes a popouts and context menu to more a block design, nothing dramatic. Expect this import addon to be added onto.

Both addon imports may be deleted from null if desired. Note: if you using these imports check the css to understand the variables if wanting to adjust certain css.

Full popout users import
```css
 @import url('https://asteria5675.github.io/addons/full_popout_avatars.css');
```

### Visual Guides
Changing imports
<img src="https://i.imgur.com/QgZbnFA.gif" />

Watch the below linked videos for basic editing of variables

Turning Null into a transparent theme and basic variable changing <a href="https://i.imgur.com/9a7ZnkY.mp4">imgur video </a> (file exceeded length limit so it does not embed on github)
another editing <a href="https://i.imgur.com/fISldFJ.mp4">shorter example</a>

Final Result - image will fit to window size
<img src="https://i.imgur.com/t25BzEy.png" />

Also note, null clear can also be used to for a translucent discord. Enable Transparency in BD settings and leave the `url()` blank. Blur will not apply to other windows when doing this.
## Final Notes
please read this readme to fully understand the countless possibilities of altering this theme.

Reason why I revived and rewrote null was because it one of the few really early basic dark mode theme that hardly changed the discord feel. However, the original got outdated quick and never got the spotlight for the unique concept of the theme.

<a href="https://discord.gg/QRxZPvc" > Support Server </a> here. 
Note: I make these themes on my free time DO NOT demand simple changes done for you. Use this readme and read it as well understand it. 

Speaking of making these themes for free if you really wanted to donate to me so I can live off another energy drink or two, then request the donate link enough on my server and I might make one who knows. I prefer not to advertise such though :)

## Readme
once again, it's called a `readme` for a reason. Start <a href="https://github.com/Asteria5675/BetterDiscordThemes/blob/master/null/README.md/#Intro">here</a> to understand how to change this theme to your desired background color/image. This readme is was created for all possible questions so read it or the theme file also containg examples/explanations. If you cannot understand anything from here, then you are better off with another theme.
