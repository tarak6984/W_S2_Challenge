      // 🧠 normalizePhoneNumber takes a string as its only argument, representing a ten-digit number
      // The function returns a string formatted as seen below
      // 🧠 Examples of usage:
      // normalizePhoneNumber("9876543210") // returns "(987) 654-3210"
      // normalizePhoneNumber("1111111111") // returns "(111) 111-1111"
      // 🧠 Edge cases:
      //   * If the argument is of an incorrect length, return the string "type a 10-digit number"
      //   * If the argument is of the correct length but any character is not an integer between 0 and 9, return "invalid phone number"
      // 🌟 HINT: instead of looping over the number's digits, loop backwards over a template "(XXX) XXX-XXXX"
      // 🌟 HINT: at each iteration, if the current character is an "X", replace it with the result of popping a digit from the number
      // 🌟 HINT: if you'd rather loop forwards, use `shift` instead of `pop`
      if (num.length !== 10) return "type a 10-digit number"
      const template = '(XXX) XXX-XXXX'.split('')
      const digits = num.split('')
      let invalidDigit = false
      for (let idx = template.length - 1; idx >= 0; idx--) {
        if (template[idx] === 'X') {
          const digit = digits.pop()
          if (
            digit !== '0' &&
            digit !== '1' &&
            digit !== '2' &&
            digit !== '3' &&
            digit !== '4' &&
            digit !== '5' &&
            digit !== '6' &&
            digit !== '7' &&
            digit !== '8' &&
            digit !== '9'
          ) {
            return "invalid phone number"
          }
          template[idx] = digit
        }
      }
      return template.join('')