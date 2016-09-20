# TabActivityDemo
ViewPager+fragment的一个demo,顶部有导航栏(实现懒加载)

懒加载简介:使用viewpager+fragment作为应用大的布局时，viewpager会通过setOffscreenPageLimit来设置预加载的项目，
不设置setOffscreenPageLimit，则默认为1（设置0无效，可以查看该方法源码知道），也就是当我们打开应用看到的时候fragment01时，
实际上其他fragment（例如fragment02）也进行了加载，只不过没有显示出来罢了，但是这样就造成了不必要的资源浪费
（例如，fragment02没有显示，但是却进行了大量的网络加载操作）。
基于上述情况，就有了懒加载方式的诞生
（即只加载当前显示页面且只加载一次，滑动到其他页面时才加载其他页面数据，当再滑动到已加载过数据的页面时不再进行数据加载操作
，若想要刷新数据，再调用相应的加载数据方法就好了）

## 预览图
<img src="https://github.com/wenwenwen888/TabActivityDemo/blob/master/preview/1.gif" width="30%" height="30%"></br>
