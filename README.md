# Router

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.5.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).



Routes 路由配置，保存那个URL对应展示哪个组件，以及在哪个RounterOutlet中展示组件。
RouterOutlet 在Html中标记路由内容呈现位置的占位符指令
Router 负责在运行时执行路由的对象，可以通过调用其navigate()和navigateByUrl()方法来导航到一个指定的路由
RouterLink 在Html中声明路由导航的指令
ActivatedRount  当前激活的路由对象，保存着当前的



使用Angular Route导航


AppRoutingModule


-- 生成相关组件
ng g component home
ng g component product

-- 修改内容
这里是商品组件
这里是主页组件

-- 添加路由配置






