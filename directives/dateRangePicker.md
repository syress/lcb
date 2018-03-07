#### 时间插件指令 misDatePicker
***

#### 指令描述
1.支持单个时间选择
2.支持时间范围选择
3.支持ngModel双向绑定
***

1.参数说明
```
 {
    single: true,   //不填默认单个选择
    format: 'YYYY-MM-DD HH:mm:ss',    //格式化时间显示，不填默认YYYY-MM-DD
    timePicker: true,   //是否显示时分秒，不填默认不显示
    startDate: new Date(),    //设置开始时间，不填默认为空
    endDate: new Date()     //设置结束时间，不填默认为空
  };
```

2.代码示例
```
 <input type="text" class="form-control input-width col-lg-10" id="endTime" [misDatePicker]="pickerOpt" [(ngModel)]="activity.endTime">
```


