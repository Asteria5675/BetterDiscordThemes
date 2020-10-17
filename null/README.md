Null - placeholder

# Intro
Null a discord theme originally created by Modder. The original version used `calc` and css variables based around HSL.
Hue based of a color wheel, Saturation for a shade gray (0%) to the full color(100%) from hue, and Lightness is the amount of light the color has 0% for black, 100% for white.
This theme is a rewite of the original to provide the user with a lot of more variables to change the difference in colours or to keep a monotone of a particular color.
A [guide]() on editing the variables of null.

## Versions
Currently 2 main versions will be supported:
  1. `Null` which will include imports of addons, users may remove the addon imports if desired, which will most likely receive more updates and changes in the furture.
  This version will preset as dark gray with dark navy blue background color.
  2. `Null Clear` a presetup transparent version of null, original file will not include addon imports. However, the theme will preset like `Null` with coloured channels, tooltips, etc.
  3. `Dark Null` will be setup to mimic the original Discord feel so no accent colours on tooltips, channels, blurple elements, mentions/channels, etc.
The third version is to appeal to lack of a "just a darker version of Discord nothing else". This version obviously could be made easily from changing things from the first file; however, it'll be ideal to remove the demand of just a dark discord even with a detailed readme.

Note: I'm aware of the idea of themes and the idea of using imports and changing variables and calling them 'themes'. Null is one theme, with different versions already preset so thousands of questions are not being asked.

## Previews
![Null](https://github.com/Asteria5675/BetterDiscordThemes/blob/master/SourceCodes/src/Screenshot_296.png)
!![Edited Dark](https://i.imgur.com/SBK3mea.png)
<img src="https://i.imgur.com/RqK7TRu.png" height="300px" width="300px"/>
## Main Variables
Main Variables - variables in theme file
```
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
`--accent` is the accent colout that applies to many regions such as pings, notification dots, blurple elements( discord blue). Users may revert the changes back as in file provide defaults to revert all are variables; however, it may be better to alter Dark Null if you deire the least changes of accents.

`--tooltip-background`,  `--blurple`,`--is-mention`, `--is-mention-bg`, `--unread`, and `--guild-selected` all use the variable `--accent` 

```
--channel-selected: linear-gradient(6deg, var(--channel-gradient-prim),  var(--channel-gradient-sec),  var(--channel-gradient-tri));
```
was setup as background image gradient user may delete the whole gradient and replace it if they desire back to the normal channel modifier ex: 
```
--channel-selected: var(--background-modifier-selected);
```

## Addons
