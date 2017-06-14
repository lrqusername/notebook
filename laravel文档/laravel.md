## laravel 目录结构
	1.public 				入口文件
	2.env					配置数据库的文件
	3.app/http/routes.php	路由的浏览
	4.app/http/controller	控制器
	5..env.example			自动忽略git提交

## 路由
	route::get('/' , 函数名@方法名);


## 创建控制
	php artisan make:controller admin/UserController	通过控制器提交.

	Route::get('/admin', 'admin\KaController@index');	路由的设置


## 语法
	dd();					是var_dump的意思
	return view('页面' , ['data'=>$data]);	分配数据,相当于Smarty里面的asign(分配
											  过去的有可能是数组)
	compact()				分配数据
	{{$data}}				页面的数据接收

## 循环语句
	@for($i = 0; $i > 5; $i++)
		<a href="">ddd</a>
	@endfor

	@foreach($data as $value)
		<a>{{$value}}</a>
	@endforeach

	@if(1 > 4)
		<a href="">ddd</a>
	@endif

	if (Input::has('name'))
	{
	//
	}

## 使用命名绑定

  1. 查$results= DB::select('select * from users where id = :id', ['id' => 1]);
  
  2. 增$insert = DB::insert('insert into users (id, name) values (?, ?)', [1, 'Dayle']);
  
  3. 改$updata = DB::update('update users set votes = 100 where name = ?', ['John']);
 
  4. 删$deleted = DB::delete('delete from users');

  5. 类似于D('user')->find(); $d = DB::table("user")->find(1);

  6. $d = DB::table("user")->where('id' , '>'  , 20)->get();

## 使用get post接收数据
  1. // 引入类
     use Illuminate\Support\Facades\Input;
	$name = Input::get();
## session使用方式
	存储数据
	session(['key' => 'vae']);
	删除数据
	session()->forget('list');
	获取数据
    $ses = session()->get('key');
	
## 注意
	lavarel区分大小写

	laravel 默认开启了 csrf验证 ，不是get请求的话需要验证csrf,在表单里 加个隐藏域  
	<input type="hidden" name="_token"         value="{{csrf_token()}}"/>

	xiugai 
## 记录