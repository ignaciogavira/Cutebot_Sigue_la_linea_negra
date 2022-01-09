# Cutebot_Sigue_la_linea_negra
Codigo para cutebot con micro:bit, sigue la línea

basic.showLeds(`
    # # . # #
    # # . # #
    . . . . .
    # . . . #
    . # # # .
    `)
basic.forever(function () {
    if (cuteBot.tracking(cuteBot.TrackingState.L_line_R_unline)) {
        cuteBot.moveTime(cuteBot.Direction.left, 100, 0.01)
    }
    if (cuteBot.tracking(cuteBot.TrackingState.L_unline_R_line)) {
        cuteBot.moveTime(cuteBot.Direction.right, 100, 0.01)
    }
    if (cuteBot.tracking(cuteBot.TrackingState.L_R_line)) {
        cuteBot.moveTime(cuteBot.Direction.forward, 100, 0.01)
    }
})
