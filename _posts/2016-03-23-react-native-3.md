---
layout: default
title: ReactNative的布局
---

今天学习下ReactNative的布局

插播广告：[SketchApp](http:www.sketchapp.com)

## 1. Q:怎么定制TabBarIOS的icon？##
A:使用[react-native-vector-icons](https:github.com/oblador/react-native-vector-icons)，与TabBarIOS结合如下

{% highlight javascript %}
var Icon = require('react-native-vector-icons/Ionicons');

<TabBarIOS.Item>....</TabBarIOS.Item>
//使用
<Icon.TabBarItem
  title="主页"
  iconName="ios-home-outline"
  selectedIconName="ios-home"
  selected={this.state.selectedTab === 'home'}
  onPress={() => {
    this.setState({
      selectedTab: 'home',
      notifCount: this.state.notifCount + 1,
    });
  }}>...</Icon.TabBarItem>
//替换，就可以使用react-native-vector-icons库中的3k+种icon了。
{% endhighlight %}

但是这个iconName和selectedIconName怎么确定呢？

在Ionicons.js文件中可以看到可以使用的名称，但是每个icon长什么样，对于非母语英语国家的人只能靠猜了，然后靠试。

插播广告：
![](/images/atom-beauty.png)
atom下最好用的格式化（美化）HTML,JS,CSS代码的扩展（package），没有之一，截止今日下载量96W+

## 2. Q:怎么设置顶部导航栏？ ##
A:使用[react-native-navbar](https://github.com/react-native-fellowship/react-native-navbar)

{% highlight react %}
<NavigationBar
  style={{borderBottomWidth:1,borderColor:"#acacac"}}
  title={titleConfig}
  rightButton={rightButtonConfig} />
{% endhighlight %}
