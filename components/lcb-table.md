#### lcb-table 组件
***

1.参数说明
>@Input()
*   tableParams:表头中文描述、每列宽度百分比、是否排序（可选）
*   list:列表数据（请求返回的list对象）
*   keys:每列数据的取值属性
*   multiple:是否支持跨页多选,默认不支持
>@Output()
*   checkedList:选中的list集合
*   sort:表头排序
*   acEvt:接收触发事件

2.代码示例
```
<mis-table [list]="activityList" [tableParams]="tableParams" [keys]="keys" [multiple]="true" (checkedList)="checkedList($event)" (sort)="sort($event)"></mis-table>
```

3.参数格式
*   tableParams
```
const theadDesc = ["ID", "活动标题", "活动种类", "pv", "uv", "新uv", "注册", "下单", "支付", "完成", "领券量", "操作"];
const colPercent = [5, 25, 10, 5, 5, 5, 5, 5, 5, 5, 5, 15];
const sortDesc = ["id", "title", null, null, "uv", null, null, null, null, null, null, null];
theadDesc.forEach((item, index) => {
  const paramItem = {
    colPercent: colPercent[index],    // 列百分比
    theadDesc: item,     // 列标题
    sortDesc: sortDesc[index]     // 排序配置
  };
  this.tableParams.push(paramItem);
});

```
*sortDesc可省略，这是排序属性*

*   keys
```
this.keys = [
  {
    dictionary: null,  // 是否有字典
    desc: [""],        // 是否有td内行的文案
    arr: ["id"]        // td内展示的行
  },
  {
    desc: ["", "开始", "结束"],
    arr: ["title", "startTime", "endTime"]
  },
  {
    dictionary: "activityKind",
    arr: ["activityKind"]
  },
  {
    arr: ['mktActivityResultStatistics.countPv']
  }
];

```
*特别说明：若有列表操作项配置，需对list数据进行重新组合，添加option属性，格式详见列表操作组件[mis-option](https://github.com/syress/lcb/blob/master/mis-options.md)*
