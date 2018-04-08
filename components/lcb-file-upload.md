#### 图片上传 lcb-file-upload
***

#### 组件描述
1.可设置单图、多图上传
2.可对多图上传进行排序
***

1.参数说明
>@Input()
* multiple:是否支持多图上传（可不填，默认单图）
>@Output()
* imgs:排序后的图片信息

2.代码示例
```
  <lcb-file-upload (imgs)="getImgs($event)" [multiple]="true"></lcb-file-upload>
  <lcb-file-upload (imgs)="getImgs1($event)"></lcb-file-upload>
```
