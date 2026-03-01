### Enabled Template (CnP)
Displays only when holding a profession tool
```
eq_str(held_type; "GatheringToolItem")
```
### Content (IDE)
```
let green = "&a";
let dark_green = "&2";
let gold = "&6";
let aqua = "&b";

let mining_lvl = prof_lvl("mining");
let mining_pct = int(prof_pct("mining"));

let mining_material = if_str(
    less_than(@{mining_lvl}; 10); "Copper";
    if_str(
        less_than(@{mining_lvl}; 20); "Granite";
        if_str(
            less_than(@{mining_lvl}; 30); "Gold";
            if_str(
                less_than(@{mining_lvl}; 40); "Sandstone";
                if_str(
                    less_than(@{mining_lvl}; 50); "Iron";
                    if_str(
                        less_than(@{mining_lvl}; 60); "Silver";
                        if_str(
                            less_than(@{mining_lvl}; 70); "Cobalt";
                            if_str(
                                less_than(@{mining_lvl}; 80); "Kanderstone";
                                if_str(
                                    less_than(@{mining_lvl}; 90); "Diamond";
                                    if_str(
                                        less_than(@{mining_lvl}; 100); "Molten";
                                        if_str(
                                            less_than(@{mining_lvl}; 110); "Voidstone";
                                            "Dernic"
                                        )
                                    )
                                )
                            )
                        )
                    )
                )
            )
        )
    )
);

let mining_line = concat(
    @{green}; "Mining "; @{dark_green}; "[";
    @{green}; "LVL"; string(@{mining_lvl}); " ";
    @{gold}; "("; string(@{mining_pct}); "%)";
    @{dark_green}; "] ";
    @{green}; "("; @{aqua}; @{mining_material}; @{green}; ")"
);

let fishing_lvl = prof_lvl("fishing");
let fishing_pct = int(prof_pct("fishing"));

let fishing_material = if_str(
    less_than(@{fishing_lvl}; 10); "Gudgeon";
    if_str(
        less_than(@{fishing_lvl}; 20); "Trout";
        if_str(
            less_than(@{fishing_lvl}; 30); "Salmon";
            if_str(
                less_than(@{fishing_lvl}; 40); "Carp";
                if_str(
                    less_than(@{fishing_lvl}; 50); "Icefish";
                    if_str(
                        less_than(@{fishing_lvl}; 60); "Piranha";
                        if_str(
                            less_than(@{fishing_lvl}; 70); "Koi";
                            if_str(
                                less_than(@{fishing_lvl}; 80); "Gylia Fish";
                                if_str(
                                    less_than(@{fishing_lvl}; 90); "Bass";
                                    if_str(
                                        less_than(@{fishing_lvl}; 100); "Molten Eel";
                                        if_str(
                                            less_than(@{fishing_lvl}; 110); "Starfish";
                                            "Dernic Fish"
                                        )
                                    )
                                )
                            )
                        )
                    )
                )
            )
        )
    )
);

let fishing_line = concat(
    @{green}; "Fishing "; @{dark_green}; "[";
    @{green}; "LVL"; string(@{fishing_lvl}); " ";
    @{gold}; "("; string(@{fishing_pct}); "%)";
    @{dark_green}; "] ";
    @{green}; "("; @{aqua}; @{fishing_material}; @{green}; ")"
);

let wood_lvl = prof_lvl("woodcutting");
let wood_pct = int(prof_pct("woodcutting"));

let wood_material = if_str(
    less_than(@{wood_lvl}; 10); "Oak";
    if_str(
        less_than(@{wood_lvl}; 20); "Birch";
        if_str(
            less_than(@{wood_lvl}; 30); "Willow";
            if_str(
                less_than(@{wood_lvl}; 40); "Acacia";
                if_str(
                    less_than(@{wood_lvl}; 50); "Spruce";
                    if_str(
                        less_than(@{wood_lvl}; 60); "Jungle";
                        if_str(
                            less_than(@{wood_lvl}; 70); "Dark";
                            if_str(
                                less_than(@{wood_lvl}; 80); "Light";
                                if_str(
                                    less_than(@{wood_lvl}; 90); "Pine";
                                    if_str(
                                        less_than(@{wood_lvl}; 100); "Avo";
                                        if_str(
                                            less_than(@{wood_lvl}; 110); "Sky";
                                            "Dernic"
                                        )
                                    )
                                )
                            )
                        )
                    )
                )
            )
        )
    )
);

let wood_line = concat(
    @{green}; "Woodcutting "; @{dark_green}; "[";
    @{green}; "LVL"; string(@{wood_lvl}); " ";
    @{gold}; "("; string(@{wood_pct}); "%)";
    @{dark_green}; "] ";
    @{green}; "("; @{aqua}; @{wood_material}; @{green}; ")"
);

let farming_lvl = prof_lvl("farming");
let farming_pct = int(prof_pct("farming"));

let farming_material = if_str(
    less_than(@{farming_lvl}; 10); "Wheat";
    if_str(
        less_than(@{farming_lvl}; 20); "Barley";
        if_str(
            less_than(@{farming_lvl}; 30); "Oat";
            if_str(
                less_than(@{farming_lvl}; 40); "Malt";
                if_str(
                    less_than(@{farming_lvl}; 50); "Hops";
                    if_str(
                        less_than(@{farming_lvl}; 60); "Rye";
                        if_str(
                            less_than(@{farming_lvl}; 70); "Millet";
                            if_str(
                                less_than(@{farming_lvl}; 80); "Decay Roots";
                                if_str(
                                    less_than(@{farming_lvl}; 90); "Rice";
                                    if_str(
                                        less_than(@{farming_lvl}; 100); "Sorghum";
                                        if_str(
                                            less_than(@{farming_lvl}; 110); "Hemp";
                                            "Dernic Seed"
                                        )
                                    )
                                )
                            )
                        )
                    )
                )
            )
        )
    )
);

let farming_line = concat(
    @{green}; "Farming "; @{dark_green}; "[";
    @{green}; "LVL"; string(@{farming_lvl}); " ";
    @{gold}; "("; string(@{farming_pct}); "%)";
    @{dark_green}; "] ";
    @{green}; "("; @{aqua}; @{farming_material}; @{green}; ")"
);

{@{mining_line}}\n
{@{fishing_line}}\n
{@{wood_line}}\n
{@{farming_line}}
```
