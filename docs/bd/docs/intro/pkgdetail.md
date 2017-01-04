## 移服接口（包名）【action=appdetail&package=xxx】
由包名package获取应用信息，该接口可以获取到商业的应用信息

## 请求说明 ##
### URL ###
> http://m.baidu.com/api?action=appdetail&package=*

### 请求方式 ###
> GET

### 支持格式 ###
> JSON/XML (默认XML)

### 请求参数 ###
|字段名称  | 备注 | 是否必选
| ------------ | ------------ | ------------
| from   | 来源，合作方标识，由百度BD提供 | <red>必选</red>
| token  | 标记，由百度分配的唯一的token，用于验证请求方的合法性 | <red>必选</red>
| type  |服务类别，type=app，对于android，type的值为app | <red>必选</red>
| package  |包名   |<red>必选</red>
|req_biz |	是否变现,1是 0否| <red>必选</red>
|bdi_imei   |android手机imei号。参见 [附录2》数据加密](/api?bdi_docs=1&action=intro&source=intro_extrainfo2 "附录2》数据加密")|  <red>必选</red>
|bdi_loc    |客户端所在的城市 例：北京市。（base64处理）| <red>必选</red>
|bdi_uip    |客户端ip（客户端用户请求ip）   |<red>必选</red>
|bdi_bear   |网络环境（WF/4G/3G/2G）  |<red>必选</red>
|resolution |手机分辨率 例：720_1280   |<red>必选</red>
|dpi    |屏幕密度 例：320 |<red>必选</red>
|apilevel   |系统api level 例：18（对应android 4.3）    |<red>必选</red>
|os_version |系统版本号 例：4.3    |<red>必选</red>
|brand  |手机品牌 例：OPSSON  |<red>必选</red>
|model  |手机型号 例：Q1  |<red>必选</red>
|pver   |协议版本（此版本固定为<red>4</red>）  |<red>必选</red>
|ua | user-agents，如 Mozilla/5.0 (compatible; MSIE 9.0; Windows Phone OS 7.5; Trident/5.0; IEMobile/9.0; HTC; Titan)|<red>必选</red>
|show_time	|点展示时间 时间戳 单位秒|<red>必选</red>
|refer_tag	|流量标识类型 board:频道/分类/软件列表;query:搜索 - query;rec:推荐位; other:其他 如流量入口是榜单形式，该参数应为 board|<red>必选</red>
|sign   |签名，<red>只针对该表的参数签名</red> 参见 [附录3》sign生成算法](/api?bdi_docs=1&action=intro&source=intro_extrainfo3 "附录3》sign生成算法")   |<red>必选</red>
|uid    |用户唯一标识 |可选
|bdi_mac    |无线网卡mac地址  |可选
|bdi_cid    |基站id   |可选
|bdi_imsi   |android手机imsi号。（base64处理）  |可选
|ct|    客户端点击时间 |可选
|cname  |客户端(宿主)名称  |可选
|cver   |客户端(宿主)版本号 |可选
|cpack| 客户端(宿主)包名|  可选

<blockquote class="bs-callout bs-callout-warning" style="padding:10px"><h4>注意</h4>为更好进行机型和网络适配，对于所有请求参数，尽可能携带可选参数; <red>所有参数（包括按 [附录2》数据加密](/api?bdi_docs=1&action=intro&source=intro_extrainfo2 "附录2》数据加密") 处理后的bdi_imei）都需要在上报时再进行urlencode</red></blockquote>

