#### 右侧滑入组件 lcb-slide
***

#### 组件描述
简单的右侧滑入效果，用户可自行往组件里填写页面逻辑
***

1.参数说明
>@Input()
* isShow:控制弹层显示与隐藏，Boolean类型

>@Output()
* onShowchange:组件本身显示、隐藏时触发的变动

2.代码示例
```
<lcb-slide [isShow]="_isShow" (onShowchange)="onShowchangeFun($event)">
  <!--展示的内容-->
</lcb-slide>
```
*注意点：若展示内容是组件级的，那滑入组件的输入输出需要一级级向上或者向下传递*
