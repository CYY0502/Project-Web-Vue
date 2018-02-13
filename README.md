# Project-Web-Vue
Vue简单实战




通过Window.localStorage将数据读存与本地服务器
window.cs={
		set:set,
		get:get,
	};
	function set(key,val){
		localStorage.setItem(key,JSON.stringify(val));
	}
	function get(key){
		var json=localStorage.getItem(key);
		if (json) {
			return JSON.parse(json);
		}
	}
//cs是接口，重新封装了set和get方法


添加任务
add: function() {
				var title=this.current.title;
				if(!title&&title!==0) return;
				
				var title=Object.assign({},this.current);
				this.list.push(title);
				console.log(this.list);
				},
//Objectassign();
这个Object.assign()方法复制所有的可枚举的属性的值由一个或多个源对象到目标对象。它将返回目标对象。
//实例：克隆对象
var obj = { a: 1 };
var copy = Object.assign({}, obj);
console.log(copy); // { a: 1 }


