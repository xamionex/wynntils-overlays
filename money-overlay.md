Always display
Change max_money if you don't like the way it's colored
It changes from white to green depending on how far you are from max_money
Change max_green if you want to have a lighter green when max_money is reached, max is 255

### Content (IDE)
```
let money_value = money;
let max_money = 500000;
let max_green = 175;
let ratio = if(greater_than(@{money_value}; @{max_money}); 1.0; divide(@{money_value}; @{max_money}));
let green = int(multiply(@{max_green}; @{ratio}));
let background_color = from_rgb(0; @{green}; 0);
let display_text = concat("Money: "; string(@{money_value}));
{to_background_text(@{display_text}; from_hex("#ffffff"); @{background_color}; "NONE"; "NONE")}
```
