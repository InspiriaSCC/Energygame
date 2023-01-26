### @activities true

```template

namespace SpriteKind {
    export const Renewable = SpriteKind.create()
}

namespace myTiles {
    //% blockIdentity=images._tile
    export const tile0 = img`
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
        . . . . . . . . . . . . . . . .
    `
}

info.onCountdownEnd(function () {
    if (info.score() < 20) {
        game.over(false)
    } else {
        game.over(true)
    }
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Renewable, function (sprite, otherSprite) {
    tiles.placeOnRandomTile(otherSprite, assets.tile`transparency16`)
    info.changeScoreBy(1)
})
let offshoreWind: Sprite = null
let energy: Sprite = null
tiles.setTilemap(tiles.createTilemap(
            hex`3200320000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010101010101010101000000000000000000000000000000000000000000000000000000000000000000000000000000000001010101010101010101010100000000000000000000000000000000000000000000000000000000000000000000000000000101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000010101010101010101010101010101010101010101010000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010101000000000000000000000000000000000000000000000000000000000001010101010101010101010101010101010101010100000000000000000000000000000000000000000000000000000000000101010101010101010101010101010101010101000000020202020202020000000000000000000000000000000000000000000101010101010101010101010101010101010100000202020202020202020202020000000000000000000000000000000000000101010101010101010101010101010101000202020202020202020202020202020000000000000000000000000000000000000001010101010101010101010101010202020202020202020202020202020202000000000000000000000000000000000000000000000000000001010101010102020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000000020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000020202020202020202020202020202020202020202020202020200000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000002020202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020202000000000000000000000000000000000000000000000000000000000202020202020202020202020202020202020202020000000000000000000000000000000000000000000000000000000000000002020202020202020202020202020202020000000000000000000000000000000000000000000000000000000000000000000000000202020202020202020202000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`,
            img`
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
                . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
            `,
            [myTiles.tile0,sprites.castle.tilePath5,sprites.castle.tileGrass1],
            TileScale.Sixteen
        ))

scene.setBackgroundColor(9)
let mySprite = sprites.create(img`
    . f f f . f f f f . f f f . 
    f f f f f c c c c f f f f f 
    f f f f b c c c c b f f f f 
    f f f c 3 c c c c 3 c f f f 
    . f 3 3 c c c c c c 3 3 f . 
    . f c c c c 4 4 c c c c f . 
    . f f c c 4 4 4 4 c c f f . 
    . f f f b f 4 4 f b f f f . 
    . f f 4 1 f d d f 1 4 f f . 
    . . f f d d d d d d f f . . 
    . . e f e 4 4 4 4 e f e . . 
    . e 4 f b 3 3 3 3 b f 4 e . 
    . 4 d f 3 3 3 3 3 3 c d 4 . 
    . 4 4 f 6 6 6 6 6 6 f 4 4 . 
    . . . . f f f f f f . . . . 
    . . . . f f . . f f . . . . 
    `, SpriteKind.Player)
if (Math.percentChance(20)) {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
} else {
    tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
}
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
for (let index = 0; index < 100; index++) {
    energy = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . f f f f . . . . . 
        . . . . . . f f 5 5 f . . . . . 
        . . . . . . f 5 5 f f . . . . . 
        . . . . . f f 5 f f . . . . . . 
        . . . . f f 5 5 f f f . . . . . 
        . . . . f 5 5 5 5 5 f . . . . . 
        . . . . f f f f 5 5 f . . . . . 
        . . . . . . f 5 5 f f . . . . . 
        . . . . . f f 5 f f . . . . . . 
        . . . . . f 5 f f . . . . . . . 
        . . . . . f f f . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Food)
    if (Math.percentChance(80)) {
        tiles.placeOnRandomTile(energy, sprites.castle.tilePath5)
    } else {
        tiles.placeOnRandomTile(energy, sprites.castle.tileGrass1)
    }
}
for (let index = 0; index < 200; index++) {
    offshoreWind = sprites.create(img`
        . . . . . . . . . . 8 8 . . . . 
        . . . . . . . . . . 1 8 8 . . . 
        . . . . . . . 8 8 8 . 1 8 8 . . 
        . . . . . . . 8 1 8 8 . 1 8 . . 
        . . . . . . . 1 . 1 8 . . 8 . . 
        . . . . . . . . 8 8 8 . . 8 . . 
        . 8 8 8 8 8 8 8 1 1 1 . 8 8 . . 
        . 1 1 1 1 1 1 1 . . . 8 8 1 . . 
        . . 8 8 8 8 8 8 8 8 8 1 1 . . . 
        . . 1 1 1 1 1 1 1 1 1 . . . . . 
        . 8 8 8 8 8 8 8 8 8 8 . . . . . 
        . 1 1 1 1 1 1 1 1 1 1 8 8 . . . 
        . . 8 8 8 8 8 8 8 8 . 1 8 8 . . 
        . . 1 1 1 1 1 1 1 8 . . 1 8 . . 
        . . . . . . . . 8 8 . . . 8 . . 
        . . . . . . . . 1 1 . 8 8 1 . . 
        `, SpriteKind.Renewable)
    tiles.placeOnRandomTile(offshoreWind, assets.tile`transparency16`)
}
info.startCountdown(10)

```
# Environmental impact - save the planet
## Introduction
### Introduction @unplugged
How do different energy sources affect the environment? Here's a suggestion for how to make the game about saving the planet.

