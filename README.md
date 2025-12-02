let x2 = 0
player.onItemInteracted(FISHING_ROD, function () {
    if (x2 == 0) {
        mobs.applyEffect(FIRE_RESISTANCE, mobs.target(NEAREST_PLAYER), 100, 1)
        x2 = 1
    } else {
        blocks.fill(
        TNT,
        pos(-10, 102, -10),
        pos(10, 102, 10),
        FillOperation.Replace
        )
        blocks.fill(
        REDSTONE_BLOCK,
        pos(-10, 101, -10),
        pos(10, 101, 10),
        FillOperation.Replace
        )
        blocks.fill(
        TNT,
        pos(-10, 97, -10),
        pos(10, 96, 10),
        FillOperation.Replace
        )
        loops.pause(1)
        blocks.fill(
        AIR,
        pos(-10, 101, -10),
        pos(10, 101, 10),
        FillOperation.Replace
        )
        x2 = 0
    }
})
