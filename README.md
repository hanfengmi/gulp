# gulp Learning
### gulp
    gulp 是前端开发过程中对代码进行自动化构建的利器,可以对资源进行优化，通过配置自动完成复杂的任务，提高工作效率
### node
gulp基于node.js实现    

1.全局安装gulp   

    `npm install gulp -g`

2.目录结构    

    └── src/            源码目录    
        ├── build/   .html 组件    
        ├── sass/     .scss .sass 文件   
        ├── css/       .css 文件
        ├── js/         .js 文件
        └── img/     图片
    └── dist/        输出目录
    └── package.json
    └── gulpfile.js
3.gulpfile.js与package.json是必须的。

    package.json可以在根目录文件使用 npm init 配置，也可以手动创建。
    对于别人的开源项目，可以使用 npm install 即可安装package.json文件中声明的所有插件模块
4.根目录添加gulp

    nnpm install gulp --save-dev

5.项目文件安装常用插件

    npm install gulp del gulp-cached gulp-uglify gulp-rename gulp-concat gulp-notify gulp-filter gulp-jshint gulp-ruby-sass gulp-rev-append gulp-cssnano gulp-replace gulp-imagemin browser-sync gulp-font-spider gulp-file-include gulp-autoprefixer --save-dev    



    var gulp = require('gulp'), // 必须先引入gulp插件
        del = require('del'),  // 文件删除
        sass = require('gulp-ruby-sass'), // sass 编译
        cached = require('gulp-cached'), // 缓存当前任务中的文件，只让已修改的文件通过管道
        uglify = require('gulp-uglify'), // js 压缩
        rename = require('gulp-rename'), // 重命名
        concat = require('gulp-concat'), // 合并文件
        notify = require('gulp-notify'), // 相当于 console.log()
        filter = require('gulp-filter'), // 过滤筛选指定文件
        jshint = require('gulp-jshint'), // js 语法校验
        rev = require('gulp-rev-append'), // 插入文件指纹（MD5）
        cssnano = require('gulp-cssnano'), // CSS 压缩
        imagemin = require('gulp-imagemin'), // 图片优化
        browserSync = require('browser-sync'), // 保存自动刷新
        fileinclude = require('gulp-file-include'), // 可以 include html 文件
        autoprefixer = require('gulp-autoprefixer'); // 添加 CSS 浏览器前缀

6.gulp API

[点这里](http://www.gulpjs.com.cn/docs/api/)

7.使用gulp

    gulp taskname



转自[原文](http://www.sheyilin.com/2016/02/gulp_introduce/)
