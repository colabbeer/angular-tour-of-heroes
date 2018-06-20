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
- angular cli新指令：`ng generate component xxx` 可以创建名为xxx的组件 
  运行后会创建一个新文件夹src/app/xxx 并生成了XxxComponent的三个文件
- 双向绑定语法 `[(ngModel)]` 需要在@NgModule装饰器上添加FormsModule模块
- mock-heroes 模拟从服务器端获取的数据
- `*ngFor` 循环输出(let .. of ..) 复写器指令repeater
- (click) `()` 监听事件
- `*ngIf` 判断指令 如果为false 整段dom移除（不存在了）若为true 添加这段dom
- css类绑定机制 `[class.some-css-class]="some-condition"` 添加到要施加样式的元素上
- `@Input()`装饰器 可以添加一个带有这个装饰器的输入属性 从而通过该属性接受其他外部组件传入的对象
- `[hero]="selectedHero"` 属性绑定语法 （单向数据绑定）
- 组件中不直接获取数据 也不保存数据 专注视图；通过创建服务`ng generate service xxx`来获取数据，然后通过依赖注入机制把它注入到组件的constructor中
- `@Injectable()`装饰器 接受该服务的元数据对象 _（provide提供商这块有些模糊 还需看资料书籍）_
- HeroService 可以从任何地方获取数据：Web 服务、本地存储（LocalStorage）或一个模拟的数据源
- ngOnInit 生命周期钩子
- `HttpClient.get()` 会返回 Observable( RxJS 库中的一个关键类) of()也返回Observable
- `Observable.subscribe()` 
- subscribe 函数把这个英雄数组传给这个回调函数，该函数把英雄数组赋值给组件的 heroes 属性(异步）
- 可以在服务中注入其他服务
- Angular 只会绑定到组件的公共属性(constructor中设置public属性)
- `--flat` 把这个文件放进了 src/app 中，而不是单独的目录中
  `--module=app` 告诉 CLI 把它注册到 AppModule 的 imports 数组中
- `routerLink`是 RouterLink 指令的选择器 会把用户的点击转换为路由器的导航操作
- Routes数组中`{ path: '', redirectTo: '/dashboard', pathMatch: 'full' }`路由匹配为默认显示的路由
- path 中的冒号（:）表示 :id 是一个占位符，它表示某个特定英雄的 id
- ActivatedRoute 保存着到这个 HeroDetailComponent 实例的路由信息。 这个组件对从 URL 中提取的路由参数感兴趣。 其中的 id 参数就是要现实的英雄的 id。
  location 是一个 Angular 的服务，用来与浏览器打交道
- `route.snapshot` 是一个路由信息的静态快照，抓取自组件刚刚创建完毕之后
- `paramMap` 是一个从 URL 中提取的路由参数值的字典
- JavaScript 的 (+) 操作符会把字符串转换成数字
- forRoot() 配置方法接受一个 InMemoryDataService 类（初期的内存数据库）作为参数
- HttpClient.put() 方法接受三个参数:URL 地址,要修改的数据（这里就是修改后的英雄）,选项 
- $ 是一个命名惯例，用来表明 heroes$ 是一个 Observable，而不是数组
- `*ngFor` 不能直接使用 Observable。 不过，它后面还有一个管道字符（|），后面紧跟着一个 async，它表示 Angular 的 `AsyncPipe`
 
 AsyncPipe 会自动订阅到 Observable，这样你就不用再在组件类中订阅了

