# ES6 modules

ES6 modules enhance JavaScript by allowing developers to modularize code, breaking it into manageable pieces that can be imported and reused across different parts of an application.

This simplifies code maintenance and debugging while also minimizing issues related to global variables and functions. 

### Exporting values

JavaScript because of its multi-paradigm nature allows us to export functions, objects, classes and primitive values using the keyword export. 

### Named exports

Any function, class or variable exported using the named export can only be imported using the same name. 

Multiple functions and variables can be exported and imported using named export.

Example:products.mjs file:
```js
// Module products.mjs
let numberSale=0;
let totalSale=0;

// Export keyword can be specified individually
// with functions and variables.
export function buy(buyer, item)
{
    buyer.total=buyer.total+item.price;
}
export function sell(item)
{
    totalSale=totalSale+item.price;
    numberSale=numberSale+1;
    item.quantity=item.quantity-1;
    return 0;
}

// Export keyword can also be used
// with multiple values.
export { totalSale, numberSale};
```
index.mjs file:
```js
import {total sale, numberSale, buy, sell } from './product.mjs';
let buyer={
    name:"GeeksforGeeks",
    total:0
};
let item={
    name="butter",
    price:10,
    quantity:100
};
console.log("Total Sale till now = ",totalSale);
buy(buyer, item);
sell(item);
console.log("Total expense of buyer = ",buyer.total);
console.log("Quantity of item left = ",item.quantity);
console.log("Total Sale till now = ",totalSale);
```

### Default exports

Anything exported as a default can be imported using any name. 

A maximum of 1 value can be exported using the default export. 

To export multiple values, one can combine them in an object and then use default export to export this object. 
```js
// Module secret_ingredient.mjs
let secretIngredient="Salsa";
export default secretIngredient;
```

### Importing values

Only the values exported from a module can be imported using the import keyword. 

### Examples
- Importing the named exports

`import { buy, sell} from './modules/products.mjs';`

- Importing the named exports using aliases:

`import { buy as buyCustomer, sell as sellCustomer} from './modules/products.mjs';`

- Importing the default export

`import productSecret from './modules/secret_ingredient.mjs';`

- Importing all the exports and creating a new object

`import * as productModule from './modules/products.mjs';`

- Importing default as well as named exports

`import defaultVal,* from './modules/hybrid.mjs';`

### Modules in browsers

Modules can be included in the browser JavaScript by setting the type attribute for the script tag as module. 

The modules loaded from an external source using src attribute are deferred by default i.e. they are loaded in parallel with HTML. 

Each module is executed only the first time when it is loaded.

<script type=”module” src=”product.mjs”></script>

JavaScript also allows dynamic loading of modules using the construct import().