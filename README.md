<h1 style="text-align:center">
    GvTan<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">的</span>yii<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">框架学习笔记</span>
</h1>
<p class="MsoListParagraph" style="margin-left:24px">
    1.<span style="font-variant-numeric: normal;font-variant-east-asian: normal;font-stretch: normal;font-size: 9px;line-height: normal;font-family: &#39;Times New Roman&#39;">&nbsp;&nbsp;&nbsp; </span>Yii<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">默认是指向</span>Site<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">控制器的，需要从新指定一下，指定方法与修改地址为：</span><span style="background:yellow;background:yellow">&#39;defaultRoute&#39; =&gt; &#39;gvtan&#39;,//</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">默认控制器</span> <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">，位置为</span><span style="background: yellow;background:yellow">config\web.php</span>; <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:aqua;background:aqua">不加载</span><span style="background:aqua;background:aqua">yii</span><span style="font-family: &#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:aqua;background:aqua">自带的默认模板样式的方法</span><span style="font-family: &#39;微软雅黑&#39;,&#39;sans-serif&#39;">，在控制器的方法中添加</span> <span style="background:yellow;background:yellow">$this-&gt;layout = false;</span>
</p>
<p class="MsoListParagraph" style="margin-left:24px">
    2.<span style="font-variant-numeric: normal;font-variant-east-asian: normal;font-stretch: normal;font-size: 9px;line-height: normal;font-family: &#39;Times New Roman&#39;">&nbsp;&nbsp;&nbsp; </span><span style="background:yellow;background:yellow">&#39;cookieValidationKey&#39; =&gt; &#39;My key&#39;</span> <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">此处的</span>key<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">为唯一</span>key<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">，最好去</span>github<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">上去生成一下。</span>
</p>
<p class="MsoListParagraph" style="margin-left:24px">
    3.<span style="font-variant-numeric: normal;font-variant-east-asian: normal;font-stretch: normal;font-size: 9px;line-height: normal;font-family: &#39;Times New Roman&#39;">&nbsp;&nbsp;&nbsp; </span>&nbsp;
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    &nbsp;&nbsp;&nbsp; <span style="background:yellow;background:yellow">$config[&#39;bootstrap&#39;][] = &#39;gii&#39;;</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp; $config[&#39;modules&#39;][&#39;gii&#39;] = [</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#39;class&#39; =&gt; &#39;yii\gii\Module&#39;,</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#39;allowedIPs&#39; =&gt; [&#39;127.0.0.1&#39;, &#39;::1&#39;, &#39;192.168.188.*&#39;,&#39;192.168.0.103&#39;],// </span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">添加后台访问权限</span><span style="background:yellow;background:yellow">ip</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">地址</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp; ];</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp; $config[&#39;modules&#39;][&#39;admin&#39;] = [ //</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">开启访问路径</span><span style="background:yellow;background:yellow">&nbsp; </span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">后台路径</span>
</p>
<p class="MsoListParagraph" style="margin-left:53px;text-indent:0">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &#39;class&#39; =&gt; &#39;app\modules\admin&#39;,</span>
</p>
<p class="MsoListParagraph" style="margin-left:24px;text-indent:18px">
    <span style="background:yellow;background: yellow">];</span>
</p>
<p class="MsoListParagraph" style="margin-left:24px;text-indent:18px">
    <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">此处配置</span>yii<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">相关文件，指定</span>ip<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">访问，与开启后台访问路径；</span>
</p>
<p>
    4<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">．在数据配置文件中添加表前缀：</span><span style="background:yellow;background:yellow">&#39;tablePrefix&#39; =&gt; &#39;gv_&#39;,</span> &nbsp;<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">位置是</span> <span style="background:yellow;background: yellow">config\db.php</span>;
</p>
<p>
    5.<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">创建模型类</span>;
</p>
<p>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="background:yellow;background:yellow">Namespace &nbsp;app\models;</span>
</p>
<p>
    <span style="background:yellow;background: yellow">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Use yii\db\ActiveRecord; //</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">需要继承此类</span>
</p>
<p>
    <span style="background:yellow;background: yellow">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; class User extends ActiveRecord</span>
</p>
<p style="text-indent:48px">
    <span style="background:yellow;background:yellow">{</span>
</p>
<p style="text-indent:48px">
    <span style="background:yellow;background:yellow">&nbsp; Public static function tableName()</span>
</p>
<p style="margin-left:48px;text-indent:48px">
    <span style="background:yellow;background:yellow">{</span>
</p>
<p style="margin-left:96px">
    <span style="background:yellow;background:yellow">Return “{{%user}}”;//{{%</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">数据表名</span><span style="background:yellow;background:yellow">}} &nbsp;</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">此处括号和百分号代表表前缀，前提是需要在</span><span style="background:yellow;background:yellow">db.php </span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">中配置了表前缀。</span>
</p>
<p style="margin-left:48px;text-indent:48px">
    <span style="background:yellow;background:yellow">}</span>
</p>
<p style="text-indent:48px">
    <span style="background:yellow;background:yellow">}</span>
</p>
<p>
    6.<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">使用模型类：需要在使用的控制器中</span><span style="background:yellow;background:yellow">use app\models\User;</span> <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">引用，然后使用静态方式调用，</span><span style="background:yellow;background:yellow">User::find-&gt;all();</span>
</p>
<p>
    7.<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">将从表中查询出来的所有数据渲染到前台页面：</span><span style="background:yellow;background:yellow">return $this-&gt;render(‘index’,[‘userdatas’=&gt;$dataall]);</span> <span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">返回数据为带数据对象的二维数组；</span>
</p>
<p>
    8.<span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;">前台页面循环输出内容：</span>
</p>
<p style="margin-left:29px">
    <span style="background:yellow;background:yellow">&lt;?php foreach ($userdatas as $userdata):?&gt;</span>
</p>
<p style="margin-left:29px">
    <span style="background:yellow;background:yellow">&nbsp;&nbsp;&nbsp;&nbsp; &lt;?php echo $userdata-&gt;id;?&gt; &nbsp;&lt;!-- &nbsp;</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">此处的</span><span style="background:yellow;background:yellow">id</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">为数据表中的字段</span><span style="background:yellow;background: yellow"> --&gt;</span>
</p>
<p style="margin-left:29px;text-indent:19px">
    <span style="background:yellow;background: yellow">&lt;?php echo $userdata-&gt;username;?&gt; &nbsp;&lt;!-- &nbsp;</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">此处的</span><span style="background:yellow;background:yellow">username</span><span style="font-family:&#39;微软雅黑&#39;,&#39;sans-serif&#39;;background:yellow;background:yellow">为数据表中的字段</span><span style="background:yellow;background: yellow"> --&gt;</span>
</p>
<p style="margin-left:29px">
    <span style="background:yellow;background:yellow">&lt;?php endforeach;?&gt;</span>
</p>
<p>
    <br/>
</p>
