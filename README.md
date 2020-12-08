## 1.HBD 建置全新 Vue CLI 專案
  ```
  $ npm install -g @vue/cli 
  $ vue create HBD
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
    ```
  - JSON-SERVER 加入 Vue cli 專案(建立免費 json server運行指令)
    ```
    $ npm install -g json-server

    運行

    json-server --watch db.json ( cmd下指令 )

    ```
  - 設定 WORKSPACE SETTINGS  
    ```
    檔案 --> 喜好設定 --> 設定 --> 
    搜尋 live server config --> 
    ignore files setting --> 
    加上 "data.josn" 在底層  
    用意 畫面更新使用
    ```
## 4.基本組件規劃
  ```
  header、content、footer
  ```
## 5.底部組件化完成
  ```
  下載區域 拆出成元件app_btn
  資料傳遞串聯化
  ```
## 6.釐清 mounted , methods 用法含意
  - axios RESTful API 串接導入方法
    ```
    使用 v-on:click="事件名稱" 技術
    ```
  - axios.get  
    ```
    axios.get(url).then((res) =>
      console.log(res)
    )
    ```
  - axios.post
    ```
    if(!this.input) return false ( input去頭尾空白****重要 )
    axios.post(url,{
      送出資料: this.(v-model 事件綁定)
    }).then((res)=>{
      this.(v-model.trim 事件綁定) = '' //更新 輸入 .trim = 去頭尾空白
      this.contentes.push(res.data) //放入 data 資料
    })
    ```
  - axios.delete (刪除需要加編號id)   
    ```
    let target = this contents(index)
    v-on:click="事件名稱(XXX.id)"
    axios.delete(url/${id}).then((res)=>{
      this.contents.splice(index, 1)
    })
    ```
## 6.新增 header 組件以及按鈕 btn 組件設定
  ```
  元件佈署 [ 
    1.header 拆寫為兩區塊元件 { 按鈕 Button 元件、Logo 元件 }
    2.按鈕規劃為 vue router 官方的路由管理切換分頁
    3.資料串聯可能使用prop vuex 或是 $emit 方式實作
  ]
  ```
  - 開設 header_btn 資料夾存放
    ```
    _header_btn、_header_logo
    ```
## 7. content 組件內規劃
  - 預計新增 輪播、搜尋、飯店公告.........( 未定數 2020/12/08 ) 
