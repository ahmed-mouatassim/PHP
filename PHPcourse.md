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
---
```php
<?php

$name = $_GET['name'];
$age = $_GET['age'];
$email = $_GET['email'];

print_r($_GET);

?>

```
استخدام `$_GET` باش نستقبل البيانات من المستخدم من خلال URL.

```
http://localhost/coursePHP/index.php?name=Younes&age=30&email=younes15@gmail.com
```

**✅ النتيجة:**
```
    Array ( [name] => Younes [age] => 30 [email] => younes15@gmail.com )
```
 🗒️ **ملاحظات :**
 
✔️ دالة `print_r` كتستعملها باش تطبع مصفوفة (array) بكل العناصر ديالها.

✔️ المصفوفة (array) تستخدم البيانات المستلمة من المستخدم من خلال URL, يعني ليس من الضروري تعريفها في الكود.

## مثال:

```php
<?php

print_r($_GET);

?>

```
```
http://localhost/coursePHP/index.php?name=Aymen&age=27&email=aymen789@gmail.com
```

**✅ النتيجة:**
```
    Array ( [name] => Aymen [age] => 27 [email] => aymen789@gmail.com )
```
---


# 🔌 PDO Connect Database MYSQL

```php
<?php 


$dsn = "mysql:host=localhost;dbname=coursephp" ; 
$user = "root" ;
$pass = "" ; 
$option = array(
    PDO::MYSQL_ATTR_INIT_COMMAND => "SET NAMES UTF8" // FOR Arabic
);

try {

    $con = new PDO($dsn , $user , $pass , $option ); 
    $con->setAttribute(PDO::ATTR_ERRMODE , PDO::ERRMODE_EXCEPTION) ;
    


}catch(PDOException $e){

  echo $e->getMessage() ;        

}

```
### هاد الكود كيربط تطبيق PHP ديالك مع قاعدة بيانات (MySQL database) باستخدام تقنية اسمها PDO (PHP Data Objects). وكايتعامل مزيان مع الأخطاء، وكيخلي الكود أكثر أمان وتنظيم.

## 🧱 تفصيل الكود:

ا **dsn:** هادي هي "Data Source Name"، يعني منين غادي نربطو قاعدة البيانات.

ا **mysql:host=localhost:** كنقولو بأن قاعدة البيانات خدامة محلياً (localhost).

ا **dbname=coursephp:** اسم قاعدة البيانات هو coursephp.

ا **root:** هو اسم المستخدم (User) ديال قاعدة البيانات، فالغالب فـ XAMPP ولا Laragon كيكون root.

ا **pass = "" :** ماكيناش كلمة مرور (فغالب الأحيان ما كتكونش فـ السيرفر المحلي).


ا **option:** كتعني إعدادات إضافية لربط قاعدة البيانات.

ا **SET NAMES UTF8:** باش يدعم اللغة العربية فـ القاعدة (مهم بزاف باش الحروف العربية ما يخرجوش مخربقين ❌).

ا **try { ... }:** كنقولو ليه جرب تربط القاعدة، وإذا وقع مشكل، سِير للـ catch.

ا **new PDO(...):** هنا كنديرو إنشاء الاتصال.

ا **setAttribute(...):** كنقولو لـ PDO بأنه إلا وقع خطأ، خصو يرمي Exception، باش نقدرو نتحكمو فيه.

ا **catch(PDOException $e):** إلا وقع خطأ فالاتصال، غادي يتحط هنا.

ا **echo $e->getMessage():** يطبع لينا رسالة الخطأ، باش نعرفو شنو وقع بالضبط.

### 🗒️ ملاحظة :
 
✔️ هاد الكود ماشي ضروري تفهموا كامل 100% حيت كتكتبوا مرة وحدة وكتبقا تخدم بيه دائما👌.

### 📌 معلومات مهمة خاصك تعرف:

✅ ال PDO = طريقة عصرية فـ PHP باش تربط مع القاعدة.

✅ خاص يكون عندك خادم محلي (XAMPP/Laragon).

✅ القاعدة خاصها تكون معمولة من قبل فـ phpMyAdmin واسمها "coursephp".

