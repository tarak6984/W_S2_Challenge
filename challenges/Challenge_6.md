     // 🧠 diceRolls takes no arguments and returns a number
      // The function throws a six-sided dice until 3 sixes in a row are obtained
      // The number of throws it took to obtain that third-in-a-row six is then returned from the function
      // 🌟 HINT: research using `Math.random` to obtain a number from 1 to 6
      // 🌟 HINT: use `while(true)` to throw the dice indefinitely, but avoid an infinite loop by making sure to break out eventually
      // 🌟 HINT: you need to keep track of the total number of throws, as well as how many sixes in a row
      let throws = 0
      let counter = 0
      while (true) {
        throws++
        const num = Math.floor(Math.random() * 6) + 1
        if (num === 6) counter++
        else counter = 0
        if (counter === 3) {
          return throws
        }
      }