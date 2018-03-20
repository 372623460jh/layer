# layer弹出层组件

该组件是用于移动端弹出层操作，该组件的基础样式基于自动视口组件

## 地址链接

- 源码所在位置：https://github.com/372623460jh/layer/tree/master/dist

- dev链接：http://libs.ijianghe.cn/js/layer/layer.js

- pro链接：http://libs.ijianghe.cn/js/layer/layer.min.js

- css链接：http://libs.ijianghe.cn/js/layer/layer.css

- demo：https://github.com/372623460jh/layer/blob/master/examples/test/test.html
    
## 用法
   
- 提示框
    
    ```javascript
    layer.open({
        content: 'hello layer',
        skin: 'msg',
        time: 2 //2秒后自动关闭
    });
    ```
- 询问框
    
    ```javascript
    layer.open({
        content: '您确定要刷新一下本页面吗？',
        btn: ['确定', '取消'],
        yes: function (index) {
            layer.close(index);
        },
        no: function () {
            console.log('取消');
        }
    });
    ```
- 底部对话框
    
    ```javascript
    layer.open({
        content: '这是一个底部弹出的询问提示',
        btn: ['删除', '取消'],
        skin: 'footer',
        yes: function (index) {
            layer.open({content: '执行删除操作'})
        },
        no: function () {
            console.log('取消');
        }
    });
    ```
- 底部提示
    
    ```javascript
    layer.open({
        content: '一个没有任何按钮的底部提示',
        skin: 'footer'
    });
    ```
- 自定义标题风格
    
    ```javascript
    layer.open({
        title: [
            '我是标题',
            'background-color: #FF4351; color:#fff;'
        ],
        content: '标题风格任你定义。'
    });
    ```
- 页面层
    
    ```javascript
    layer.open({
        type: 1,
        content: '可传入任何内容，支持html。一般用于手机页面中',
        anim: 'up',
        style: 'position:fixed; bottom:0; left:0; width: 100%; height: 200px; padding:10px 0; border:none;'
    });
    ```
- loading层
    
    ```javascript
    layer.open({type: 2});
    ```
- loading带文字
    
    ```javascript
    layer.open({
        type: 2,
        content: '加载中'
    });
    ```