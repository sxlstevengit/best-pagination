# best-pagination 是什么?
用于web开发中异步分页组件
# 依赖 
- jquery.1.11.x
# 安装
## script
```html
// import jquery.js
<script type="text/javascript" src="js/jquery.js"></script>
// import best-pagination.js
<script type="text/javascript" src="js/best-pagination.js"></script>
```
# 使用
index.js
```html
<script type="text/javascript">
$(function(){

  	// 实例化Pagination
	var pagination = new Pagination({
		container: $("#J-pagination1"),
		curPage: 1,
		totalPage: 1,
		handler: function(value) {
			console.log(value);
		}
	});
  
});
</script>
```
# 结构
## 配置
|属性|说明|默认值|字段类型|
|:---|---|---|---|
| `container`|组件根节点.|`$("body")`|`jQuery object`|
| `curPage`|当前页码|`1`|`Number`|
| `totalPage`|总页码.||`Number`|
| `range`|页码区间范围.|`4`|`Number`|
| `showBox`|分页信息框.|`false`|`Boolean`|
| `lang`|按钮文本.|`first: "首页",prev: "上一页",next: "下一页",last: "尾页"`|`String`|
| `handler`|切换页码后回调.|function(){}|`Function`|
## 方法
#### reset(totalPage)
重置组件
```html
pagination.reset(totalPage);
```