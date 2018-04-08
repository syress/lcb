#### 列表操作组件 lcb-options
***

##### 组件描述
依赖bootstrap的dropdown组件，通过文字描述，显示可操作项，可设置显示操作的个数，多余操作则以弹出的形式展示。其包括两种类型的操作：1.跳页；2.事件，通过传入参数options进行配置

1.参数说明
>@Input()
*   options:组件渲染数据展示（必填项）

数据格式
```
{
  showCount: 1, //显示的操作个数，大于该值的操作，将通过点击下拉进行展示
  optList: [{
    desc: "编辑",   //操作文字描述
    url: `/misMarket/activity/update/${item.id}`,   //操作点击所跳转的链接
    queryParams: "",    //链接请求参数
  }, {
    desc: "删除",
    event: 'delete'
  }]
};
```
其中，optList内容有两种类型，一种是url跳转类，一种是event操作类，操作类通过@Output()通知父组件对操作参数进行处理。
*   itemId:操作数据的唯一标识，一般是id（非必填）
*此组件搭配[mis-table](https://github.com/syress/lcb/blob/master/mis-table.md)时，itemId是自动带入的，无需输入*

>@Output()
*   acEvtOption:点击操作向父组件传递的数据

数据格式
```
{event: "delete", id: 75}
```

2.代码示例
```
<mis-options [options]="item.options" [itemId]="item.id" (acEvtOption)="acEvtOption($event)"></mis-options>
```
