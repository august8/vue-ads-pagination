# vue-ads-pagination

Vue ads pagination is a vue js pagination component. 
On the left side you find some information about the shown items.
On the right side you can select a specific, the first, last, next or previous page.

It uses the handy
[tailwind](https://tailwindcss.com/docs/what-is-tailwind/) css library for styling.

## Demo

![Demo](https://media.giphy.com/media/1AfMQogZf9Y5ci8ck3/giphy.gif)

I've written a demo in [JSFiddle](https://jsfiddle.net/arnedesmedt/18n9k6vm)

## Installation

You can install the package via npm or yarn.

#### NPM

```npm install vue-ads-pagination --save```

#### YARN

```yarn add vue-ads-pagination```

## Usage

You can add the vue-ads-pagination component by using the following code in your project.

```vue
<template>
  <div id="app">
    <vue-ads-pagination
        :page="3"
        :itemsPerPage="10"
        :maxVisiblePages="4"
        :totalItems="200"
        @page-change="pageChange"
    />
  </div>
</template>

<script>
import VueAdsPagination from 'vue-ads-pagination';

export default {
    name: 'app',
    components: {
        VueAdsPagination,
    },

    methods: {
        pageChange (page, range) {
            console.log(page, range);
        },
    },
};
</script>
```

### Properties

- `page`: *(type: number, default: 0)* A zero-based number to set the page.
- `itemsPerPage`: *(type: number, default: 10)* The max amount of items on one page.
- `maxVisiblePages`: *(type: number, default: 5)* The number of pages to be visible if their are too many pages.
- `totalItems`: *(type: number, required)* The total amount of items.

### Events

- `page-change`: Emitted on creation, to know the initial state, and if another page is clicked. It contains the following parameters:
    - `page`: *(type: number)* The zero-based current page.
    - `range`: *(type: object)* Object with the following parameters:
        - `start`: *(type: number)* A zero-based number to identify the first item.
        - `end`: *(type: number)* A zero-based number to identify the last item.
        
## Testing

We use the jest framework for testing this pagination component. Run the following command to test it:

```
npm run test:unit
```

## Changelog

Read the [CHANGELOG](CHANGELOG.md) file to check what has changed.

## Issues

If you have any issues (bugs, features, ...) on the current project, add them [here](https://gitlab.com/arnedesmedt/vue-ads-pagination/issues/new).

## Contributing

Do you like to contribute to this project? Please, read the [CONTRIBUTING](CONTRIBUTING.md) file.

## Social

[1]: http://www.twitter.com/arnesmedt
[1.1]: http://i.imgur.com/wWzX9uB.png (@ArneSmedt)
 - Follow me on [![alt text][1.1]][1]
 
## Donate

Want to make a donation? 
That would be highly appreciated!

Make a donation via [PayPal](https://www.paypal.me/arnedesmedt).
