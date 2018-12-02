---
layout: post
title:  "Wordpress Direct Plugin Installation"
date:   2014-06-18
tag:
- Wordpress
comments: true
---

Wordpress는 기본적으로 FTP, SFTP 등의 프로토콜을 통해 새로운 테마와 플러그인을 웹에서 설치하고 업데이트하는 방법을 제공한다. 하지만 FTP를 설정하는 과정은 번잡하고 고통스럽다. 그러나 Wordpress 폴더와 하위 파일의 소유자와 권한을 바꿔주기만 하면 손쉽게 Wordpress 알림판에서 플러그인을 바로 설치할 수 있다.

### wp-config.php 수정

먼저 wp-config.php을 수정해야 한다. 아래 코드를 추가해주자.

```
define('FS_METHOD', 'direct');
```

### Wordpress 폴더 소유자 변경

Wordpress 폴더의 소유자를 웹서버로 변경해준다. Apache의 경우 소유자와 소유 그룹이 둘 다 apache이어야 한다. 아니라면 다음 명령을 써서 바꿔주자.

```
chown -R apache:apache wordpress/
```

### Wordpress 폴더 권한 확인

다음 권한이 되도록 바꿔준다.

```
-rw-r--r--
```
