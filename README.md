# ehi-i18n

#### 介绍
一个简单的I18n组件,足够完成日常使用的国际化功能,比较适合没有引入jQuery,vue等组件的项目

#### 软件架构
原生JS


#### 安装教程

下载 ehi-i18n.js
建立 xx.json 的语言包 xx与语言名称一致

#### 使用说明


```javascript
 <div>
        <h1 i18n="[html,attr.title]welcomeLogin" title=""></h1>
        <input type="text" i18n='[value]nameTips'> <br>
        <input type="text"  i18n='[value]pwdTips'> <br>
        <input type="checkbox"  i18n='[value]rememberPassword'> <br>
        <button i18n='login'></button>
    </div>
    <script src="./ehi-i18n.js"></script>
    <script>
        let i18n = new EhiI18n('./lan/',()=>{
            //获取当前语言
            console.log(`当前语言${i18n.getLanguage()}`)
            //从语言中获取值,可在Js获取的时候使用
            console.log(i18n.get('login'))
        });
        //切换语言,可以无刷新切换语言,callback会被触发执行
        //i18n.setLanguage('us')
        //重新加载当前语言,会触发callback
        //i18n.loadLanguage()

    </script>
```


#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