## 返回结果 ##
### XML示例 ###
```xml
<?xml version="1.0" encoding="UTF-8" ?>
<response>
    <statuscode>0</statuscode>
    <statusmessage>done</statusmessage>
    <result>
        <app>
            <sname><!--[CDATA[优酷]]--></sname>
            <docid>9828067</docid>
            <catename><!--[CDATA[影音播放]]--></catename>
            <cateid>506</cateid>
            <size>33028082</size>
            <download_url><!--[CDATA[http://cp01-appsearch-24.epc.baidu.com:8230/api?action=redirect&token=&from=1017206c&type=app&dltype=new&refid=1895639339&tj=soft_9828067_1827869107_%E4%BC%98%E9%85%B7&refp=action_batchapp&blink=c762687474703a2f2f612e67646f776e2e62616964752e636f6d2f646174612f7769736567616d652f306334623032633566643063333361322f796f756b755f3130352e61706b3f66726f6d3d6131313031ce57&crversion=1]]--></download_url>
            <icon><!--[CDATA[http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=9de6e80ad53e45aec5e89db13379bf5e&ref=http%3A%2F%2Fh.hiphotos.bdimg.com&src=http%3A%2F%2Fh.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2F354e9258d109b3de8b5cf4d0c4bf6c81810a4ca2.jpg]]--></icon>
            <versioncode>105</versioncode>
            <package>com.youku.phone</package>
            <iconhdpi><!--[CDATA[http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=d89d487982a99df117cb6016e60a0039&ref=http%3A%2F%2Fd.hiphotos.bdimg.com&src=http%3A%2F%2Fd.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2F5a12b31bb051f819fd2d10f2d2b44aed2e73e77a.jpg]]--></iconhdpi>
            <brief><!--[CDATA[【暑期重磅】<br-->2016新版好声音：开启夏日HIGH唱模式，不仅有周杰伦“小公举”等四位导师，更有李咏担当主持PK好舌头<br>【16个老公等你撩一夏】<br>微微一笑很倾城：全网独播，看杨洋郑爽湿身咚，媲美双宋CP好肤质<br>任意依恋：年度超甜虐恋韩剧，金宇彬秀智边虐边爱，只在优酷热播<br>幻城：全网热播，十年一瞬，幻你回城<br>诛仙青云志：联合独播，十年诛仙，引爆今夏<br>十宗罪：全网独播，诡异离奇的悬疑实案，撩人心弦的惊天侦破<br>步步惊心:丽：同步韩国全网独播即将上线，IU迷之穿越虐恋李准基，鲜肉王子团驾到苏裂天际<br>【更多热播霸屏来袭】<br>综艺：极限挑战2、火星情报局、金星秀、花样姐姐2、RM、我们相爱吧2、欢乐喜剧人、花样男团、跨界歌王、咱们穿越吧<br>剧集：好先生、欢乐颂、小丈夫、山海经、因为爱情有幸福、好想好想爱上你、琅琊榜、仙剑云之凡、解密，鲜肉大剧尽在优酷<br>海外：夜班经理、奶酪陷阱、学校2015、Oh我的维纳斯，步步惊心:丽即将上线<br>电影：老炮儿、功夫熊猫3、荒野猎人、美人鱼、星球大战、神探夏洛克，小门神，院线最新大片扎堆热播。]]&gt;</brief>
            <type>soft</type>
            <versionname>5.8.2</versionname>
            <all_download>0</all_download>
            <signmd5>1384977886</signmd5>
            <updatetime>2016-08-23</updatetime>
            <platform_version>4.0</platform_version>
            <packageid>1827869107</packageid>
            <all_download_pid>509660417</all_download_pid>
            <icon_source><!--[CDATA[http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=2988c90cff5bfc364c7411d1db02d1e2&ref=http%3A%2F%2Fb.hiphotos.bdimg.com&src=http%3A%2F%2Fb.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2Fd78f8c5494eef01fc33f1f7de8fe9925bc317d5b.jpg]]--></icon_source>
            <screenshot><!--[CDATA[http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=7df1d00c32ece507dcf91866d13758cd&ref=http%3A%2F%2Fe.hiphotos.bdimg.com&src=http%3A%2F%2Fe.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2Fe8d4b31c8701a18b03e301f7962f07082838fe7a.jpg;http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=702a4dfe5f5f6d7f4e6efbf3d87a4ab5&ref=http%3A%2F%2Fh.hiphotos.bdimg.com&src=http%3A%2F%2Fh.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2F9e1f4134970a304e02c1b042d9c8a786c8175ca2.jpg;http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=66165e1d2183e60871bcd5d73f1437a0&ref=http%3A%2F%2Fe.hiphotos.bdimg.com&src=http%3A%2F%2Fe.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2Ff6cad1c8a786c91753e04281c13d70cf3ac757a2.jpg;http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=e55855fbce9d7c7638c859bc63605f2c&ref=http%3A%2F%2Ff.hiphotos.bdimg.com&src=http%3A%2F%2Ff.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2F0f81800a19d8bc3eac6215728a8ba61ea8d3451b.jpg;http://cdn00.baidu-img.cn/timg?vsapp&size=b800_800&quality=100&imgtype=3&er&sec=0&di=b3a2001a44d8ef46dd3213925b0a6cc9&ref=http%3A%2F%2Fb.hiphotos.bdimg.com&src=http%3A%2F%2Fb.hiphotos.bdimg.com%2Fwisegame%2Fpic%2Fitem%2Fb209b3de9c82d158d5494909880a19d8bd3e42ba.jpg]]--></screenshot>
            <md5>e0eb8a370c4b02c5fd0c33a282de3c46</md5>
        </app>
    </result>
</response>
```

### 返回字段说明 ###
----------
参见 [附录4》返回APP字段说明](/api?bdi_docs=1&action=intro&source=intro_extrainfo4 "附录4》返回APP字段说明")

### 错误示例 ###
```xml
<?xml version="1.0" encoding="UTF-8" ?>
<response>
    <statuscode>108</statuscode>
    <statusmessage>[from] , param is signed in a wrong type</statusmessage>
</response>
```
### 错误说明 ###
参见 [附录4》返回码对照表](/api?bdi_docs=1&action=intro&source=intro_extrainfo4 "附录4》返回码对照表")