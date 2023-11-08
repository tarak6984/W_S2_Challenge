# Challenge 3: Booleanize Object

### Objective
Develop the `booleanize` function so it transforms an object's properties based on the criteria listed under Requirements. This function will loop over each property in the object and apply certain transformations to its values, while also handling edge cases related to property names.

### Function Signature
```javascript
function booleanize(obj)
```

### Parameters
- **obj:** An object with any number of properties.

### Requirements
1. Transform the number zero (`0`) into the boolean `false`.
2. Transform the number one (`1`) into the boolean `true`.
3. If a value is `null`, delete the entire key-value pair from the object.
4. If any property name exceeds 9 characters, return the string `"shorten all prop names to 9 chars or less"`.

### Maintain Original Object Structure
- Ensure that no unintended changes are made to the object's structure or other properties.

### Examples

#### Example 1
```javascript
let obj = {
  keyZero: 0,
  keyOne: 1,
  keyNull: null,
  keyTwo: 2
};

let result = booleanize(obj);
console.log(result);
```
Expected Output:
```javascript
{
  keyZero: false,
  keyOne: true,
  keyTwo: 2
}
```

#### Example 2
```javascript
let obj = {
  veryLongPropertyName: 0,
  keyOne: 1
};

let result = booleanize(obj);
console.log(result);
```
Expected Output:
```javascript
"shorten all prop names to 9 chars or less"
```
- Remember not to modify the structure or properties of the object unless specified in the requirements.