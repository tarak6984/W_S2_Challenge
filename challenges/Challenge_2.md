// 🧠 mineSweeper takes a grid as its first argument, and coordinates x and y as the second and third args
//  The grid is an array of arrays in the following format: [["🟥","🟦","🟥"],["🟦","🟥","🟥"],["🟥","🟦","🟦"]]
//  Each subarray is a row of the grid, the first subarray being the top row:
//  [
//    ["🟥", "🟦", "🟥"],
//    ["🟦", "🟥", "🟥"],
//    ["🟥", "🟦", "🟦"]
//  ]
//  The coordinates x and y are numbers: either 1 or 2 or 3
//    * An x = 1 and y = 1 means the top-left square
//    * An x = 3 and y = 1 means the top-right square
//    * An x = 3 and y = 3 means the bottom-right square
//  Red squares are mines and blue squares are safe
//    * If mineSweeper is called with such coordinates that the player lands on red, return the string "🟥 💀"
//    * If the player lands on blue, return the string "🟦 🥳"
// 🧠 Edge cases:
//    * If the x or y coordinates are under 1 or over 3, return the string "invalid coordinates"