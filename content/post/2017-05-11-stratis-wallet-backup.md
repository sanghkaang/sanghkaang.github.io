![](https://steemitimages.com/0x0/https://cdn-images-1.medium.com/max/800/1*lnHRa3D7XxjCp4Fl7hPgHQ.jpeg)

안녕하세요.

지난글에서 지갑을 무사히 설치했다면 이번글에선 지갑을 백업하는법을 알아보겠습니다.
지갑을 무사히 설치하였더라도, 만일의 사태는 발생할 수 있습니다. 지갑이 설치된 컴퓨터가 파손된다면 어떻게 할건가요?

이럴때를 대비해 지갑을 백업해둬야만 합니다. 관리부주의로 가상화폐의 소유권을 잃어버릴수도 있습니다. 이 글을 읽으시는 분들도 반드시 백업파일을 만들어두시길 바랍니다.

# 백업방법 1

![](../images/stratis-backup/1.png)
-   간단하게 `파일 -> 지갑 백업`을 통해 백업 파일을 만들 수 있습니다.

![](../images/stratis-backup/2.png)
-   원하는 경로에 원하는 이름으로 백업 파일을 만들수 있습니다.
-   이름은 원하는대로 설정 가능하지만 일반적으로는 `wallet`으로 하는걸 추천드립니다.(복원할떄 파일 이름이 `wallet.dat`이어야 복원가능함)
-   저는 **백업파일을 압축하여 암호를 걸어둔 뒤** USB, 그리고 클라우드에 보관중입니다.

# 백업방법 2
![](../images/stratis-backup/3.png)
-   위의 방법으로 `wallet.dat`파일을 생성해도 되지만 스트라티스 지갑을 설치하셨다면 이미 `wallet.dat`파일이 생성되어있습니다. 이 파일을 복사해서 백업파일로 사용하셔도 됩니다.
-   **각 운영체제별로 wallet.dat 경로가 다릅니다.** 아래의 내용을 참조해주세요.
-   윈도우의 경우, 예를 들어 로그인계정이 `sanghun`이라면 `wallet.dat`의 경로는 *C:\Users\sanghun\AppData\Roaming\Stratis\wallet.dat*입니다.

```
Windows: C:\Users\<로그인한유저명>\AppData\Roaming\Stratis\wallet.dat
Mac: ~/Library/Application Support/stratis/wallet.dat
Linux:  ~/.stratis/wallet.dat
```

# 복구방법
-   컴퓨터를 포맷해서 지갑이 날라갔거나, 지갑을 다른곳으로 옮기고싶을떄 위에서 만들어둔 백업파일을 사용하면 됩니다.
-   백업파일을 아래의 경로에 넣어주세요.

```
Windows: C:\Users\<로그인한유저명>\AppData\Roaming\Stratis\wallet.dat
Mac: ~/Library/Application Support/stratis/wallet.dat
Linux:  ~/.stratis/wallet.dat
```



생각보다 쉽죠? 이게 끝입니다. 간단한 방법으로 이렇게 가상화폐를 지킬수 있습니다. 최근 거래소를 타겟으로한 ddos공격이 늘고 있습니다. 혹시 거래소에 스트라티스를 두고 계시다면 이번 기회에 꼭 개인지갑을 생성해서 개인지갑에 보관하는걸 추천드립니다.
