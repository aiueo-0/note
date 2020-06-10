


## 使用Git Bash创建Key
```
1.打开 Git Bash

2.ssh-keygen -t rsa -b 4096 -C "你的邮箱"，注意填写你的邮箱！

3.按三次回车,（第一次enter之后，会让填写passphrase，最好的办法是什么都不如输入，++直接回车，直接回车，直接回车++ 当然也passphrase也可以随便输入，记事本记一下，待会设置完之后检测需要用到）

4.运行ll ~/.ssh,可以看到有2个文件，这里记住id_rsa就是钥匙,千万不要把这个东西泄漏出去，id_rsa.pub就是锁，需要上传的是这个锁而不是钥匙。

5.运行 cat ~/.ssh/id_rsa.pub，得到一串东西完整的复制这串很长的乱码，复制到打开的GitHub网页KEY框里(gitHub->Settings->SSH and GPG keys)，点击提交，填写账户密码，或者选择一个GitHub账户即可

6.回到Git Bash，输入ssh -T git@github.com，得到如下图所示，如果passphrase 未设置，则直接enter回车即可，如果设置了就记住第4步设定的密码

```
