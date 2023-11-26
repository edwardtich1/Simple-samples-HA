# Mushroom-Cards-simple-samples
Оформление карты и иконки

```yaml
    card_mod:
      style:
        mushroom-shape-icon$: |
          ...
        .: |
          ha-card {
          ...
          }  
```
С фоном иконки:

<image src="https://community-assets.home-assistant.io/original/4X/3/f/6/3f6832419fffb35cb247a5077344f869567c814f.jpeg">

```yaml
card_mod:
  style: |
    ha-card {
      width: fit-content;
    }
```
Без фона иконки:

<image src="https://community-assets.home-assistant.io/original/4X/e/7/4/e7427bad3ac543510bd0a6e9ef41d83d4dfec2de.jpeg">

```yaml
card_mod:
  style: |
    ha-card {
      width: fit-content;
    }
    mushroom-shape-icon {
      --shape-color: none !important;
    }
```
Без фона карты:

<image src="https://community-assets.home-assistant.io/original/4X/9/9/0/9906fb11295099beadce3a1b73af3ab7e9154075.jpeg">

```yaml
card_mod:
  style: |
    ha-card {
      width: fit-content;
      background: none;
      border: none !important;
      box-shadow: none !important;
    }
```
Нет фона карты или фона иконки:

<image src="https://community-assets.home-assistant.io/original/4X/6/7/c/67ca662fc57639888dbdd68fa4bbc8e3e5978b5d.jpeg">

```yaml
card_mod:
  style: |
    mushroom-shape-icon {
      --shape-color: none !important;
    }
    ha-card {
      width: fit-content;
      background: none;
      border: none !important;
      box-shadow: none !important;
    }
```
И последнее: без фона карточки, фона фигуры или фона значка:

<image src="https://community-assets.home-assistant.io/original/4X/3/7/4/374dd9fb63ea2c50dc11d3fcd27b8c66741f7028.jpeg">

```yaml
card_mod:
  style: |
    mushroom-shape-icon {
      --shape-color: none !important;
    }
    ha-card {
      width: fit-content;
      background: none;
      border: none !important;
      box-shadow: none !important;
    }
    mushroom-badge-icon {
      --main-color: none !important;
    }
```
