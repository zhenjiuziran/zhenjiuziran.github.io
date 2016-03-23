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