✅ ما تنساش تشعل السيرفر (Apache + MySQL).


 # 📚 PDO Fetch

### قراءة البيانات من قاعدة البيانات باستخدام PDO

```php
<?php

include "connect.php" ;

$stmt = $con->prepare("SELECT * FROM users");
$stmt->execute();
$users = $stmt->fetchall(PDO::FETCH_ASSOC);

echo "<pre>" ;
print_r($users) ;
echo "</pre>" ;

?>

```

## 🧱 تفصيل الكود:
 
ا **"include "connect.php:** هاد السطر كيدخل الملف ديال الاتصال بقاعدة البيانات (connect.php).

ا **prepare :** مهمة باش تحمي التطبيق ديالك من الهجمات (مثل SQL Injection) وكتخلي الكود منظم أكثر.

ا **" SELECT * FROM users ":** كيعني جيب ليا جميع السطور (rows) من جدول users.

ا **execute():** هاد السطر كيخلّي الاستعلام يتنفذ فعلاً، 
حيت دابا غير حضّرنا الاستعلام، وبهذا السطر كنديروه فعّال.

ا **fetchAll(PDO::FETCH_ASSOC):** هادي كتجيب جميع النتائج من قاعدة البيانات.

ا **print_r():** كتطبع المصفوفة بطريقة مفهومة.

### 🗒️ ملاحظات :
✔️ داك connect.php ضروري يكون فيه con$ معرف ومربوط مزيان.

✔️ تأكد أن جدول users راه موجود فـ قاعدة البيانات.

✔️ إذا وقع خطأ، استعمل try/catch باش تعرف السبب.

## 📦 **أنواع Fetch:**

| الطريقة                         | التوضيح                                                       |
|----------------------------------|----------------------------------------------------------------|
| `fetch()`                        | كتجيب **سطـر واحد** فقط من النتائج                            |
| `fetchAll()`                     | كتجيب **جميع السطور** دفعة وحدة                               |
| `fetch(PDO::FETCH_ASSOC)`        | كيرجع النتائج كمصفوفة بمفاتيح الأعمدة                         |
| `fetch(PDO::FETCH_NUM)`          | كيرجع النتائج بالأرقام (0, 1, 2...) بلا أسماء الأعمدة         |
| `fetch(PDO::FETCH_BOTH)`         | كيرجع النتائج بزوج: المفاتيح والأسامي (أرقام وأسامي الأعمدة) |
| `fetch(PDO::FETCH_OBJ)`          | كيرجع النتائج على شكل كائن (object)                           |
| `fetchColumn()`                  | كتجيب **قيمة وحدة فقط** من أول سطر (مثلاً اسم أو عدد)        |
| `rowCount()`                     | عدد السطور لي جابهم الاستعلام                                 |
| `prepare()`                      | تحضير الاستعلام قبل التنفيذ                                   |
| `execute()`                      | تنفيذ الاستعلام                                               |
| `bindParam()` / `bindValue()`    | لحماية من SQL Injection                                       |


```php
<?php 

<?php

include "connect.php" ;

$stmt = $con->prepare("SELECT * FROM users where username = 'mohammed'");
$stmt->execute();
$users = $stmt->fetchall();

$count = $stmt->rowCount() ;

echo $count ;

 ?>

```

### هاد الكود كيرجع عدد السطور اللي جابهم الاستعلام, مثلا اذا كان في الجدول username واحد اسمه mohammed فسيعطيك الرقم واحد، واذا كان فيه اثنان اسمهم mohammed فسيعطيك الرقم اثنان، ...

## 🧱 تفصيل الكود:
ا **prepare("SELECT * FROM users WHERE username = 'mohamed'"):** كنحضّرو استعلام SQL فيه شرط "جيب ليا جميع السطور من جدول users لي فيهم username = 'mohamed'"

ا **rowCount():** كترجع عدد السطور اللي جابهم الاستعلام.

ا **echo $count:** كيطبع عدد النتائج على الشاشة.

# 🔁 تحويل البيانات لصيغة JSON باستعمال PHP

### ⚠️ المشكل: البيانات بصيغة PHP Array

