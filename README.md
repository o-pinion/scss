# Scss Variables

More infos and example in [our wiki](https://github.com/rbalet/scss-opinionated/wiki)

## Quick start

In the working repository

```
npm i scss-opinionated@latest
```

Then import in the following order in you main.scss style and where you need it

```scss
@import 'scss-opinionated/mixin';
@import 'scss-opinionated/utilities';
```

You can import specific mixins like follow
```scss
@use 'scss-opinionated/mixins/shadow' as shadow;
@use 'scss-opinionated/mixins/grid' as grid;
@use 'scss-opinionated/mixins/browser' as browser;
// ...
@include shadow.box-shadow(1);
```

**Note**
- `scss-opinionated/mixin` have to be imported in every scss file that needs they mixins
- `scss-opinionated/utilities` should be imported **only once**. If not, it's gonna create useless classes
- mixin and utilities work good together but you could only use one of the both if you need it

## Css Variable
### Border
```scss
:root {
  --border-smallest: 4px; // Extra small : Menu, Snackbars, Text fields
  --border-smaller: 8px; // Small : Chips, Rich tooltip
  --border-small: 10px; // Medium : Cards, Small FABs
  --border: 16px; // Large : FABs, Navigation drawers
  --border-big: 20px;
  --border-bigger: 28px; // Extra large : Dialogs, Large FABs, Search view (full-screen), Time picker, Time input
  --border-rounded: 50px;
  --border-circle: 100%; // @TODO remove in favor of --full
  --border-full: 100%; // Full : Badge, Buttons, Sliders, Switches, Search bards
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

```css
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

## Authors

- **Raphaël Balet** - _Initial work_ - [Megaphone](https://megaphone.info)

[![BuyMeACoffee](https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png)](https://www.buymeacoffee.com/widness)

## License  
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
