GvTan的yii框架学习笔记
1.	Yii默认是指向Site控制器的，需要从新指定一下，指定方法与修改地址为：'defaultRoute' => 'gvtan',//默认控制器 ，位置为config\web.php; 不加载yii自带的默认模板样式的方法，在控制器的方法中添加 $this->layout = false;
2.	'cookieValidationKey' => 'My key' 此处的key为唯一key，最好去github上去生成一下。
3.	
    $config['bootstrap'][] = 'gii';
    $config['modules']['gii'] = [
        'class' => 'yii\gii\Module',
        'allowedIPs' => ['127.0.0.1', '::1', '192.168.188.*','192.168.0.103'],// 添加后台访问权限ip地址
    ];
    $config['modules']['admin'] = [ //开启访问路径  后台路径
        'class' => 'app\modules\admin',
];
此处配置yii相关文件，指定ip访问，与开启后台访问路径；
4．在数据配置文件中添加表前缀：'tablePrefix' => 'gv_',  位置是 config\db.php;
5.创建模型类;
	Namespace  app\models;
	Use yii\db\ActiveRecord; //需要继承此类
	class User extends ActiveRecord
{
	Public static function tableName()
{
Return “{{%user}}”;//{{%数据表名}}  此处括号和百分号代表表前缀，前提是需要在db.php 中配置了表前缀。
}
}
6.使用模型类：需要在使用的控制器中use app\models\User; 引用，然后使用静态方式调用，User::find->all();
7.将从表中查询出来的所有数据渲染到前台页面：return $this->render(‘index’,[‘userdatas’=>$dataall]); 返回数据为带数据对象的二维数组；
8.前台页面循环输出内容：
<?php foreach ($userdatas as $userdata):?>
	<?php echo $userdata->id;?>  <!--  此处的id为数据表中的字段 -->
<?php echo $userdata->username;?>  <!--  此处的username为数据表中的字段 -->
<?php endforeach;?>
