#### 分页组件 mis-pagination
***

#### 组件描述
基于bootstrap ui
组件内部点击分页自动触发路由更新，业务层接收到更新信息即可发送相应的请求。
***

1.参数说明
>@Input()
* pageInfo:分页数据信息

数据格式
```
{
  currentPage: 1,   //当前页
  pageSize: 20,   //每页条数 
  totalCount: "109"   //总条数
}
```
