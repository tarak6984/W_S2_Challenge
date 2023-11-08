# Challenge 5: Normalize Phone Number

### Objective
Create the `normalizePhoneNumber` function that takes a string representing a ten-digit number and returns it formatted in a specific phone number format.

### Function Signature
```javascript
function normalizePhoneNumber(num)
```

### Parameters
- **num:** A string representing a ten-digit phone number.

### Requirements
1. Format the input string `num` into the phone number format: "(XXX) XXX-XXXX".
2. If the input `num` is not exactly ten digits long, return the string "type a 10-digit number".
3. If the input `num` contains any characters that are not integers between 0 and 9, return "invalid phone number".

### Examples

#### Example 1
```javascript
let result = normalizePhoneNumber("9876543210");
console.log(result);
```
Expected Output:
```javascript
"(987) 654-3210"
```

#### Example 2
```javascript
let result = normalizePhoneNumber("1111111111");
console.log(result);
```
Expected Output:
```javascript
"(111) 111-1111"
```

### Edge Cases
- Ensure that the function accurately checks for the length of the input string and validates each character.

### Hints
- Consider using a template "(XXX) XXX-XXXX" and loop backwards, replacing 'X' with digits from the input number.
- To iterate forward, use `shift` instead of `pop` when processing the digits.