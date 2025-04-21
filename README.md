# special
special from project
<?php
session_start();

// أنشئ الجلسة إذا لم تكن موجودة
if (!isset($_SESSION['items'])) {
    $_SESSION['items'] = [];
}

// إضافة عنصر جديد إذا تم الإرسال
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $item = [
        'name' => $_POST['name'],
        'price' => floatval($_POST['price'])
    ];
    $_SESSION['items'][] = $item;
    header("Location: opening.php");
    exit();
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    .x1{
        position: absolute;

            top: 50%;
            left: 100%; 
            transform: translate(-50%, -50%);
    }
    .rectangle {
      width: 1221px;
      height: 80px;
      background-color: orange;
    }
    i {
        font-size: 60px;
    }
    .info{
        text-align: right ;
    }
    .count{
        text-align: right;
    }
    .view{
        text-align: right;

    }
    .l1{
        font-size: 32px;
    }
    .a {
        text-align: right;
    }
    .rate{
        text-align: right;

    }
</style>
<script>
        function increment() {
            const qty = document.getElementById('quantity');
            if (parseInt(qty.value) < parseInt(qty.max)) {
            qty.value = parseInt(qty.value) + 1;
        }}

        function decrement() {
            const qty = document.getElementById('quantity');
            if (parseInt(qty.value) > parseInt(qty.min)) {
                qty.value = parseInt(qty.value) - 1;
            }
        }
    </script>    
<body>
<div class="rectangle">
    <i> &nbsp; Shopping </i>
</div>

    <div class="info">
        <h1 >   اسم المنتج :  الهاتف الذكي سامسونغ جلاكسي الجيل الرابع يعمل بنظام الأندرويد </h1>
        <h2 > Samsung-Galaxy-A51 :  الكود   </h2>
        <h2 > 10000.00 DA  :  السعر   </h2>
        <h2 >  :  الوصف   </h2>
        <h3>استمتع بتجربتك مع الهاتف الذكي سامسونغ غالاكسي A51 المميز، الذي يأتي بشاشة كاملة عالية الدقة تمنحك تجربة رائعة وسلسلة، كما أنه مزود بكاميرا رباعية بعدة أوضاع تصوير احترافية ومعالج عالي الأداء وبقدرة استجابة عالية في جميع استخداماتك.    
</h3>
</div>

<br>

<div class="count">
<button onclick="decrement()">-</button>
    <input type="number" id="qty" value="1" min="0" max="10">
    <button onclick="increment()">+</button>
      <l1> :الكمية  </l1>
      <br>
      <br>
      <form method="POST">
        <input type="hidden" name="name" value="الهاتف الذكي سامسونغ جلاكسي الجيل الرابع يعمل بنظام الأندرويد">
        <input type="hidden" name="price" value="10000.00">
        
        <button type="submit">  إضافة </button>
    </form> 
</div>

<x1>
<img src="c:\VSCode\HTML\11111111\samsung-a51-blue.jpg">
    </x1>
<hr>
<hr>
<form class="view" method="post" action="save.php">
    <label for="view">          :الرأي    </label><br>
    <textarea name="view" id="view" rows="10" cols="50" placeholder="ماهو رأيك ؟"></textarea><br><br>
    <button type="submit">ارسال</button>
</form>

<form class="rate">
    <h2> :أرى أن المنتج  </h2>
    <button> منتج ممتاز </button>
    <br>
    <br>
    <button> منتج جيد </button>
    <br>
    <br>
    <button> منتج عادي </button>
    <br>
    <br>
    <button> منتج سيء </button>
</form>
<form class="news" >
    <h2> :المنتجات الجديدة </h2>
<a href="page2.html">
    <img src="c:\VSCode\HTML\11111111\projet01.PNG" alt="اضغط هنا" width="150">
  </a>
  <a href="page2.html">
    <img src="c:\VSCode\HTML\11111111\projet02.PNG" alt="اضغط هنا" width="150">
  </a>

    </form>

    <script type="text/javascript">
        let count = 1;
        const counter = document.getElementById("counter");

        function increase() {
            if (count < 10) {
                count++;
                counter.textContent = count;
            }
        }

        function decrease() {
            if (count > 1) {
                count--;
                counter.textContent = count;
            }
        }
    </script>
</body>
    
</html>
