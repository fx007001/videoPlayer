# 调整dplayer的源码 然后在vue2中使用dplayer 
- 下载dplayer源码 https://github.com/DIYgod/DPlayer
- 安装依赖后直接运行该项目代码 
 - 主要目录文件 
 - template 中主要包含有两个文件 
    - video.art 为播放器的模板
    - player.art 为播放器的控制栏模板文件 - 主要修改这部分内容
    - 在js文件中 主要是player.js 定义DPlayer类 其余文件负责实现功能的
      - template.js 定义操作dom对象、需要添加或修改控制按钮 是修改这个文件 -主要也是修改播放器控制按钮栏
      - options.js 初始化配置项文件
      - i18n.js 国际化 修改一些文案的时候可以在这里调整
      - setting.js 定义了设置按钮中的几个操作方法
      - events 定义播放器的事件
     - css 使用 scss编写 文件结构也比较清晰
# 在vue2中使用dplayer 
- 使用npm i dplayer 安装dplayer播放器 - 安装之后会发现 在node_modules中打开dplayer文件夹 使用的是dplayer的打包文件 
- 可以直接拷贝 dist 目录中的js文件到自己的组件库中使用 - 如果你想要修改dplayer的话
- 使用this.db 调用dplayer提供的所有事件
- 你也可以直接使用vue-dplayer  如果你想要修改dplayer的话 建议可以直接将dplayer导入到自己的项目中使用 而不是安装vue-dplayer

## Project setup

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

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
