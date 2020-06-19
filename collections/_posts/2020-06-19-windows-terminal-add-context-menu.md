---
title: "windows 10 context menu에 terminal  추가하기"
category:
    - os
tags:
    - terminal
---

Microsoft에서 WSL2 및 terminal 서비스를 하게 되면서 자주 사용하게 되는데

PowerShell과 같이 폴더에서 오른쪽클릭해서 해당위치로 바로 못여는것에 대한 아쉬움이 있었다.

![](/assets/img/20200619/Untitled.png)

[그림] terminal에서 실행시킨 ubuntu

위 아쉬움을 해결하고자 구글링을 해본결과!!

해결법을 찾게되어 공유하고자 한다.

사실 terminal에서 한줄만 실행시키면 되긴하는데 혹시 찾으시는분이 있을까봐 공유를 한다.

---

# 준비물

- windows Terminal  
[설치 바로가기](https://aka.ms/terminal){:target='_blank'}
- windows PowerShell7  
[설치 방법 보러가기](https://github.com/PowerShell/PowerShell/releases){:target='_blank'}

---

# 설치

powerShell7를 관리자권한으로 실행시킨 후

~~~powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/lextm/windowsterminal-shell/master/install.ps1'))
~~~

위 코드를 입력시킨다.

![](/assets/img/20200619/Untitled1.png)

[그림] contextmenu에 terminal를 추가한 사진
