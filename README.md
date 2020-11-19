## 1.moustache 建置全新 Vue CLI 專案
  ```
  $ npm install -g @vue/cli 
  $ vue create moustache
  ```
## 2.建立 bootstrap-vue 
  - 專案目錄下輸入
    ```
    $ npm install vue bootstrap-vue bootstrap --save
    ```
  - main.js 加上
    ```
    import BootstrapVue from 'bootstrap-vue'
    import 'bootstrap/dist/css/bootstrap.css'
    import 'bootstrap-vue/dist/bootstrap-vue.css'
    Vue.use(BootstrapVue)
    ```
## 3.環境建立
  - 安裝 Vue-CLI 命令行工具
    ```
    $ npm install -g @ vue / cli
    ```
  - Pug 加入 Vue cli 專案
    ```
    $ npm i vue-cli-plugin-pug
    ```
  - SASS 加入 Vue cli 專案
    ```
    $ npm install sass-loader node-sass --save-dev
## 4.組件規劃
  ```
  header、content、footer、app_btn
  ```
## 5.底部組件化完成
  ```
  下載區域 拆出成元件app_btn
  資料傳遞串聯化
  ```