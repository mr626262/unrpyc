init -2 python:
    room = Room("clothesshop", hours=(1,23))
    room.display_name = "Zava"
    room.buy = [
        Gift("sexy underwear", money_cost = 0, label = "underwear", desire_bonus = 50, relationship_bonus = 50),
        Gift("sexy dress", money_cost = 0, label = "clothes", desire_bonus = 50, relationship_bonus = 50),
        Gift("cute top", money_cost = 0, label = "clothes", desire_bonus = 50, relationship_bonus = 50),
        Gift("nice scarf", money_cost = 0, label = "clothes", desire_bonus = 50, relationship_bonus = 50),
        Gift("sexy swimsuit", money_cost = 0, label = "swimsuit", desire_bonus = 50, relationship_bonus = 50),
        Gift("cute swimsuit", money_cost = 0, label = "swimsuit", desire_bonus = 50, relationship_bonus = 50),
        Gift("purse", money_cost = 0, label = "purse", desire_bonus = 50, relationship_bonus = 50),
        Gift("fancy purse", money_cost = 0, label = "purse", desire_bonus = 50, relationship_bonus = 50),
        Gift("shoes", money_cost = 0, label = "shoes", desire_bonus = 50, relationship_bonus = 50),
        Gift("fancy shoes", money_cost = 0, label = "shoes", desire_bonus = 50, relationship_bonus = 50),
        ]
    room.exits = ["mall"]
    ROOMS[room.name] = room

    shop = Activity(
        "shop",
        duration = 0,
        display_name = "shop",
        action = renpy.call_in_new_context,
        action_params = ["clothesshop_shop"]
        )
    room.activities.append(shop)

label clothesshop_shop:
    python:
        result = game.select(["Women clothes","Men clothes"])
        if result == "Women clothes":
            game.shop(ROOMS["clothesshop"].buy)
        else:
            shop = [
                Equip("fancy suit", money_cost = 0, traits_effects = {"pacifist":1,"princess":1}),
                Equip("leather jacket", money_cost = 0, traits_effects = {"submissive":1,"rebel":1}),
                Equip("tweed blazer", money_cost = 0, traits_effects = {"bookworm":1,"family":1}),
                Equip("sweat pants", money_cost = 0, traits_effects = {"sportsy":1, "dominant":1}),
                Equip("funny shirt", money_cost = 0, traits_effects = {"geek":1,"playful":1}),
                Equip("military fatigues", money_cost = 0, traits_effects = {"submissive":1,"gourmand":1}),
                ]
            game.shop(shop)
    return
