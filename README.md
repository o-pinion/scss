# Scss Variables
More infos and example in [our wiki](https://github.com/o-pinion/scss/wiki)

[![npm version](https://img.shields.io/npm/v/@o-pinion/scss.svg)](https://www.npmjs.com/package/@o-pinion/scss)
![NPM](https://img.shields.io/npm/l/@o-pinion/scss)
![npm](https://img.shields.io/npm/dm/@o-pinion/scss)


## Quick start

In the working repository

```
npm i @o-pinion/scss@latest
```

Then import in the following order in you main.scss style and where you need it

```scss
@import '@o-pinion/scss/mixin';
@import '@o-pinion/scss/utilities';
```

You can import specific mixins like follow
```scss
@use '@o-pinion/scss/mixins/shadow' as shadow;
@use '@o-pinion/scss/mixins/grid' as grid;
@use '@o-pinion/scss/mixins/browser' as browser;
// ...
@include shadow.box-shadow(1);
```

**Note**
- `@o-pinion/scss/mixin` have to be imported in every scss file that needs they mixins
- `@o-pinion/scss/utilities` should be imported **only once**. If not, it's gonna create useless classes
- mixin and utilities work good together but you could only use one of the both if you need it

## Css Variable
### Radius
```scss
:root {
  --radius-smallest: 4px; // Extra small : Menu, Snackbars, Text fields
  --radius-smaller: 8px; // Small : Chips, Rich tooltip
  --radius-small: 10px; // Medium : Cards, Small FABs
  --radius: 16px; // Large : FABs, Navigation drawers
  --radius-big: 20px;
  --radius-bigger: 28px; // Extra large : Dialogs, Large FABs, Search view (full-screen), Time picker, Time input
  --radius-rounded: 50px;
  --radius-circle: 100%; // @TODO remove in favor of --full
  --radius-full: 100%; // Full : Badge, Buttons, Sliders, Switches, Search bards
}
```

### Spacing

Source: https://uxdesign.cc/ui-cheat-sheet-spacing-friendships-e37a6fccc407  
```scss
:root {
  --space-smallest: 4px; // BBFE
  --space-smaller: 8px; // Best friends
  --space-small: 12px;
  --space: 16px; // Close friends
  --space-big: 24px; // Close-ish friends
  --space-bigger: 32px; // Friends
  --space-biggest: 64px; // Acquaintances
  --space-giant: 72px; // Distant acquaintances
  --space-gargantuan: 128px; // Stranger
}
```

### Width
Similar as bootstrap 

```scss
:root {
  @media (min-width: 576px) and (max-width: 768px) {
    --container-max-width: 540px;
  }
  @media (min-width: 768px) and (max-width: 992px) {
    --container-max-width: 720px;
  }
  @media (min-width: 992px) and (max-width: 1200px) {
    --container-max-width: 960px;
  }
  @media (min-width: 1200px) {
    --container-max-width: 1140px;
  }
}
```

### Z-index
```css
:root {
  --z-index-highest: 1000;
  --z-index-higher: 100;
  --z-index-high: 10;
  --z-index-normal: 1;
}
```

## Mixins
### Grid
```scss
@include sm, md, lg, xl , xxl { };
@include smUp, mdUp, ... {};
@include smOnly, mdOnly, ... {};
@include sm-md, sm-lg, ... {}

// Where
$sm: 576px !default;
$md: 768px !default;
$lg: 992px !default;
$xl: 1200px !default;
$xxl: 1500px !default;

@mixin sm {
  @media (max-width: #{$md - 1px}) {
    @content;
  }
}
```

## Authors

- **Raphaël Balet** - _Initial work_ - [Megaphone](https://megaphone.info)

[![BuyMeACoffee](https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png)](https://www.buymeacoffee.com/widness)

## License  
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details
