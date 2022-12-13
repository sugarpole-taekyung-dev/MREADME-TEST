# RFID

# Description

## 1. 개발 환경 및 개발 소스 다운로드

### 1.1 윈도우

- **Windows 10 버전**으로 테스트 진행했습니다. (기타 버전은 테스트 진행하지 않았습니다.)

### 1.2 C#

- **.NET Framework 4 버전** 이상이 설치되어 있어야 합니다.
    
    (관련 프로젝트: RFID_DeviceHistory, RFID_ReaderLib)
    
- **.NET Framework 4.6 버전** 이상이 설치되어 있어야 합니다.
    
    (관련 프로젝트: RainDropRFID)
    

### 1.3 Mysql

- **8.0.23 버전**으로 테스트 진행했습니다. ****(기타 버전은 테스트하지 않았습니다)

### 1.4 개발 소스

- DB가 준비되어 있지 않다면 프로젝트 내 CleanDB 폴더에서 ‘sql.bat’의 사용자, 암호, 포트번호를 수정한 후 파일을 실행시킵니다.
    
    참고:  2.1 개발자가 수정해야 할 파일
    

## 2. 프로그램 구조 및 소스 수정

### 2.1 프로그램 디렉터리 구조

![RainDropRFID](https://user-images.githubusercontent.com/120069592/207229300-37dd3450-6ad9-428e-bd20-4c3d4ef39d1a.png)


### 2.1 개발자가 수정해야 할 파일

1. setting.ini 파일의 MAINEXAM 섹션을 DB에 맞게 수정합니다.
    
    (DB는 Raindrop과 공유합니다.)
    
2. sql.bat 파일의  user, 비밀번호, port 를 사용자의 DB에 맞게 수정합니다. 
    
    ex) "C:\Program Files (x86)\MariaDB 10.4\bin\mysql" -u root -proot -P3306 < raindrop_smartfactory.sql
    "C:\Program Files (x86)\MariaDB 10.4\bin\mysql" -u ‘아이디’ -p’비밀번호’ -P’포트번호’ < raindrop_smartfactory.sql
    

| 파일이름 | 설명 | 코드에서의 사용구분 |
| --- | --- | --- |
| setting.ini  | DB연동, 장비연동, 환경설정에 따른 기능사용 여부 등을 설정합니다. | 설정 |
| sql.bat | 데이터베이스 생성 | DB |