ملي كنجيبو البيانات من قاعدة البيانات، PHP كيرجع لينا مصفوفة (Array) بهاد الشكل:
```
Array
(
    [0] => Array
        (
            [id] => 1
            [username] => ahmed
            [email] => ahmedmou@gmail.com
        )

    [1] => Array
        (
            [id] => 2
            [username] => mohammed
            [email] => mohammed@gmail.com
        )

    [2] => Array
        (
            [id] => 3
            [username] => Younes
            [email] => youness55@gmail.com
        )

)

```

هاد الصيغة ماغاديش يفهمها Flutter حيت هادي خاصة بـ PHP.

**💡 الحل: استعمال دالة ()json_encode :**

كتعطينا PHP  واحد الدالة ساهلة سميتها json_encode، الدور ديالها هو تشد أي مصفوفة (Array) فـ PHP وتحولها لـ JSON.

فالكود ديالنا، بلاصة ما نطبعو المصفوفة مباشرة، كنستعملو هاد الدالة:

```php

<?php

include "connect.php" ;

$stmt = $con->prepare("SELECT * FROM users where username = 'ahmed'");
$stmt->execute();
$users = $stmt->fetchall(PDO::FETCH_ASSOC);

$count = $stmt->rowCount() ;

echo json_encode($users) ;

?>
```

✔️ **هاد الكود كيحول البيانات اللي عندنا فـ PHP (بحال المصفوفات - Arrays) لواحد الصيغة سميتها JSON .**

✔️ **هاد JSON هي بحال شي لغة مشتركة أو مترجم كيخلي لغات البرمجة المختلفة (بحال PHP فالباك ايند و Dart فالفلاتر) يقدرو يتفاهمو بيناتهم.**

**✅ النتيجة: البيانات بصيغة JSON**

دابا، ملي كنستعملو هاد الدالة، النتيجة اللي كترجع كتكون بهاد الشكل:

```json
[
    {
        "id": "1",
        "username": "ahmed",
        "email": "ahmedmou@gmail.com"
    },
    {
        "id": "2",
        "username": "mohammed",
        "email": "mohammed@gmail.com"
    },
    {
        "id": "3",
        "username": "Younes",
        "email": "youness55@gmail.com"
    }
]
```

**✔️ هاد الصيغة الجديدة (اللي هي عبارة على List ديال Maps فـ Dart) ساهلة بزاف على Flutter باش يقراها ويتعامل معاها.**

**➕ مثال إضافي: إرسال رسالة بسيطة :**

نقدرو نستعملو json_encode حتى باش نصايبو رسائل بسيطة. مثلا، إلى بغينا نرجعو رسالة ديال النجاح أو الفشل.


```php

$response = array("message" => "How Are You");

echo json_encode($response);

```
✅ النتيجة فالمتصفح (Browser) كتكون:

```
{
  "message": "How Are You"
}
```

# 📑 insert Data to database

```php
<?php

include "connect.php" ;

$ahm = $con->prepare("INSERT INTO `users` (`username`, `email`) VALUES ('Yasser', 'yasser@gmail.com')");
$ahm->execute() ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
**✔️ هاد الكود كيقول ليك زيد واحد row في جدول users فيها القيم دياله username = Yasser و email = yasser@gmail.com.**

**✔️  الكود كيرجع رسالة نجاح أو فشل حسب ما حدث.**

## 🧱 تفصيل الكود:

ا **prepare("INSERT INTO `users` (`username`, `email`) VALUES ('Yasser', 'yasser@gmail.com')"):** هاد السطر كنحضّرو استعلام SQL فيه شرط "أضف ليا سطر جديد في جدول users فيه username = Yasser و email = yasser@gmail.com"

ا `()execute:` هاد السطر كيخلّي الاستعلام يتنفذ فعلاً، 

ا `()rowCount:` كترجع عدد السطور اللي جابهم الاستعلام.

ا `if (count$ > 0):` هاد السطر كيرجع رسالة نجاح أو فشل حسب ما حدث.

---

### هاد الاكواد عندها نفس الدور 👇 :

```php
<?php

include "connect.php" ;

$ahm = $con->prepare("INSERT INTO `users` (`username`, `email`) VALUES (?, ?)");
$ahm->execute(array("Samir","samir@gmail.com")) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>
 ```
 ---
```php
<?php

