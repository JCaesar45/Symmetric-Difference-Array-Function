```markdown
# Symmetric Difference Array Function (`diffArray`)

## Description
`diffArray` is a JavaScript function that takes two arrays and returns a new array containing items that are **only in one** of the input arrays, not in both. This is known as the *symmetric difference*.

## Purpose
This function helps identify elements that are unique to each array by comparing their contents and filtering out the common items.

## Usage
Call the `diffArray` function with two arrays as arguments:

```javascript
const result = diffArray(array1, array2);
``

### Parameters
- `array1` (Array): The first array to compare.
- `array2` (Array): The second array to compare.

### Returns
- A new array containing the symmetric difference of the two input arrays.

## Example

```javascript
const arrayA = ["diamond", "stick", "apple"];
const arrayB = ["stick", "emerald", "bread"];

const result = diffArray(arrayA, arrayB);
console.log(result); 
// Output: ["diamond", "apple", "emerald", "bread"]
``

## Implementation

```javascript
function diffArray(arr1, arr2) {
  const uniqueInArr1 = arr1.filter(item => !arr2.includes(item));
  const uniqueInArr2 = arr2.filter(item => !arr1.includes(item));
  return [...uniqueInArr1, ...uniqueInArr2];
}
``

## Notes
- The function uses the `filter` method to filter out common items.
- The returned array contains only items found in exactly one of the input arrays.
- If both arrays are identical, the function returns an empty array.

## License
This code is provided as-is for educational purposes.
