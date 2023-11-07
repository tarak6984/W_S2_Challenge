      // 🧠 booleanize takes an object as its single argument, which can have any number of properties
      // Loop over the properties and then return the object, after applying the following transformations:
      //    * If a value is the number zero, it must be transformed into the Boolean false
      //    * If a value is the number one, it must be transformed into the Boolean true
      //    * If a value is null, the whole key-value pair must be deleted from the object
      // 🧠 Edge cases:
      //    * If a property name exceeds 9 characters, return the string "shorten all prop names to 9 chars or less"
      // 🌟 HINT: careful not to perform any unintended changes on the object
      for (let key in obj) {
        if (key.length > 9) {
          return "shorten all prop names to 9 chars or less"
        }
        if (obj[key] === null) {
          delete obj[key]
        }
        if (obj[key] === 0) {
          obj[key] = false
        } else if (obj[key] === 1) {
          obj[key] = true
        }
      }
      return obj