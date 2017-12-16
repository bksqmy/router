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




AppRoutingModule


-- 生成相关组件
ng g component home
ng g component product

-- 修改内容
这里是商品组件
这里是主页组件

-- 添加(路由配置)
const routes: Routes = [
  {path: '', component: HomeComponent},
  {path: 'product', component: ProductComponent},
];
-- RouterOutlet
在app.component.html 会有一个<router-outlet></router-outlet>，有插座的作用
-- 寻找匹配的路由组件
<a [routerLink]="['/']">主页</a>
<a [routerLink]="['/product']">商品详情</a>
-- routerLink是一个数组，而不是一个字符串


-- 在代码中通过router对象进行导航
在 app.component.ts 添加函数
  toProductDetails() {
    this.router.navigate(['/product']);
  }
在 app.component.html  添加导航引用
<input type="button" value="商品详情" (click)="toProductDetails()">

-- 当用户输入一个没有定义的路由
-- 生成一个组件 code404
ng g component code404
-- 当输入不存在插座时，能够跳转到404页面
注意路由顺序，否则会直接匹配404页面
 {path: '', component: HomeComponent},
  {path: 'product', component: ProductComponent},
  {path: '**', component: Code404Component},

-- 重定向路由
当用户访问一个特定的地址时，将其重定向到一个指定的地址
{path: '', redirectTo: '/home', pathMatch: 'full'},
 {path: '/home', component: HomeComponent},

-- 子路由
生成商品的描述组件
ng g component productDesc
这是一个牛X的商品
ng g component sellerInfo
销售员ID {{sellerId}}

children属性



