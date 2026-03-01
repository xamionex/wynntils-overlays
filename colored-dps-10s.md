### Enabled Template (C&P)
```
greater_than(adavg; 0)
```
### InfoBoxContent (IDE)
```
let dps = adavg;

let maxColor = rainbow_shader;
let toptierColor = from_hex("#00ffff");
let highColor = from_hex("#00ff00");
let midtopColor = from_hex("#aaff00");
let midColor = from_hex("#ffff00");
let midbottomColor = from_hex("#ffaa00");
let lowColor = from_hex("#ff0000");
let minColor = from_hex("#555555");

let textColor = if(
    greater_than(@{dps}; 2000000);
    @{maxColor};
    if(
        greater_than(@{dps}; 1000000);
        @{toptierColor};
        if(
            greater_than(@{dps}; 500000);
            @{highColor};
            if(
                greater_than(@{dps}; 200000);
                @{midtopColor};
                if(
                    greater_than(@{dps}; 100000);
                    @{midColor};
                    if(
                        greater_than(@{dps}; 50000);
                        @{midbottomColor};
                        if(
                            greater_than(@{dps}; 25000);
                            @{lowColor};
                            @{minColor}
                        )
                    )
                )
            )
        )
    )
);

let formatted_dps = if(
    greater_than(@{dps}; 1000000);
    concat(string(round(divide(@{dps}; 1000000); 1)); "M");
    if(
        greater_than(@{dps}; 1000);
        concat(string(round(divide(@{dps}; 1000); 1)); "K");
        string(@{dps})
    )
);

{with_color(styled_text("10s:"); rainbow_shader())} {with_color(styled_text(@{formatted_dps}); @{textColor})}
```
