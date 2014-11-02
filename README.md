# jquery.shoppingcart

Simple shopping cart jQuery plugin using local storage.

## Installation

Include script *after* the jQuery library (unless you are packaging scripts somehow else):

```html
<script src="/path/to/jquery.shoppingcart.js"></script>
```

## Browser requirements

![ScreenShot](https://bytebucket.org/vov1/jquery.shoppingcart/raw/5876a7a86acc2d0e3239c274c4505973eae5198b/browsersupport.png?token=e9f7108e74828b3c17e16a10e3f12db299664551)

## Usage

Add item:

```javascript
$.shoppingcart('add',{
				'id': 123,
				'image': 'path/to/image.png',
				'name': 'ProductName',
				'code': 'Product123',
				'url': 'catalog/clothes/product/123',
				'attributes': ['S', 'Black'],
				'price': 30,
				'count': 1
			});
```

**Only *id* & *price* are required!**

Edit item:
```javascript
$.shoppingcart('edit',{
				'id': 123,
				'image': 'path/to/newImage.png',
				'name': 'ProductNewName',
				'code': 'ProductNew123',
				'url': 'catalog/clothes/product/123',
				'attributes': ['M', 'White'],
				'price': 60,
				'count': 2
			});
```

**Only *id* is required!**

Remove item:
```javascript
$.shoppingcart('remove', {'id': 123});
```

Clear cart:
```javascript
$.shoppingcart('clear');
```

Get items count:
```javascript
// Returns integer
$.shoppingcart('getCount');
```

Get total cart price:
```javascript
// Returns float
$.shoppingcart('getPrice');
```

Get item by id:
```javascript
// Returns object { 'id', 'image', 'name', 'code', 'url', 'attributes', 'price', 'count' }
$.shoppingcart('getById', id);
```

Get all cart items:
```javascript
// Returns ARRAY of object { 'id', 'image', 'name', 'code', 'url', 'attributes', 'price', 'count' }
$.shoppingcart('getAll');
```

## Authors

[Volodymyr Stelmakh (vov1)](https://bitbucket.org/vov1)