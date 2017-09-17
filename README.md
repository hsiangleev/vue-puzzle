
### vue拼图
 [链接地址]( https://hsiangleev.github.io/vue-puzzle/ )
>1. 定义组件box
> 2. 使用slot在父组件插入button，调用子组件this.$children[0].randomNum()重新生成随机数组达到重新开始游戏的目的
> 3.  子组件中使用v-for生成li，再添加样式时使用 (!val) 给空值添加样式
> 4.  代码思路：
> 	* 定义两个数组，一个为完成后的，一个为打乱的
> 	打乱数组代码: <br>
> ```javascript
> 	this.randomArr.sort(function (a,b){
> 	  return Math.random()-0.5;
> 	})
> ```
> 	* 每次移动前获取点击的 value 值，和其上下左右的 value 值
> 	* 判断若四周有value值为空，则交换数组顺序
> 	交换数组顺序代码: <br>
> 	this.randomArr.splice(index,1,lNum);<br>
> 	this.randomArr.splice(index-1,1,cNum);<br>
> 	* 每次移动后判断两个数组是否相等
> 	代码: <br>
> ```javascript
> 	if(this.numArr.join(" ")==this.randomArr.join(" ")){
> 		return true;
> 	}else{
> 		return false;
> 	}
> ```

***