include "connect.php" ;

$ahm = $con->prepare("INSERT INTO `users` (`username`, `email`) VALUES (:us, :em)");
$ahm->execute(
    array(
        ":us" => "Zakariya",
        ":em" => "zakariya@gmail.com" ,
        )) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>
 ```

# 🔁 Update :

```php
<?php

include "connect.php" ;

$ahm = $con->prepare("UPDATE `users` SET username = 'Aymen' WHERE id = 3 ");
$ahm->execute() ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
---
```php
<?php

include "connect.php" ;

$ahm = $con->prepare("UPDATE `users` SET username = ? WHERE id = ? ");
$ahm->execute(array("Aymen", 3)) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
---

```php
<?php

include "connect.php" ;

$ahm = $con->prepare("UPDATE `users` SET username = :us WHERE id = :id ");
$ahm->execute(
    array(
        ":us" => "Aymen",
        ":id" => 3,
        )) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{	
    echo "faild" ;
}
?>

```

# 🗑️ Delete :

```php
<?php

include "connect.php" ;

$ahm = $con->prepare("DELETE FROM `users` WHERE id = 3 ");
$ahm->execute() ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
---
```php
<?php

include "connect.php" ;

$ahm = $con->prepare("DELETE FROM `users` WHERE id = ? ");
$ahm->execute(array(3)) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
---
```php
<?php

include "connect.php" ;

$ahm = $con->prepare("DELETE FROM `users` WHERE id = :id ");
$ahm->execute(
    array(
        ":id" => 3,
        )) ; 

$count = $ahm->rowCount() ;

if ($count > 0) {
    echo "seccess" ;
}else{
    echo "faild" ;
}
?>

```
---
# 📁 اهم الملفات لي خاص يكونو عندك فالمشروع ديالك :

 ## 1_ crud.dart :

 ```dart

import 'package:http/http.dart' as http;
import 'dart:convert';

class Crud {
  getRequest(String url) async {
    try {
      var response = await http.get(Uri.parse(url));
      if (response.statusCode == 200) {
        var responsebody = jsonDecode(response.body);
        return responsebody;
      } else {
        print("Error ${response.statusCode}");
      }
    } catch (e) {
      print("Error $e");
    }
  }
  postRequest(String url, Map data) async {
    try {
      var response = await http.post(Uri.parse(url), body: data);
      if (response.statusCode == 200) {
        var responsebody = jsonDecode(response.body);
        return responsebody;
      } else {
        print("Error ${response.statusCode}");
      }
    } catch (e) {
      print("Error $e");
    }
  }
}

?>
```

**📦 أول حاجة: شنو كيدير هاد الكود كاملًا؟ هاد الكود عبارة عن class سميتو Crud فيه جوج دوال:**

ا `getRequest:` باش تدير طلب من نوع GET (مثلاً تجيب بيانات).

ا `postRequest:` باش تبعث بيانات للسيرفر (مثلاً تسجل user ولا تدير login).

## 🧱 تفصيل الكود:
```dart
import 'package:http/http.dart' as http;
```
✔️ هادي كتستورد المكتبة ديال **http** اللي كتخليك تبعث وتستقبل البيانات من وإلى السيرفر.

✔️ كنستعملو **as http** باش نسميو هاد المكتبة **http** فالكود، بحال اسم مستعار.

---
```dart
import 'dart:convert';
```
✔️ هادي مكتبة ديال **Dart** كتسمح لينا نحولو النصوص لـ **JSON** أو العكس.


✔️ حيت السيرفر كيرد علينا فالغالب بـ **JSON،** خاصنا **jsonDecode** باش نفهموه.

---
```dart
class Crud {}
```
✔️ هنا كنعلنو على **class** سميتو **Crud**.

✔️ هاد **class** غادي نستعملوه باش نديرو اتصالات مع الـ **backend** ديالنا.

---
```dart
getRequest(String url) async {}
```
✔️ هادي دالة سميتو **getRequest** اللي بتحتاجو واحد **parameter** سميتو url (اللي هي عبارة عن رابط).

---
```dart
var response = await http.get(Uri.parse(url));

