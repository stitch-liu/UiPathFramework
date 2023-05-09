MySQL 使用AES_ENCRYPT与AES_DECRYPT进行加密存储

# 例子：
# 加密
insert into users(username, password) values ('account1', aes_encrypt('password', 'keyword'));

# 解密
select username, aes_decrypt(password, 'keyword') as psd from users