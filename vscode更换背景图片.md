## vscode更换背景图片

### 下载插件

- vscode搜索插件*background*  

  如图

![](C:\Users\xiaoxiaoweii\Desktop\front_end_tool_use\images\vscode更换背景图片-1.png)

### 安装使用

- 修改代码文件地址:设置--拓展--在settings.json  中编辑

- 添加代码

  ```json
  //*******************************************background
      "background.enabled": true,  //是否启用背景
      "background.useDefault": false,  //是否使用默认图片
      "background.customImages": [    //路径数组，可以是多张图，不同窗口不同背景图
          "file:///D:/VScodeBg/c7aff5ee371dbce9.jpg",
      ],
      "background.style": {  
          "content": "''", // 背景图文字
          "pointer-events": "none", //禁止任何触发事件
          "position": "absolute", // 绝对定位
          "z-index": "9999", // 优先级设置
          "width": "100%", // 与父级同宽
          "height": "100%", // 与父级同高
          "background-position": "center", //居中
          "background-repeat": "no-repeat", // 不重复
          "background-size": "cover", // 覆盖
          "opacity": 0.1 // 透明度
      }
      //*******************************************background   
  ```

### 修改效果

- 单个窗口

  ![](C:\Users\xiaoxiaoweii\Desktop\front_end_tool_use\images\vscode更换背景图片-2.png)

- 两窗口

![](C:\Users\xiaoxiaoweii\Desktop\front_end_tool_use\images\vscode更换背景图片-3.png)

