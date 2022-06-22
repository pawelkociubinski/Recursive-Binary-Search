# Recursive Binary Search

```javascript
const input = [12, 13, 14, 15, 16, 17];

function binarySearch(numbers, val, left = 0, right = numbers.length - 1) {
  const mid = Math.floor((left + right) / 2);

  if (val === numbers[mid]) {
    return mid;
  }

  if (left >= right) {
    return -1;
  }

  if (val < numbers[mid]) {
    return binarySearch(numbers, val, left, mid - 1);
  } else {
    return binarySearch(numbers, val, mid + 1, right);
  }
}

const result = binarySearch(input, 14)
console.log(result); // 2
```