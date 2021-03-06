# ListViewPlus
带有上拉加载下拉刷新的ListView
## 运行效果图 ##
![运行效果图](https://github.com/crazycodeboy/ListViewPlus/blob/master/raw/ListViewPlus%E8%BF%90%E8%A1%8C%E6%95%88%E6%9E%9C%E5%9B%BE.gif?raw=true)
##如何使用##
1. ListViewPlus是基于ListView开发的自定义控件，大家可以将ListViewPlus当成ListView来使用。
2. 使用ListViewPlus需要实现ListViewPlusListener接口，该接口定义了两个方法：
```java
public void onRefresh();//下拉刷新的时候会被回调
public void onLoadMore();//上拉加载更多的时候被回调
```
提示：实现了该接口之后要调用public void setListViewPlusListener(ListViewPlusListener l) 
来设置监听器。  
3. 为了方便使用，程序提供了
```java
public void setRefreshEnable(boolean enable)//设置下拉刷新是否可用
public void setLoadEnable(boolean enable)//设置上拉加载是否可用
```
两个方法来设置是否启用上拉加载和下拉刷新。  
4. 当刷新数据完成之后要通过public void setRefreshTime(String time)方法来设置刷新时间。     
5. 通过setAutoLoadEnable(boolean enable)方法可以启用上垃到底部时自动加载功能。
