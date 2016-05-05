# UmengRestApiPhpDemo

// *****需要php安装mcrypt插件

// 调用方法  
$key = "273d7e70c2d115e62e0e45656ff82b39";  
$aes = new AesEncrypt($key);  

$data = '{"source_uid": "123312", "source": "qq", "source_name": "hello"}';  
// 加密  
$data = pack("N",strlen($data)).$data;  
$string = $aes->encrypt($data);  
echo base64_encode($string);  
// 解密  
echo " ||  ",$aes->decrypt($string);  
