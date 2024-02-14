# 축구왕

![Copy of Copy of fms 유저 테스트](https://github.com/fms-chukguwang/.github/assets/39757235/e557b6d7-684e-401f-ae83-93beede4b0ff)

### **프로젝트 소개**

축구를 사랑하는 모든 사람들을 위한, 축구팀 종합 관리 플랫폼, **축구왕** 

지역 기반 축구 커뮤니티 및 팀 관리 플랫폼. 지역 팀 모집, 경기 일정 및 결과 기록, 선수 통계, 소셜 기능, 실시간 업데이트로 축구팀을 효울적으로 관리 하세요! 

**Service Link** : https://www.fms-chukguwang.site/

**GitHub Link** : https://github.com/fms-chukguwang

### 팀원 소개

https://www.notion.so/7693693c07d549649c62f434affaf30c?pvs=21

### 서비스 아키텍처
![Untitled](https://github.com/fms-chukguwang/.github/assets/39757235/0c2d14f2-ece3-46f7-a806-c047fcbe55f2)


### 기술적 의사결정

| 선택 기술 | 선택이유 및 근거 |
| --- | --- |
| Github Actions | - 지속적인 통합/지속적인 배포 (CI/CD) 구축을 통해 효율적이고 일관된 배포 및 테스트 프로세스를 구현하고자 함



### 프로젝트 주요 기능

시연 영상
1. 경기 생성
https://github.com/fms-chukguwang/.github/assets/39757235/3f58b40c-07f0-432f-8ddf-2cb969f0847b

2. 경기 이메일 수락
https://github.com/fms-chukguwang/.github/assets/39757235/279991ba-c77d-4dfd-b00d-b00c5d8f8e2f

3. 경기 전술 설정
https://github.com/fms-chukguwang/.github/assets/39757235/9760a34f-b461-45c9-9450-603f295dc96f


1. **팀 관리**
![2](https://github.com/fms-chukguwang/.github/assets/39757235/d55ebd53-ea01-42df-a7d7-d487c83f7c86)


2. **선수 및 통계 관리**
![3](https://github.com/fms-chukguwang/.github/assets/39757235/7c588357-66c4-498e-a554-e6514e6686fd)


3. **일정 및 전술 관리**
![4](https://github.com/fms-chukguwang/.github/assets/39757235/e69d85eb-4bfd-400c-9acc-f2c13d35cc8a)

4. **경기 결과 관리**
![5](https://github.com/fms-chukguwang/.github/assets/39757235/baeaf529-524b-4406-b389-d2577ef17cc2)

5. **채팅 및 실시간 알림**
![6](https://github.com/fms-chukguwang/.github/assets/39757235/40eaf581-9cdb-4004-b5b5-786b4220fbea)

6. **어드민 페이지**
![7](https://github.com/fms-chukguwang/.github/assets/39757235/4123b4bf-82c2-42a4-bcb0-334b30189cce)

### 트러블 슈팅

- **1.사용자 데이터 안전 이슈**
   문제점: http의 사용
  
   해결방안: https를 사용해서 사용자 데이터 보안 강화
    
- **2. SQL 인젝션 이슈**
    
    문제점: sql 인젝션으로 민감한 정보 유출 우려. teamId에 0 OR 1=1 조건은 항상 true
 
    해결방안: SQL 인젝션을 방지하기 위해서는 사용자 입력을 쿼리 문자열에 직접 삽입하는 대신
    파라미터화된 쿼리를 사용
    
   
- **3. 멤버 검색 속도 이슈**
    
    문제점: 멤버 검색 할때 속도가 느림
    
    해결책: 인덱스를  써서 속도를 빠르게함
    
    관련 깃허브 리포지토리: https://github.com/fms-chukguwang/index-testing

    
- **4.파일로 로그 저장시 관리**
    
    문제점: 로그를 파일로 저장해서 관리의 어려움. 로그 파일을 사용하는 의미x
 
    해결방안: 로그를 Mongo db에 저장하도록 변경
    