### Step 1
Let's start by adding a fossil fuel source, like coal. Find a ``||loops:repeat 4 times||`` block from the ``||loops:Loops||``-menu and place it in your main code, underneath the other ``||loops:repeat||`` blocks. Write 100 where i says 4 to make 100 instances of coal on the map.
```block
for (let index = 0; index < 100; index++) {
	
}
```
### Step 2
Get a ``||variables:set mySprite2 to||`` block from the ``||sprites:Sprites||`` menu. Create a new variable called ``||variables:coal||`` by clicking where it says ``||variables:mySprite2||`` and choose ``||variables:create new||``. Add a new variable kind called ``||sprites:Fossil||`` in a similar way by clicking where it says ``||sprites:Player||``. Click the gray square and draw a piece of coal.
```block
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
let coal: Sprite = null
for (let index = 0; index < 100; index++) {
    // @highlight
    coal = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f . . . . . . . 
        . . . f f f f f f f . . . . . . 
        . . . f f f f f f f f f . . . . 
        . f f f f f f f 8 f f f . . . . 
        f f f f f f f f 1 8 f f . . . . 
        f f f f f f f f f 1 f f f . . . 
        f f f f f f f f f f f f f . . . 
        . f f f f f f f f f f f f . . . 
        . . . . f f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . . . f f f . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Fossil)
}
```
### Step 3
Get a ``||logic:if then else||`` block from the ``||logic:Logic||`` menu and place it inside the ``||loops:Repeat||`` block you just got.
```block
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
let coal: Sprite = null
for (let index = 0; index < 100; index++) {
    coal = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f . . . . . . . 
        . . . f f f f f f f . . . . . . 
        . . . f f f f f f f f f . . . . 
        . f f f f f f f 8 f f f . . . . 
        f f f f f f f f 1 8 f f . . . . 
        f f f f f f f f f 1 f f f . . . 
        f f f f f f f f f f f f f . . . 
        . f f f f f f f f f f f f . . . 
        . . . . f f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . . . f f f . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Fossil)
    // @highlight
    if (true) {
    	
    } else {
    	
    }
}
```
### Step 4
Find a small ``||math:0 % chance||`` block from the ``||math:Math||`` menu and place it where it says ``||logic:true||`` in the last block you fetched. Type in 80 where it says 0.
```block
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
let coal: Sprite = null
for (let index = 0; index < 100; index++) {
    coal = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f . . . . . . . 
        . . . f f f f f f f . . . . . . 
        . . . f f f f f f f f f . . . . 
        . f f f f f f f 8 f f f . . . . 
        f f f f f f f f 1 8 f f . . . . 
        f f f f f f f f f 1 f f f . . . 
        f f f f f f f f f f f f f . . . 
        . f f f f f f f f f f f f . . . 
        . . . . f f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . . . f f f . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Fossil)
    // @highlight
    if (Math.percentChance(80)) {
    	
    } else {
    	
    }
}
```
### Step 5
Fetch a ``||scene:place mySprite on random||`` block from the ``||scene:Scene||`` menu. Change ``||variables:mySprite2||`` to ``||variables:coal||``, click the gray square and choose the green tile.
```block
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
let coall: Sprite = null
for (let index = 0; index < 100; index++) {
    coal = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f . . . . . . . 
        . . . f f f f f f f . . . . . . 
        . . . f f f f f f f f f . . . . 
        . f f f f f f f 8 f f f . . . . 
        f f f f f f f f 1 8 f f . . . . 
        f f f f f f f f f 1 f f f . . . 
        f f f f f f f f f f f f f . . . 
        . f f f f f f f f f f f f . . . 
        . . . . f f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . . . f f f . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Fossil)
    if (Math.percentChance(80)) {
        // @highlight
        tiles.placeOnRandomTile(coal, sprites.castle.tileGrass1)
    } else {
    	
    }
}
```
### Step 6
Find another ``||scene:place mySprite on random||`` block in the ``||scene:Scene||`` menu. Change ``||variables:mySprite2||`` to ``||variables:coal||``, click the gray square and choose the sand coloured tile. You've now distributed the coal resources between the two islands. If you want to, you can add more fossil fuel sources by repeating the procedure in step 1-6.
```block
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
let kcoal: Sprite = null
for (let index = 0; index < 100; index++) {
    coal = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . f f f . . . . . . . 
        . . . f f f f f f f . . . . . . 
        . . . f f f f f f f f f . . . . 
        . f f f f f f f 8 f f f . . . . 
        f f f f f f f f 1 8 f f . . . . 
        f f f f f f f f f 1 f f f . . . 
        f f f f f f f f f f f f f . . . 
        . f f f f f f f f f f f f . . . 
        . . . . f f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . f f f f f f f . . . . 
        . . . . . . . f f f . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Fossil)
    if (Math.percentChance(80)) {
        tiles.placeOnRandomTile(kcoal, sprites.castle.tileGrass1)
    } else {
        // @highlight
        tiles.placeOnRandomTile(coal, sprites.castle.tilePath5)
    }
}
```

