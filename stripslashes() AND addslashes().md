```
<!DOCTYPE HTML >

<html>

<head>

<meta http-equiv="Content-Type" content="text/html; charset=utf-8">

<title>應用addcslashes()函數和stripslashes()函數分別對字串進行轉義和還原</title>

</head>

<body>

<?php

 $str = "select * from tb_book where bookname = 'PHP5從入門到放棄'";

 echo $str."<br>";

$a = addslashes($str);  //對字串中的特殊字元進行轉義

 echo $a."<br>"; //輸出轉義後的字元

 $b = stripslashes($a); //對轉義後的字元進行還原

 echo $b."<br>"; //將字元原義輸出

?>

</body>

</html>
```

### addslashes()返回字符串，該字符串為了數據庫查詢語句等的需要在某些字符前加上了反斜線。
### 例:
```
<?php
$str = "Is your name O'reilly?";

// 輸出：Is your name O\'reilly?
echo addslashes($str);
?>
```
### stripslashes()該函數用於清理從數據庫或HTML表單中取回的數據。
### 例:
```
<?php
echo stripslashes("Who\'s John Adams?") ;
?>
```













