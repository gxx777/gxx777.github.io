# PyCrypto\PyCryptodome\PyCryptodomex



- PyCrypto

  - Python『前』主流加解密库，但已停更。
  - 所有模块都安装在 `Crypto` 包下

- PyCryptodome: 

  - 与 pyCrypto 有一些关联，并且可以被视为从 PyCrypto 迁移到 PyCryptodome 时的替代品。

  - ```
     pip install pycryptodome
    ```

  - 为了兼容`PyCrypto`的API 在这种情况下，所有模块都安装在 `Crypto` 包下。引入方式和`PyCrypto` 一致

- PyCryptodomex:  

  - ```py
     pip install pycryptodomex
    ```

  - **一个独立于旧 PyCrypto 的库。**

  - 是 PyCryptodome 的独立版本，具有不同的命名约定；而不是包`Crypto`，你必须使用`Cryptodome`. 



## 举一个例子

1. PyCrypto

```
from Crypto.Cipher import Salsa20

key = b'0123456789012345'
cipher = Salsa20.new(key)
```

2. PyCryptodome

```
from Crypto.Cipher import Salsa20

key = b'0123456789012345'
cipher = Salsa20.new(key)
```

3. PyCryptodomex

```
from Cryptodome.Cipher import Salsa20
key = b'0123456789012345'
cipher = Salsa20.new(key)
```

