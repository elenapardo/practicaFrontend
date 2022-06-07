# Javascript exercises

To solve this exercise you can use [codepen](https://codepen.io/) or [codesandbox](https://codesandbox.io/) to execute JS code and then you have to include it in a repository.

## Exercise 1. Objects

Based on the input object we want to access to an specific property called `credit-card`. What should we add in the console.log statement?

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

const solution = input.billing.paymentMethod

// add your solution in the console.log
console.log(solution)
```

## Exercise 2. map

Based on the input object we want to have only the orders without the price info and with the locale at the end of the productId.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

input.orders.map((order) => {
  order.productld +='-'+
order.storeLocale;
  delete order.price
  delete order.storeLocale;
  return order;
});



const expected = [{
  productId: 'product-1-nl',
},
{
  productId: 'product-2-es',
},
{
  productId: 'product-3-en',
}]
```

## Exercise 3. filter

Based on the input object we want to have the same object but only the orders with a price greater than 10.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

let res = input.orders.filter((item) => item.price > 10);
console.log(res);

input.orders = res;


console.log(input);


const expected = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};
```

## Exercise 4. map & filter

Based on the input object we want to have the name of the order productIds
 with a price greater than 10, and separated by commas.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

let result = '';
const productsGreaterThanTen = input.orders.filter((order) => {
	return order.price > 10;
})
.map((product) => {
	result += product.productId + ', ';
  return product;
});

result = result.substring(0, result.length - 2);

console.log(result);

result = result.substring(0, result.lenght - 2);
console.log(result);


const expected = 'product-1, product-2';
```

## Exercise 5. reduce

Based on the input object we want the total price of the orders, 
and include them in the object.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

input.totalPrice = input.orders.reduce((a, b) => {
	return a.price + b.price;
});

console.log(input);

const expected = {
  totalPrice: 39,
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};
```

