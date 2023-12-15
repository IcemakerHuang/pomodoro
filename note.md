安裝：
npm create vuetify@latest

```js
√ Project name: ... pomodoro
√ Which preset would you like to install? » Custom (Choose your features)
√ Use TypeScript? ... No
√ Use Vue Router? ... Yes
√ Use Pinia? ... Yes
√ Use ESLint? ... Yes
√ Would you like to install dependencies with yarn, npm, pnpm, or bun? » npm
```

npm i -D @vue/eslint-config-standard

.eslintrc.js 新增
```js
  extends: [
    'plugin:vue/vue3-essential',
    'eslint:recommended',
    '@vue/standard' // 新增
  ],
```

砍掉 components layout 資料夾
src\router\index.js ->新增path 和 物件 -> src\views 新增對應乾淨 .vue

src\router\index.js 新增fn
```js
router.afterEach((to, from) => {
  document.title = to.meta.title
})
```


回App.vue 新增 navbar (Vuetify)、新增icon (mdi-icon)

到個別.vue 修增功能