# vue-wxlogin

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

```
## Install
``` bash
npm install vue-wxlogin --save-dev
```

``` bash
import wxlogin from 'vue-wxlogin';
Vue.component('my-component', {
    components: {
        wxlogin
    }
});
```

## Usage
  
``` html
<wxlogin></wxlogin>
```
  
## Available props

| Event         |Type           | Default    | Description                                         |
|---------------|---------------|------------|-----------------------------------------------------|
| appid         |String         |            | 应用唯一标识，在微信开放平台提交应用审核通过后获得  |
| scope         |String         |            | 应用授权作用域，拥有多个作用域用逗号（,）分隔，网页应用目前仅填写snsapi_login即可 |
| redirect_uri  |String         |            | 重定向地址，需要进行UrlEncode                        |
| state         |String         |            | 用于保持请求和回调的状态，授权请求后原样带回给第三方。该参数可用于防止csrf攻击（跨站请求伪造攻击），建议第三方带上该参数，可设置为简单的随机数加session进行校验                                            |
| theme         |String         |            | 提供"black"、"white"可选，默认为黑色文字描述。      |
| href          |String         |            | 自定义样式链接，第三方可根据实际需求覆盖默认样式。  |

``` html
<wxlogin :appid="appid" :scope="scope" :redirect_uri="redirect_uri"></wxlogin>
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
