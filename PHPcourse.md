# 📘 مقدمة إلى PHP

## ✅ ما هي PHP؟
PHP (اختصار لـ **Hypertext Preprocessor**) هي لغة برمجة تُستخدم بشكل واسع لتطوير مواقع الويب الديناميكية.  
تُشتغل في الخادم (server-side)، يعني الكود كيتم تنفيذه فالسيرفر وكيترسل الناتج للمستخدم.

---

## 🧠 مميزات PHP
- 🔄 **ديناميكية**: كتخدم مع قواعد البيانات باش تصايب صفحات تتغير تلقائياً.
- 💰 **مجانية ومفتوحة المصدر**.
- 🌐 **متوافقة** مع جميع الخوادم (Apache, Nginx).
- 🧩 **تدعم العديد من أنظمة إدارة المحتوى** بحال WordPress.

---

## 🛠️ المتطلبات
باش تخدم بـ PHP خاصك:
- خادم محلي (Local Server) بحال:
  - [XAMPP](https://www.apachefriends.org/)
  - [Laragon](https://laragon.org/)
- محرر كود (VS Code مثلاً).



# 📘 أكواد PHP

## 1. echo

```php
<?php
  echo "Hello, World!";
?>
```
**✅ النتيجة:**
```
 Hello, World!
```
 🗒️ **ملاحظات :**

✔️ في بداية اي كود كتكون  `<?php` 

✔️ كتستعمل `echo`  باش تطبع شي حاجة.

✔️ `?>` نهاية الكود.



## 2. variables

```php
<?php

$age = 20;
echo "age = $age";

?>
```
**✅ النتيجة:**
```
 age = 20
```
---

```php
<?php

$name = "ahmed";
echo "How are you $name";

?>
```
**✅ النتيجة:**
```
 How are you ahmed
```

 🗒️ **ملاحظة :**

✔️ عند استدعاء متغير او عند تعريفه كتستعمل `$` قبل اسمه.

## 3. Conditions

```php
<?php

$price = 1300;
if ($price > 1000) {
    echo "price > 1000";
}else{
    echo "price < 1000";
}

?>

```
**✅ النتيجة:**
```
 price > 1000
```
---

```php
<?php

$price = 2900;
if ($price > 3000) {
    echo "Iphone 12";
}elseif($price > 2800 && $price < 3000){
    echo "Iphone 11";
}
else{
    echo "Iphone 8";
}

?>

```
**✅ النتيجة:**
```
 Iphone 11
```
## 4. Loops

```php
<?php

$i = 0;
while($i < 10){
    echo   $i;
    $i++;
}

?>


```
**✅ النتيجة:**
```
 0123456789
```

```php
<?php

for($i = 2015 ; $i <= 2025 ; $i++){
    #هاد السطر ديال html 
    echo "<br>";
    echo $i;
}
?>

```
**✅ النتيجة:**
```
 2015
 2016
 2017
 2018
 2019
 2020
 2021
 2022
 2023
 2024
 2025
```

## 5. Fonctions

```php
<?php

function printname($name){
    echo "Hello $name";
    #هاد السطر ديال html 
    echo "<br>";
}

printname("Ahmed");
printname("Younes ");
printname("Mohammed ");
printname("Walid ");
?>

```
**✅ النتيجة:**
```
 Hello Ahmed
 Hello Younes
 Hello Mohammed
 Hello Walid
```

---

```php
<?php

$name = 'ahmed';

function printname(){
    echo  $GLOBALS['name'];

}

printname();

?>

```
**✅ النتيجة:**
```
 ahmed
```

 🗒️ **ملاحظة :**

✔️ ملي كيكون المتغير خارج الدالة كتستعمل `GLOBALS$` باش تقدر تستخدمه في الدالة.

## 6. **Arrays**


```php
<?php

$listname = array("Ahmed", "Mohammed", "Younes", "Shady", 5, 32) ;

echo $listname[2]; 

?>

```
**✅ النتيجة:**
```
 Younes
```
---

```php
<?php

$listname = array(
    "name" => "ahmed",
    "age" => 22 ,
    "city" => "Casablanca"
    ) ;

echo $listname['name']; 

?>

```
**✅ النتيجة:**
```
 ahmed
```
---

```php
<?php

$listname = array(
    "name" => "ahmed",
    "age" => 22 ,
    "city" => "Casablanca"
    ) ;

echo $listname['age']; 

?>

```
**✅ النتيجة:**
```
 22
```
---

```php
<?php

$listname = array(
    "name" => "ahmed",
    "age" => 22 ,
    ) ;

foreach($listname as $key => $value){
    echo $key;
    echo "<br/>";
}
?>

```
**✅ النتيجة:**
```
    name
    age
```
---

```php
<?php

$listname = array(
    "name" => "ahmed",
    "age" => 22 ,
    ) ;

foreach($listname as $key => $value){
    echo $value;
    echo "<br/>";
}
?>

```
**✅ النتيجة:**
```
    ahmed
    22
```
---

```php
<?php

$listname = array(
    "name" => "ahmed",
    "age" => 22 ,
    "city" => "Casablanca"
    ) ;

foreach($listname as $key => $value){
    echo "$key = $value <br>";
}
?>

```
**✅ النتيجة:**
```
    name = ahmed
    age = 22
    city = Casablanca
```
 🗒️ **ملاحظات :**
 
- `foreach`: حلقة كنستعملوها باش ندورو على جميع العناصر داخل المصفوفة (array).

- `$key`: هو المفتاح (key) ديال كل عنصر فالمصفوفة. مثلاً: `"name"`.

- `$value`: هو القيمة (value) المرتبطة داك المفتاح. مثلاً: `"ahmed"`.

- `echo "$key = $value <br>";`: كيطبع المفتاح والقيمة ديالو على شكل نص، و`<br>` كتدير سطر جديد فـ HTML.

---

```php
<?php

$listname = array(
    "name",
    "ahmed",
    "mohamed",
    "ali",
    array("Casablanca", "Rabat", array(
        "name" => "Yasser",
        "age" => 20,
    ))
);

echo $listname[4][2]["name"];

?>

```
**✅ النتيجة:**
```
    Yasser
```
 🗒️ **ملاحظة :**
 
✔️ الكود فيه مصفوفة داخل مصفوفة داخل مصفوفة، وكيطبع الاسم "Yasser" من داخل آخر وحدة.

---

```php
<?php

$listname = array(
    "name",
    "ahmed",
    "mohamed",
    "ali",
    array("Casablanca", "Rabat", array(
        "name" => "Yasser",
        "age" => 20,
    ))
);

print_r ($listname[4][2]);
?>

```
**✅ النتيجة:**
```
    Array ( [name] => Yasser [age] => 20 )
```
 🗒️ **ملاحظة :**
 
✔️ دالة `print_r` كتستعملها باش تطبع مصفوفة (array) بكل العناصر ديالها.

---

```php
<?php

$listname = array(
    "name",
    "ahmed",
    "mohamed",
    "ali",
    array("Casablanca", "Rabat", array(
        "name" => "Yasser",
        "age" => 20,
        "rr" => array(
            "name" => "Zakaria",
            "age" => 33,
        )
    ))
);

print_r ($listname[4][2]["rr"]["name"]);
?>

```
**✅ النتيجة:**
```
    Zakaria
```
## 7. **GET**

```php
<?php

$name = $_GET['name'];

echo $name ;  
?>

```
استخدام `$_GET` باش نستقبل البيانات من المستخدم من خلال URL.

```
http://localhost/phpcourse.php?name=Ahmed
```

**✅ النتيجة:**
```
    Ahmed
```
---
```
http://localhost/phpcourse.php?name=Zakaria
```

**✅ النتيجة:**
```
    Zakaria
```
---

```php
<?php

$name = $_GET['name'];
$age = $_GET['age'];
$email = $_GET['email'];

echo $name ;
echo "<br>";
echo $age ;
echo "<br>";
echo $email ;

?>

```
استخدام `$_GET` باش نستقبل البيانات من المستخدم من خلال URL.

```
http://localhost/coursePHP/index.php?name=ahmed&age=22&email=ahmedmouatassim@gmail.com
```

**✅ النتيجة:**
```
    ahmed
    22
    ahmedmouatassim@gmail.com
```
---
```
http://localhost/coursePHP/index.php?name=mohammed&age=20&email=mohammed2003@gmail.com
```

**✅ النتيجة:**
```
    mohammed
    20
    mohammed2003@gmail.com
```
