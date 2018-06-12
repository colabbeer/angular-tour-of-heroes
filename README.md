# AngularTourOfHeroes

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.8.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## tips
- src/styles.css 文件存放一些全局的样式
- angular cli新指令：ng generate component xxx 可以创建名为xxx的组件 
  运行后会创建一个新文件夹src/app/xxx 并生成了XxxComponent的三个文件
- 双向绑定语法[(ngModel)] 需要在@NgModule装饰器上添加FormsModule模块
- mock-heroes 模拟从服务器端获取的数据
- *ngFor 循环输出(let .. of ..) 复写器指令repeater
- (click) ()监听事件
- *ngIf 判断指令 如果为false 整段dom移除（不存在了）若为true 添加这段dom
- css类绑定机制 [class.some-css-class]="some-condition" 添加到要施加样式的元素上
