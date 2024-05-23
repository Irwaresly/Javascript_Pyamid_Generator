# Pyramid Pattern Generator

This JavaScript script generates a pyramid pattern using a specified character and number of rows. The pyramid can be either normal or inverted, depending on the `inverted` flag.

## Table of Contents

- [Description](#description)
- [Usage](#usage)
- [Example Output](#example-output)
- [Customization](#customization)
- [Contributing](#contributing)

## Description

The script generates a pyramid pattern with a specified number of rows (`count`) and a specified character (`character`). The pyramid can either be normal or inverted based on the `inverted` flag. The resulting pattern is stored in a variable called `result` and printed to the console.

## Usage

To use this script, simply copy and paste the code into a JavaScript file (e.g., `pyramid.js`) and run it using Node.js or any JavaScript runtime environment.

```javascript
const character = "!";
const count = 10;
const rows = [];
let inverted = false;

function padRow(rowNumber, rowCount) {
  return (
    " ".repeat(rowCount - rowNumber) +
    character.repeat(2 * rowNumber - 1) +
    " ".repeat(rowCount - rowNumber)
  );
}

for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    rows.push(padRow(i, count));
  }
}

let result = "";

for (const row of rows) {
  result = result + "\n" + row;
}

console.log(result);
```

## Example Output

The following is an example output of the script when `count` is set to `10`, `character` is `"!"`, and `inverted` is `false`:

```
          !
         !!!
        !!!!!
       !!!!!!!
      !!!!!!!!!
     !!!!!!!!!!!
    !!!!!!!!!!!!!
   !!!!!!!!!!!!!!!
  !!!!!!!!!!!!!!!!!
 !!!!!!!!!!!!!!!!!!!
```

If the `inverted` flag is set to `true`, the pyramid will be inverted:

```
 !!!!!!!!!!!!!!!!!!!
  !!!!!!!!!!!!!!!!!
   !!!!!!!!!!!!!!!
    !!!!!!!!!!!!!
     !!!!!!!!!!!
      !!!!!!!!!
       !!!!!!!
        !!!!!
         !!!
          !
```

## Customization

You can customize the pyramid by modifying the following variables:

- `character`: The character used to build the pyramid. Default is `"!"`.
- `count`: The number of rows in the pyramid. Default is `10`.
- `inverted`: A boolean flag that determines if the pyramid should be inverted. Default is `false`.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to create a pull request or open an issue.
