# snmp
FreeDSx/SNMP 中文文档
> 基于 https://github.com/FreeDSx/SNMP

Freedsx SNMP 是一个纯的 PHP SNMP库。依赖其他扩展。它实现了RFC 3412 / RFC 3416 / RFC 3414中描述的SNMP客户端功能。它还包括在各种其他RFC中描述的功能，例如SHA2认证（RFC 7860）和强加密机制（3DES / AES-192-256）。有些主要功能包括：

SNMP版本1,2和3支持。

支持所有身份验证机制（MD5，SHA1，SHA224，SHA256，SHA384，SHA512）。

支持所有隐私加密机制（DES，3DES，AES128，AES192，AES256）。

支持所有客户端请求类型（GET，GetNext，GetBulk，Set，Inform，Trapv1，Trapv2）。

支持发送SNMPv1和SNMPv2陷阱（包括通知请求）。

陷阱宿服务器用于接收和处理传入陷阱。

隐私/加密支持需要OpenSSL扩展。64位计数器（BigCounter）需要GMP扩展。



## configuration 配置

配置列表

- host
- port
- version
- community
-  user
- use_auth
- auth_pwd
- auth_mech
- use_priv
- priv_mech
- priv_pwd
- engine_id
- context_name
- timeout_connect
- timeout_read

```
use FreeDSx\Snmp\SnmpClient;

$snmp = new SnmpClient([
    'host' => 'server',
    'version' => 2,
    'community' => 'foo',
]);
```

#### 参数解析：

- host
 连接主机，默认 `localhost`
-  port  
-  version
-  community
-  user
-  use_auth
-  auth_pwd
-  auth_mech
-  use_priv
-  priv_pwd
-  engine_id
-  context_name
-  timeout_connect
-  timeout_read
