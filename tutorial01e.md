### @activities true

```template
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
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)

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
```
# Kodekraft: Code an energy game
## introduction
### introduction @unplugged

Make your own game where you gather energy and score points. How many points can you score before the time runs out?

### Step 1
Here's a little premade code to use as a starting point. Look at the code and test the game. 
```blocks
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
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)

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
```


### Step 2
Make your player character appear in a random spot. In the ``||Scene:Scene||`` menu, find ``||Scene:place mySprite on top of random...||``. Place this in ``||loops:on start||``, underneath ``||Variables:Set mySprite to...||``. Click the grey square and choose the sand coloured tile from the menu that pops up. 

```blocks
tiles.setTilemap(tilemap`level1`)
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
// @highlight
tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
let energy = sprites.create(img`
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

 ```

### Step 3
Make the energy sprite (Lightning) appear in a random spot too. Find a ``||scene:place mySprite on top of random...||`` block and place it underneath the ``||variables:set energy to...||``. Here you'll have to change mysprite to energy and remember to choose a tile. 

```blocks
tiles.setTilemap(tilemap`level1`)
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
tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
let energy = sprites.create(img`
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
// @highlight
tiles.placeOnRandomTile(energy, sprites.castle.tilePath5)

```

### Step 4
We need more energy sprites. Use a ``||loops:repeat||`` loop from the ``||loops:loops||``  menu to repeat the two lower blocks in ``||loops:on start||`` about 100 times.
Tip: You can move individual blocks by pressing and holding Ctrl while you drag them.

```blocks
let energy: Sprite = null
tiles.setTilemap(tilemap`level1`)
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
tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
controller.moveSprite(mySprite)
scene.cameraFollowSprite(mySprite)
// @highlight
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
    tiles.placeOnRandomTile(energy, sprites.castle.tilePath5)
}

```


### Step 5

When the player catches a lightning, we want it to disappear. In the ``||Sprites:Sprites||`` menu you'll find ``||Sprites:on sprite of kind player overlaps...||``. Place it anywhere on the screen. Change it so ``||variables:otherSprite||`` is of the kind ``||Sprites:food||``

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
})

```

### Step 6
Inside the block you just created, first place a ``||Sprites:destroy mySprite||`` block. 
Click on the variable ``||variables:otherSprite||`` and drag it to the oval area that says ``||variables:mySprite||``.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    // @highlight
    otherSprite.destroy()
})
```

### Step 7

We need to keep track of your score. In the ``||Info:Info||`` menu you'll find ``||Info:change score by..||``. Place this block in the ``||Sprites:overlap||`` block. Test the game to check if your score increases when you capture energy.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    // @highlight
    info.changeScoreBy(1)
})
```

## Countdown

### Step 8

The final touch is a countdown clock. At the bottom of the ``||Loops:on start||`` block, place a ``||Info:start countdown||`` block. It's up to you to decide how much time you'll have to gather points.

```blocks
let energy: Sprite = null
tiles.setTilemap(tilemap`level1`)
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
tiles.placeOnRandomTile(mySprite, sprites.castle.tilePath5)
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
    tiles.placeOnRandomTile(energy, sprites.castle.tilePath5)
}
// @highlight
info.startCountdown(10)

```
### Step 9
Finished! Play the game and see how many points you can score. 

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>


