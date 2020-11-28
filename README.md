# eBook

```css
npm install -g @vue/cli
```

# 创建一个项目

## 1.命令

- 运行以下命令来创建一个新项目：

  ```
  vue create hello-world
  ```

  可以选默认的包含了基本的 Babel + ESLint 设置的 preset，也可以选“手动选择特性”来选取需要的特性。

  ![CLI 预览](https://cli.vuejs.org/cli-new-project.png)

  手动设置则提供了更多的选项，它们是面向生产的项目更加需要的。

  ![CLI 预览](https://cli.vuejs.org/cli-select-features.png)

- 

  ```
  //使用uniapp模板创建项目
  vue create -p dcloudio/uni-preset-vue my-project
  ```

  ### 使用cli创建项目和使用HBuilderX可视化界面创建项目有什么区别

  - 编译器的区别
    - cli创建的项目，编译器安装在项目下。并且不会跟随HBuilderX升级。如需升级编译器，执行n**pm update**。
    - HBuilderX可视化界面创建的项目，编译器在HBuilderX的安装目录下的plugin目录，随着HBuilderX的升级会自动升级编译器。
    - 已经使用cli创建的项目，如果想继续在HBuilderX里使用，可以把工程拖到HBuilderX中。注意如果是把整个项目拖入HBuilderX，则编译时走的是项目下的编译器。如果是把src目录拖入到HBuilderX中，则走的是HBuilderX安装目录下plugin目录下的编译器。
    - cli版如果想安装less、scss、ts等编译器，需自己手动npm安装。在HBuilderX的插件管理界面安装无效，那个只作用于HBuilderX创建的项目。
  - 开发工具的区别
    - cli创建的项目，内置了d.ts，同其他常规npm库一样，可在vscode、webstorm等支持d.ts的开发工具里正常开发并有语法提示。
    - 使用HBuilderX创建的项目不带d.ts，HBuilderX内置了uni-app语法提示库。如需把HBuilderX创建的项目在其他编辑器打开并且补充d.ts，可以在项目下先执行 npm init，然后npm i @types/uni-app -D，来补充d.ts。
    - 但vscode等其他开发工具，在vue或uni-app领域，开发效率比不过HBuilderX。详见：https://ask.dcloud.net.cn/article/35451
    - 发布App时，仍然需要使用HBuilderX。其他开发工具无法发布App，但可以发布H5、各种小程序。如需开发App，可以先在HBuilderX里运行起来，然后在其他编辑器里修改保存代码，代码修改后会自动同步到手机基座。
    - 如果使用cli创建项目，那下载HBuilderX时只需下载10M的标准版即可。因为编译器已经安装到项目下了。

## 2.使用图形化界面

```bash
vue ui
```