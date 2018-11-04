# jx_busStation_map
The demo is used AMAP API，which is used to show the map of the busline.
In this demo, I revised the place of the searchbar by css file that is nearly copied from the offical website. Besdies, I add the start point and end point keywords as the inputs. And, I adopt click function to combine the inputs with busTravel query.

resources:

Problems and Solved:
1. 搜索框需要输入多次进行查询，但是只能点击一次。
   addlistener 来实现多次click触发，单纯的onclick = 函数，目前不知道为什么不能多次触发。
2. 多次搜索后，每次搜索结果会在之前的结果上叠加，因此map上多条路径。
   需要定义全局变量，通过clear()函数来进行清除。
3. 多次panel框会叠加出现。
   需要将之前的线路结果清除，需要绑定click search 来清除，通过内容清零的方式来实现的。


To be solved:
4. 初始化应该只显示搜索框和地图，不应该出现panel框和查询成功的log提示。


20181104：
问题4 解决了，因为程序直接在脚本中调用了，//杠掉就可以了。
 	 针对空输入进行判断，并且进行提示信息。

	

