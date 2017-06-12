<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script src="./js./jquery-1.12.1.min.js"></script>
	<link rel="stylesheet" href="./css./1.css">
</head>
<body>
	<header id="head">
		<div class="six-item"></div>
		<div class=" six-item">2</div>
		<div class="six-item">3</div>
		<div class=" six-item">4</div>
	</header>
	<main id="main">
		<div><a href="http://www.baidu.com">1</a></div>
		<div><a href="">2</a></div>
		<div><a href="">3</a></div>
	</main>

</body>
<script>

	// 历史记录
	var n  = sessionStorage.getItem("item");
	console.log(n);
	$('#head div').eq(n).addClass('add');
	$('#head div').click(function(){
		$(this).addClass("add").siblings().removeClass("add");
	})
	$('.six-item').each(function(){
		$(this).click(function(e){
			// 得到当前索引
			var i= $(this).index();
			console.log(i)
			sessionStorage.setItem('item',i);
		})
	})


	
</script>
</html>
