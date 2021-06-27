# day7

[flexible textarea hight](https://reffect.co.jp/vue/textarea_resize_vue_js)

## 学んだこと
- [Element.scrollHeight は読み取り専用のプロパティで、あふれて画面上に表示されない部分を含めた、要素の中身の幅の寸法](https://developer.mozilla.org/ja/docs/Web/API/Element/scrollHeight)
- `@Watch('tweet', { immediate: true })`で初回もwatchを走らせる
- [`Vue.$nextTick` DOM更新後にコールバックを実行する](https://jp.vuejs.org/v2/api/index.html)
## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Run your unit tests
```
yarn test:unit
```

### Run your end-to-end tests
```
yarn test:e2e
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
