# 购买Redis实例<a name="ZH-CN_TOPIC_0102039829"></a>

购买Redis实例支持“包年包月”和“按需付费”两种方式。您可以根据业务需要购买相应计算能力和存储空间的Redis实例，同时可购买多个Redis实例。

## 前提条件<a name="section62331491"></a>

Redis实例运行于虚拟私有云。购买Redis实例前，需保证有可用的虚拟私有云，并且已配置好安全组与子网。

创建虚拟私有云、安全组以及子网的方法，请参见[环境准备](环境准备.md)或者《虚拟私有云用户指南》。

## 操作步骤<a name="section24112512"></a>

1.  登录[管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0102039895.gif)图标，选择区域和项目。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >此处请选择与租户的应用服务相同的区域。  

3.  单击页面上方的“服务列表”，选择“数据库 \> 分布式缓存服务”，进入分布式缓存服务信息页面。
4.  单击“购买缓存实例”，进入购买页面。
5.  选择“计费模式”。单击选择“包年/包月”或者“按需付费”。
6.  填写Redis实例的参数。参数说明如[表1](#table5373863818728)所示。

    **表 1**  参数说明

    <a name="table5373863818728"></a>
    <table><thead align="left"><tr id="row5933206518728"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.3.1.1"><p id="p5858956018728"><a name="p5858956018728"></a><a name="p5858956018728"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="83%" id="mcps1.2.3.1.2"><p id="p4813390218728"><a name="p4813390218728"></a><a name="p4813390218728"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row153681361123"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p53681836827"><a name="p53681836827"></a><a name="p53681836827"></a>区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p183684366219"><a name="p183684366219"></a><a name="p183684366219"></a>DCS服务所在区域，可在页面左上角切换区域。</p>
    </td>
    </tr>
    <tr id="row109721311105019"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p1199512215509"><a name="p1199512215509"></a><a name="p1199512215509"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p89961721195017"><a name="p89961721195017"></a><a name="p89961721195017"></a>Redis实例的名称。</p>
    <a name="ul91142212509"></a><a name="ul91142212509"></a><ul id="ul91142212509"><li>名称不能为空。</li><li>只能以英文字母开头。</li><li>创建单个实例时，名称长度为4到64位的字符串。批量创建实例时，名称长度为4到56位的字符串，且实例名称格式为“自定义名称-<em id="i320102295010"><a name="i320102295010"></a><a name="i320102295010"></a>n</em>”，其中n从000开始，依次递增。例如，批量创建两个实例，自定义名称为dcs_demo，则两个实例的名称为dcs_demo-000和dcs_demo-001。</li><li>仅包含英文字母、数字、下划线（_）和中划线（-）。</li></ul>
    </td>
    </tr>
    <tr id="row1397401165016"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p153832213505"><a name="p153832213505"></a><a name="p153832213505"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p134320227508"><a name="p134320227508"></a><a name="p134320227508"></a>对Redis实例的描述信息。</p>
    </td>
    </tr>
    <tr id="row3606388018728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p110575018728"><a name="p110575018728"></a><a name="p110575018728"></a>缓存类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p2245694518728"><a name="p2245694518728"></a><a name="p2245694518728"></a>缓存的引擎类型，单击选择“Redis”。</p>
    </td>
    </tr>
    <tr id="row2846066118728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p5613947218728"><a name="p5613947218728"></a><a name="p5613947218728"></a>缓存版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p5100339218728"><a name="p5100339218728"></a><a name="p5100339218728"></a>缓存的引擎类型的版本，目前支持3.0.7。</p>
    </td>
    </tr>
    <tr id="row55532325104357"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p1824480104357"><a name="p1824480104357"></a><a name="p1824480104357"></a>实例类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p13565167104357"><a name="p13565167104357"></a><a name="p13565167104357"></a>缓存实例的类型。Redis实例支持“单机”、“主备”和“集群”。</p>
    <div class="note" id="note1771175816202"><a name="note1771175816202"></a><a name="note1771175816202"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p28641128829"><a name="p28641128829"></a><a name="p28641128829"></a>集群Redis实例不支持通过VPC对等连接的方式进行跨VPC访问。</p>
    </div></div>
    <p id="p5105963408"><a name="p5105963408"></a><a name="p5105963408"></a>请根据实际需要选择实例类型，不同实例类型适用不同的业务场景，具体参考<a href="http://support.huaweicloud.com/productdesc-dcs/zh-cn_topic_0088428506.html">实例缓存类型说明</a>。</p>
    </td>
    </tr>
    <tr id="row1166533611517"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p25231444105115"><a name="p25231444105115"></a><a name="p25231444105115"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p552614415511"><a name="p552614415511"></a><a name="p552614415511"></a>可选择的不同可用分区。</p>
    <div class="note" id="note13528144155115"><a name="note13528144155115"></a><a name="note13528144155115"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1253034413517"></a><a name="ul1253034413517"></a><ul id="ul1253034413517"><li>当主备或者集群Redis实例进行跨可用分区部署时，如果其中一个可用分区故障，另一个可用分区的节点不受影响。备节点会自动升级为主节点，对外提供服务，从而提供更高的容灾能力。</li><li>由于实例跨可用分区部署时网络访问效率略低于部署在同一可用分区内，因此Redis实例跨可用分区部署时，主备节点之间同步效率会略有降低。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row136661636155119"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p15467441511"><a name="p15467441511"></a><a name="p15467441511"></a>跨可用区部署</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p2548144185115"><a name="p2548144185115"></a><a name="p2548144185115"></a>跨可用分区部署的开关。</p>
    </td>
    </tr>
    <tr id="row5666153615115"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p655213446510"><a name="p655213446510"></a><a name="p655213446510"></a>备可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p655484414515"><a name="p655484414515"></a><a name="p655484414515"></a>备可用分区。</p>
    <div class="note" id="note2555204411512"><a name="note2555204411512"></a><a name="note2555204411512"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p155597445513"><a name="p155597445513"></a><a name="p155597445513"></a>只有“跨可用区部署”开关为打开状态，当前存在多个可用分区，并且用户选择的实例类型为“主备”或“集群”时，才会显示该参数。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row5088731918728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p5731035618728"><a name="p5731035618728"></a><a name="p5731035618728"></a>实例规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p12782887115750"><a name="p12782887115750"></a><a name="p12782887115750"></a>缓存实例的规格。</p>
    <div class="p" id="p187771325152014"><a name="p187771325152014"></a><a name="p187771325152014"></a>Redis实例规格为：<a name="ul3392184713239"></a><a name="ul3392184713239"></a><ul id="ul3392184713239"><li>单机和主备实例规格支持2GB、4GB、8GB、16GB、32GB和64GB。</li><li>按需付费的集群实例，支持的实例规格为64GB、128GB和256GB；包年/包月付费的集群实例，支持的实例规格为64GB、128GB、256GB、512GB和1024GB。</li></ul>
    </div>
    <p id="p195594514220"><a name="p195594514220"></a><a name="p195594514220"></a>用户默认配额为最多创建5个实例，总内存不超过400GB。</p>
    <p id="p13895221123619"><a name="p13895221123619"></a><a name="p13895221123619"></a>用户如需增加配额，单击规格下方的“申请扩大配额”，即可跳转到工单管理界面提交工单，增加配额。</p>
    </td>
    </tr>
    <tr id="row3119715618728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p5533269218728"><a name="p5533269218728"></a><a name="p5533269218728"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p5276310218728"><a name="p5276310218728"></a><a name="p5276310218728"></a>已创建的虚拟私有云。</p>
    <a name="ul353316111561"></a><a name="ul353316111561"></a><ul id="ul353316111561"><li>虚拟私有云可以为您的Redis实例构建隔离的、用户自主配置和管理的虚拟网络环境。</li><li>单击“查看虚拟私有云”，系统跳转到虚拟私有云界面，选择相应的虚拟私有云，可以查看安全组的出方向规则和入方向规则。</li></ul>
    </td>
    </tr>
    <tr id="row4851808618728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p184411618728"><a name="p184411618728"></a><a name="p184411618728"></a>子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p1515573018728"><a name="p1515573018728"></a><a name="p1515573018728"></a>子网名称与IP地址段。</p>
    </td>
    </tr>
    <tr id="row196181012465"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p49541115154613"><a name="p49541115154613"></a><a name="p49541115154613"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p395471584614"><a name="p395471584614"></a><a name="p395471584614"></a>已创建的安全组。</p>
    <p id="p35999277569"><a name="p35999277569"></a><a name="p35999277569"></a>安全组是一组对弹性云服务器的访问规则的集合，为同一个VPC内具有相同安全保护需求并相互信任的弹性云服务器提供访问策略。</p>
    </td>
    </tr>
    <tr id="row3827185974517"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p182815593451"><a name="p182815593451"></a><a name="p182815593451"></a>公网访问</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p148281959104513"><a name="p148281959104513"></a><a name="p148281959104513"></a>公网访问的开关。</p>
    <div class="note" id="note55151547163815"><a name="note55151547163815"></a><a name="note55151547163815"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul14605173614573"></a><a name="ul14605173614573"></a><ul id="ul14605173614573"><li>公网访问与VPC内访问相比，可能存在网络丢包和抖动等情况，且访问时延有所增加，因此建议仅在业务开发测试阶段开启公网访问Redis实例。</li><li>公网访问只支持Redis密码模式，免密模式暂不支持，请注意设置密码。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row16239840114613"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p112391540184615"><a name="p112391540184615"></a><a name="p112391540184615"></a>弹性IP地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p651757154010"><a name="p651757154010"></a><a name="p651757154010"></a>开启公网访问功能的Redis实例，需要通过弹性IP访问。</p>
    <p id="p1184063620435"><a name="p1184063620435"></a><a name="p1184063620435"></a>用户可下拉选择已有的弹性IP，或者单击“创建弹性IP”跳转到虚拟私有云的“申请弹性IP”界面创建弹性IP。</p>
    <div class="note" id="note06888212424"><a name="note06888212424"></a><a name="note06888212424"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul725713468420"></a><a name="ul725713468420"></a><ul id="ul725713468420"><li>只有“<span id="ph3257246144217"><a name="ph3257246144217"></a><a name="ph3257246144217"></a>公网访问</span>”开关为打开状态才会显示该参数。</li><li>如果用户在虚拟私有云的服务页面手动解绑定或删除EIP，DCS服务会自动关闭相应缓存实例的公网访问功能。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row99846205521"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p172524296529"><a name="p172524296529"></a><a name="p172524296529"></a>免密访问</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p2252112915214"><a name="p2252112915214"></a><a name="p2252112915214"></a>免密访问的开关。</p>
    <div class="note" id="note22851625115610"><a name="note22851625115610"></a><a name="note22851625115610"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul151104364521"></a><a name="ul151104364521"></a><ul id="ul151104364521"><li>免密模式存在安全风险，请谨慎使用。</li><li>若打开了“公网访问”开关，必须设置密码。</li><li>若申请免密模式的Redis实例，申请成功后，可以通过重置密码进行密码设置，具体可参考<a href="开启Redis实例的免密访问.md">开启Redis实例的免密访问</a>章节。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row6515734618728"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p3400959418728"><a name="p3400959418728"></a><a name="p3400959418728"></a>密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p204469959544"><a name="p204469959544"></a><a name="p204469959544"></a>连接Redis实例的密码。包括密码及确认密码。</p>
    <div class="note" id="note14021145182415"><a name="note14021145182415"></a><a name="note14021145182415"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul74450401594"></a><a name="ul74450401594"></a><ul id="ul74450401594"><li>只有“免密访问”开关为关闭状态时，才会显示该参数。</li><li>DCS服务出于安全考虑，在密码访问模式下，连接使用Redis实例时，需要先进行密码认证。请妥善保存密码，并定期更新密码。</li></ul>
    </div></div>
    <p id="p1205499104250"><a name="p1205499104250"></a><a name="p1205499104250"></a>Redis实例密码必须满足以下复杂度要求：</p>
    <a name="ul65262816102030"></a><a name="ul65262816102030"></a><ul id="ul65262816102030"><li>密码不能为空。</li><li>输入长度为6到32位的字符串。</li><li>必须包含如下四种字符中的两种组合：<a name="ul1443183119407"></a><a name="ul1443183119407"></a><ul id="ul1443183119407"><li>小写字母</li><li>大写字母</li><li>数字</li><li>特殊字符包括（`~!@#$^&amp;*()-_=+\|{}:,&lt;.&gt;/?）</li></ul>
    </li></ul>
    </td>
    </tr>
    <tr id="row175574015417"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p185589055411"><a name="p185589055411"></a><a name="p185589055411"></a>时间窗</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p2558130125418"><a name="p2558130125418"></a><a name="p2558130125418"></a>运维操作时间。</p>
    <p id="p538867566"><a name="p538867566"></a><a name="p538867566"></a>用户可选择22:00-02:00、02:00-06:00、06:00-10:00、10:00-14:00、14:00-18:00和18:00-22:00，在选择的时间段内，服务运维可对实例节点进行维护操作。</p>
    </td>
    </tr>
    <tr id="row118341211193619"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p108351611113614"><a name="p108351611113614"></a><a name="p108351611113614"></a>备份策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p19835121183611"><a name="p19835121183611"></a><a name="p19835121183611"></a>只有当实例类型为“主备”时显示该参数。关于实例备份的说明及备份策略的设置请参考<a href="备份与恢复说明.md">备份与恢复说明</a>。</p>
    </td>
    </tr>
    <tr id="row1750163032614"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p117113447261"><a name="p117113447261"></a><a name="p117113447261"></a>配置费用</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><p id="p5171184419267"><a name="p5171184419267"></a><a name="p5171184419267"></a>购买当前规格的实例费用。</p>
    <p id="p5778171732811"><a name="p5778171732811"></a><a name="p5778171732811"></a>选择包年/包月付费模式时，显示当前规格下购买时长的一次性总费用。</p>
    <p id="p17855145173311"><a name="p17855145173311"></a><a name="p17855145173311"></a>选择按需付费模式时，显示当前规格下每小时所需费用。</p>
    </td>
    </tr>
    <tr id="row108211720133714"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.3.1.1 "><p id="p782242083715"><a name="p782242083715"></a><a name="p782242083715"></a>购买量</p>
    </td>
    <td class="cellrowborder" valign="top" width="83%" headers="mcps1.2.3.1.2 "><a name="ul068711613138"></a><a name="ul068711613138"></a><ul id="ul068711613138"><li>选择“包年/包月”付费模式时购买量包括使用时长和实例个数。</li><li>选择“按需付费”时购买量指购买缓存实例个数。<div class="note" id="note104381255145315"><a name="note104381255145315"></a><a name="note104381255145315"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p683523815318"><a name="p683523815318"></a><a name="p683523815318"></a>开启公网访问后，不支持批量创建Redis实例。</p>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

7.  填写完上述信息后，单击“立即购买”，进入确认页面。

    页面显示申请的分布式缓存服务的实例名称、缓存版本和实例规格等信息。

8.  确认实例信息无误后，提交请求。
    -   如果选择“包年/包月”，单击“去支付”，进入付款页面，完成付款后即可创建实例。

        如果暂不确定，可关闭页面，暂不支付，稍后可在“费用 \> 我的订单”中支付或取消订单。

    -   如果选择“按需付费”，单击“提交”，开始创建实例。

9.  缓存实例创建成功后，用户可以在“缓存管理”页面，查看并管理自己的缓存实例。
    1.  创建缓存实例大约需要5到15分钟，如果创建集群实例，则需要大约30分钟。
    2.  缓存实例创建成功后，默认“状态”为“运行中”。
        -   对于“按需付费”模式的实例，如果创建缓存实例失败，可参考[删除缓存实例](删除缓存实例.md)，删除创建失败的缓存实例，然后重新购买。如果重新购买仍然失败，请联系客服。
        -   对于“包年/包月”模式的实例，有如下约束：
            -   付款成功后，才会创建缓存实例。
            -   如果创建缓存实例失败，可能是因为资源开通失败导致。用户可以联系客服取消订单，然后到“费用 \> 我的订单”中执行退订操作。




## 相关产品及文档<a name="section152613113129"></a>

<a name="zh-cn_topic_0046844820_table1073594361220"></a>
<table><thead align="left"><tr id="zh-cn_topic_0046844820_row197372430123"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0046844820_p4737243111216"><a name="zh-cn_topic_0046844820_p4737243111216"></a><a name="zh-cn_topic_0046844820_p4737243111216"></a>相关产品</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0046844820_p18737144301214"><a name="zh-cn_topic_0046844820_p18737144301214"></a><a name="zh-cn_topic_0046844820_p18737144301214"></a>相关文档</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0046844820_row17371443131210"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0046844820_p13372054101419"><a name="zh-cn_topic_0046844820_p13372054101419"></a><a name="zh-cn_topic_0046844820_p13372054101419"></a><a href="https://www.huaweicloud.com/product/dcs.html?infodocbz" target="_blank" rel="noopener noreferrer">分布式缓存 Redis</a></p>
<p id="zh-cn_topic_0046844820_p19548105714519"><a name="zh-cn_topic_0046844820_p19548105714519"></a><a name="zh-cn_topic_0046844820_p19548105714519"></a><a href="https://www.huaweicloud.com/product/dcsmem.html?infodocbz" target="_blank" rel="noopener noreferrer">分布式缓存 Memcached</a></p>
<p id="zh-cn_topic_0046844820_p8862161219564"><a name="zh-cn_topic_0046844820_p8862161219564"></a><a name="zh-cn_topic_0046844820_p8862161219564"></a><a href="https://www.huaweicloud.com/product/ecs.html?infodocbz" target="_blank" rel="noopener noreferrer">弹性云服务器 ECS</a></p>
<p id="zh-cn_topic_0046844820_p841193941416"><a name="zh-cn_topic_0046844820_p841193941416"></a><a name="zh-cn_topic_0046844820_p841193941416"></a><a href="http://www.huaweicloud.com/product/vpc.html?infodocbz" target="_blank" rel="noopener noreferrer">虚拟私有云 VPC</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0046844820_p1381695711471"><a name="zh-cn_topic_0046844820_p1381695711471"></a><a name="zh-cn_topic_0046844820_p1381695711471"></a><a href="https://support.huaweicloud.com/usermanual-dcs/dcs-zh-ug-180315001.html?infodocbz" target="_blank" rel="noopener noreferrer">购买Redis实例</a></p>
<p id="zh-cn_topic_0046844820_p682916370595"><a name="zh-cn_topic_0046844820_p682916370595"></a><a name="zh-cn_topic_0046844820_p682916370595"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0082114847.html?infodocbz" target="_blank" rel="noopener noreferrer">连接Redis实例</a></p>
<p id="zh-cn_topic_0046844820_p16726748155912"><a name="zh-cn_topic_0046844820_p16726748155912"></a><a name="zh-cn_topic_0046844820_p16726748155912"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0061845451.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例扩容</a></p>
<p id="zh-cn_topic_0046844820_p12250886517"><a name="zh-cn_topic_0046844820_p12250886517"></a><a name="zh-cn_topic_0046844820_p12250886517"></a><a href="https://support.huaweicloud.com/usermanual-dcs/zh-cn_topic_0079545637.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例备份恢复</a></p>
<p id="zh-cn_topic_0046844820_p143616360517"><a name="zh-cn_topic_0046844820_p143616360517"></a><a name="zh-cn_topic_0046844820_p143616360517"></a><a href="https://support.huaweicloud.com/migration-dcs/zh-cn_topic_0078784423.html?infodocbz" target="_blank" rel="noopener noreferrer">缓存实例数据迁移</a></p>
</td>
</tr>
</tbody>
</table>

