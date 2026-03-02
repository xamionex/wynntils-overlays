Always displays
Change max_speed if you don't like the way it's colored
It changes from white to cyan depending on how far you are from max_speed

### Content (IDE)
```
let speed = bps;
let max_speed = 20;
let ratio = if(greater_than(@{speed}; @{max_speed}); 1.0; divide(@{speed}; @{max_speed}));
let red = int(multiply(255; subtract(1.0; @{ratio})));
let background_color = from_rgb(@{red}; 255; 255);
let display_text = concat("Speed: "; string(round(@{speed}; 1)); " bps");
{to_background_text(@{display_text}; from_hex("#000000"); @{background_color}; "NONE"; "NONE")}
```
