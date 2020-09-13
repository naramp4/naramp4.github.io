---
title: "windows10에서 node.js 설치하기"
category:
    - node.js
tags:
    - web
    - node.js
    - windows10
---

windows10에서 node.js를 설치하는 여러방법 중 wsl(Linux용 windows 하위 시스템 - [자세히보기](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10){: target="_blank"})를 사용하여 설치를 해보았지만, 너무 느린 관계로 네이티브 Windows에서 node.js를 설치하는 방법을 알아보도록 하겠다.

# nvm-windows를 이용하여 node.js 및 npm 설치

1. [windows-nvm repository](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows){: target="_blank"}에서 nvm-setup.zip을 다운로드 및 설치

    ![/assets/img/20200913/Untitled.png](/assets/img/20200913/Untitled.png)

2. PowerShell를 열고 node.js설치
    - 최신버전 설치
        ```powershell
        nvm install latest
        ```

    - 원하는 버전 설치
        1. 설치가능한 버전 확인

        ```powershell
        nvm list available
        ```

        2. 버전 선택 후 설치

        ```powershell
        nvm install <version>
        ```

3. 설치된 버전 확인

    ```powershell
    nvm ls
    ```

4. 버전 선택

    ```powershell
    nvm use <version>
    ```

---

# 출처

[windows 개발자 센터 - Windows에 직접 Node.js 개발 환경 설치](https://docs.microsoft.com/ko-kr/windows/nodejs/setup-on-windows){: target="_blank"}