```
✔️ هادي كتستعملو دالة **http.get** من المكتبة **http**.

✔️ ا `await`: كنقولو ليه انتظر حتى نوصل نتائج الطلب.

✔️ ا `Uri.parse(url)`:  كنحولو الرابط (url) لـ **URI** (Uniform Resource Identifier) باش نرسله.

---

```dart
if (response.statusCode == 200) 

```
✔️ كيتأكد واش الجواب من السيرفر OK (الكود 200 = النجاح).

---

```dart
var responsebody = jsonDecode(response.body);

```
✔️ كنحولو الجواب لي جاء من السيرفر من **JSON** إلى **Dart Object** باش نستعملوها فـ Flutter.

✔️ ا `response.body` :  هي النص اللي جا من السيرفر (فالغالب **JSON**).

✔️ ا `jsonDecode` : كتحول النص إلى **Map** ولا **List**.

---

```dart
else {
  print("Error ${response.statusCode}");
}
```
✔️ إلا ماكانتش 200، كيطبع الخطأ ديال الكود.

---

```dart
catch (e) {
  print("Error $e");
}
```
✔️ `try/catch` : باش يتجنب crash فـ حالة كاين مشكل فـ الاتصال.

---

### الدالة الثانية `postRequest`:

```dart
postRequest(String url, Map data) async {}
```
✔️ هادي دالة سميتو **postRequest** اللي بتحتاجو **2 parameters**:

**1_** ا `url`: الرابط اللي نرسلو له البيانات.

**2_** ا `data`: البيانات اللي نرسلوها.

---

```dart
var response = await http.post(Uri.parse(url), body: data);

```
✔️ هنا كيسيفط طلب **POST** فيه البيانات اللي فـ **data**.

---

### ✅ الخلاصة :

✔️ ا `getRequest` : باش تجيب معلومات من السيرفر (مثلاً لائحة ديال المنتجات).

✔️ ا `postRequest` : باش تسيفط معلومات (مثلاً تسجل **user**).

 ✔️الكلاس **Crud** : يسهل عليك الخدمة، بلا ما تعاود تكتب الكود ديال **http.post** كل مرة.

## 2_ linkapi.dart :

```dart
const String linkServerName = "http://192.168.137.1/coursephp";
//Auth
const String linkSignUp = "$linkServerName/auth/signup.php";

```
---

```dart
const String linkServerName = "http://192.168.137.1/coursephp";
```

✔️ هنا كنخزنو رابط السيرفر فـ متغيّر اسميتو **linkServerName**.

✔️ ***192.168.137.1*** هو **IP address** ديال السيرفر (غالبًا الهاتف ولا الحاسوب اللي خدام فيه **XAMPP** أو **Laragon**).

✔️ ا **"coursephp"** هو اسم المجلد اللي فيه ملفات **PHP** ديالك (مثلاً signup.php, login.php…).

✔️ ا `const` معناها هاد القيمة ما غاديش تتبدل.

---
```dart
const String linkSignUp = "$linkServerName/auth/signup.php";

```

✔️ هنا كنستعملو **linkServerName** باش نبنيو رابط **signup.php**.

✔️ ا `/auth/signup.php` : يعني الملف **signup.php** كاين داخل مجلد اسميتوه **auth** داخل **coursephp**.

✔️ النتيجة النهائية ديال **linkSignUp** غادي تولي:

```php
 http://192.168.137.1/coursephp/auth/signup.php

```

✔️ وهاد الرابط هو اللي غادي تبعث ليه البيانات ديال التسجيل من تطبيق Flutter.

### 🧠 علاش درنا هكا؟
✔️ باش:

➖ ما نعاودوش نفس الرابط بزاف ديال المرات.

➖  إيلا بغيت تبدل IP ولا المجلد، تبدل غير فـ واحد المكان.

### ✅ مثال الاستعمال:

```dart
var response = await http.post(Uri.parse(linkSignUp), body: {
  "name": "ahmed",
  "email": "ahmed@gmail.com",
  "password": "1234"
});
```

✔️ يعني الكود ديالك غادي يبعت المعلومات مباشرة لـ **signup.php**.

---