### Step 7
We'll let the planet itself be player 2 and give it some life that will be reduced if we gather certain types of energy. Get a ``||info:set player2 life to 3||`` block from the ``||info:Info||`` menu and place it inside your main ``||loops:on start||`` loop, right at the very bottom underneath the rest of your main code.

```block
info.player2.setLife(3)
```

### Step 8
Grab a ``||info:change player2 life by -1||`` block from the ``||info:Info||`` menu and place it inside the ``||sprites:on sprite of kind player overlaps otherSprite of kind Food||`` block that controls what happens when you pick up the lightnings. The lightnings represent fossil fuels and have a negative impact on the planet's life.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
    // @highlight
    info.player2.changeLifeBy(-1)
```

### Step 9
In your own game, you can repeat step 2 for any ``||sprites:on sprite of kind player overlaps otherSprite of kind [EnergyKind]||`` block that represents fuels that are harmful to the environment. Renewable energy sources can be left as they are, since they have a neutral or at least much smaller negative impact on the environment.

```blocks
namespace SpriteKind {
    export const Fossil = SpriteKind.create()
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Fossil, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
    // @highlight
    info.player2.changeLifeBy(-1)
})
```

### Step 10
What happens when the planet runs out of life? Well, it probably goes without saying, but you'll have to use a ``||info:on player 2 life zero||`` block from the ``||info:Info||`` menu to make something happen. You can put sounds from the ``||music:Music||`` menu in there, animate the screen with blocks from the ``||scene:Scene||`` menu, or maybe just place a ``||game:game over||`` block from ``||game:Game||`` menu in there? (Warning: The ``||game:game over||`` block will stop any other blocks inside the ``||info:on life zero||``  from taking effect.)

```blocks
info.player2.onLifeZero(function () {
	
})
```
```ghost
music.baDing.play()
scene.cameraShake(4, 500)
effects.confetti.startScreenEffect()
game.over(false)
```
### Step 11
That's it for the environmental impact of energy sources.
Here's an extra challenge:
Maybe some actions have a positive impact on the environment? You could introduce rare items that increase the health of the planet if you remove them. Plastic in the ocean, for instance. Which blocks would you use to add these to your game? It's up to you!

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

