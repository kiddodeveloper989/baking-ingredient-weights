# Baking ingredient weights (cups to grams)

An open dataset of **160 common baking ingredients** with their weight per US cup, tablespoon and teaspoon.
Useful for recipe apps, nutrition tools, meal planners, and converting volume recipes to grams.

Maintained by [BakeMath](https://bakemath.web.app), free baking calculators. Every ingredient has a converter page with full tables, for example [all-purpose flour](https://bakemath.web.app/cups-to-grams/all-purpose-flour/).

## Files
- `ingredients.json`: array of objects
- `ingredients.csv`: the same data as CSV

Fields: `slug`, `name`, `category`, `grams_per_us_cup`, `grams_per_tbsp`, `grams_per_tsp`, `url`

## Sample
| Ingredient | g / cup | g / tbsp | g / tsp |
|---|---|---|---|
| All-purpose flour | 120 | 7.5 | 2.5 |
| Bread flour | 120 | 7.5 | 2.5 |
| Whole wheat flour | 113 | 7.1 | 2.4 |
| Cake flour | 114 | 7.1 | 2.4 |
| Self-rising flour | 113 | 7.1 | 2.4 |
| 00 flour (pizza flour) | 116 | 7.3 | 2.4 |
| Rye flour | 106 | 6.6 | 2.2 |
| Spelt flour | 102 | 6.4 | 2.1 |

## Method
Weights are averages for one US cup (236.6 mL) of ingredient spooned into the cup and leveled (brown sugar packed; liquids filled to the line). Real weights vary with brand, humidity and technique. For exact baking, weigh your ingredients.

## Use it
```js
const data = await fetch('https://raw.githubusercontent.com/kiddodeveloper989/baking-ingredient-weights/main/ingredients.json').then((r) => r.json());
const flour = data.find((i) => i.slug === 'all-purpose-flour');
console.log(flour.grams_per_us_cup); // 120
```

## License
Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit "BakeMath (bakemath.web.app)" with a link.

Want a ready-made converter instead? Embed the free [cups to grams calculator](https://bakemath.web.app/cups-to-grams/) on your site (the embed code is on the page).
