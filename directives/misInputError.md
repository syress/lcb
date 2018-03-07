#### 表单错误提示指令 misInputError
***

#### 指令描述
结合继承自基类Model的，包含验证信息的类时，可实现实时输入监测
***

#### 注意点
用该指令的input标签，一定要声明id
***

1.代码示例
```
<input type="email" class="form-control input-width" *misInputError="activity.validationErrors.title" id="title"  [(ngModel)]="activity.title" placeholder="活动标题">
```
数据格式
上例中activity.validationErrors.title的值是由字符串数组组成的，指令会一次将错误信息列于input框下。如
```
["请输入活动内容", "手机号码格式有误"]
```



