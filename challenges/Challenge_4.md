     // 🧠 scrub takes a string "text" as its first argument, and an array of forbidden words "forbidden" as its second
      // Any word in the text included in the array of forbidden words is replaced with a word of equal length but made of lowcase "x"
      // The scrubbed text is then returned from the function, as seen in the examples below
      // No punctuation is used in the text
      // 🧠 Examples of usage:
      //    scrub("out of the silent planet", ["of", "silent"]) // returns "out xx the xxxxxx planet"
      //    scrub("the ghost of the navigator", ["the"]) // returns "xxx ghost of xxx navigator"
      //    scrub("lost somewhere in time", []) // returns "lost somewhere in time"
      //    scrub("aces high", ["high", "aces", "hearts"]) // returns "xxxx xxxx"
      //    scrub("", ["high", "aces""]) // returns ""
      // 🌟 HINT: useful array methods to use are `push`, `indexOf`, `split`, `join`
      if (!text.length || !forbidden.length) return text
      const words = text.split(' ')
      const result = []
      for (let idx = 0; idx < words.length; idx++) {
        const word = words[idx]
        let idxForbidden = forbidden.indexOf(word)
        if (idxForbidden > -1) {
          let sub = ''
          for (let char in forbidden[idxForbidden]) {
            sub += 'x'
          }
          result.push(sub)
        } else {
          result.push(word)
        }
      }
      return result.join(' ')