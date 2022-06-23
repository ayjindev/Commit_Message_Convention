# Git Commit Message Convention

---

# Git : Commit Message Convention

**[Github commit 메세지 규칙의 필요성](about:blank#28af4853-e183-4daf-893c-55c627622097)**

**[좋은 git 커밋 메시지를 작성하기 위한 7가지 약속](about:blank#ed6258b8-a6b3-4435-b89a-1bb425dd6803)**

**[커밋 메시지 구성](about:blank#fa8fe5aa-f510-4016-944e-51e4238b895e)**

[Header](about:blank#b3e98d2a-064e-4bd6-b476-895d99e88a55)

[Body](about:blank#c6162e8a-5f62-45f8-a564-cccab447308b)

[Footer](about:blank#7a34bbee-da53-4a52-b868-c376cefff0b7)

**[예시](about:blank#72b30983-2b52-409f-8e9c-0fe087b5bef1)**

**[Commitlint-bot 붙히기](about:blank#3b56f227-8b20-4825-b3a8-d699f501497e)**

**[Reference](about:blank#f90bfc2b-95f1-4b78-940b-7aef2cbb1359)**

# **Github commit 메세지 규칙의 필요성**

일단 commit 메세지 규칙의 필요성에 대해 공감이 이루어져야 잘 지켜질 것 같아서 규칙의 필요성을 정리해보았습니다.

- 팀원과의 소통
- 편리한 과거의 기록 추적
- 이슈를 함께 작성하면서 이슈와 관련된 진행 사항을 확인 가능

# **좋은 git 커밋 메시지를 작성하기 위한 7가지 약속**

> 이하 약속은 커밋 메시지를 English로 작성하는 경우에 최적화되어 있습니다. 한글 커밋 메시지를 작성하는 경우에는 더 유연하게 적용하셔도 좋을 것 같네요.
> 

```
   제목과 본문을 한 줄 띄워 분리하기
   제목 첫 글자를 대문자로
   제목은 영어 50자 이내 (한글은 25자 이내)
   제목 끝에 마침표(.) 금지
   제목은 명령문으로 (적용 시, 이 커밋은 <커밋 메시지> 합니다)
   본문은 영어 72자 마다 개행 (한글은 36자 마다)
   본문은 "어떻게" 보다 "무엇을", "왜"를 설명한다.
   본문에 여러줄의 메시지를 작성할 땐 "-"로 구분
```

# **커밋 메시지 구성**

모든 커밋 메시지는 다음과 같이 **세 영역으로 구성**되며, 각 영역은 **빈 줄로 분리**된다.

## Header

- 헤더는 **50자 내로 작성**한다.
- 헤더는 **"태그: 제목"의 형태이며, : 뒤에만 space가 있음에 유의**
    
    ```
    <태그>: <제목>
    ```
    
- 제목은 **개조식 구문으로 작성**한다.
    
    > 개조식 구문 : 완전한 서술형으로 문장을 종결하는 것이 아니라 간결하고 요점적인 단어로 서술되는 문장형태로서, 내용을 길게 풀어서 표현하지 않고 중요하고 핵심적인 요소만 간추려 항목별로 나열하듯이 표현하는 방식- 국립국어원 -
    > 
- 제목 뒤에 특수문자는 삽입하지 않는다. (마침표도 쓰지 않는다)
- 태그는 영어로 쓰되 첫 문자는 대문자
- 주요 <태그> 리스트
    
    ```
    Feat    : 기능 (새로운 기능)
    Fix     : 버그 (버그 수정)
    Refactor: 리팩토링
    Style   : 스타일 (코드 형식, 세미콜론 추가: 비즈니스 로직에 변경 없음)
    Docs    : 문서 (문서 추가, 수정, 삭제)
    Test    : 테스트 (테스트 코드 추가, 수정, 삭제, 리팩토링: 비즈니스 로직에 변경 없음)
    Chore   : 기타 변경사항 (빌드 스크립트, 패키지 매니저 설정 수정 등)
    ```
    
- 기타 <태그> 리스트
    
    ```
    Design  : CSS 등 사용자 UI 디자인 변경
    !BREAKING CHANGE : 커다란 API 변경의 경우
                      (ex A PI의 arguments, return 값의 변경, DB 테이블 변경, 급하게 치명적인 버그를 고쳐야 하는 경우)
    !HOTFIX : 급하게 치명적인 버그를 고쳐야하는 경우
    Comment : 필요한 주석 추가 및 변경
    Rename  : 파일 혹은 폴더명을 수정하거나 옮기는 작업만인 경우
    Remove  : 파일을 삭제하는 작업만 수행한 경우
    ```
    

## Body

- 본문은 제목 만으로 표현이 가능할 때에는 생략 가능
- 여러줄 작성시 필요에 따라 ‘-’ 표기
- 본문은 **한 줄 당 72자 내**로 작성한다.
- 본문 내용은 양에 구애받지 않고 **최대한 상세히 작성**한다.
- 본문 내용은 어떻게 변경했는지 보다 **무엇을 변경했는지** 또는 **왜 변경했는지**를 설명한다.

```
본문
- 소기능1
- 소기능2
```

## Footer

- 꼬리말은 이슈 트래킹을 위함 (관련 이슈가 없으면 생략 가능)
- **"태그: #이슈번호"의 형태이며, : 뒤에만 space가 있음에 유의**
- 여러개의 이슈번호를 적을때는 쉼표로 구분

```
<태그>: #<이슈번호>
```

- 주요 <태그> 리스트
    
    ```
    Resolves   : 이슈를 해결했을 때 사용
    Ref        : 참고할 이슈가 있을 때 사용
    Related to : 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)
    Fixes      : 이슈 수정중 (아직 해결되지 않은 경우)
    ```
    

```
Resolves: #123
Ref: #456
Related to: #48, #45
```

## **예시**

```
feat: 패킷 송신 이벤트에 관련된 로그 출력 기능 추가

커밋에 대한 자세한 설명
- 커밋에 대한 더욱 자세한 설명1
- 커밋에 대한 더욱 자세한 설명2

Resolves: #123
Ref: #456
Related to: #48, #45
```

# **Commitlint-bot 붙히기**

여러 팀원들과 같이 프로젝트를 진행할때 나말고 다른 사람들이 commitlint를 맞추지 않다면 아무런 소용이 없을 겁니다. 프로젝트에 commitlint-bot을 붙혀 이러한 문제점들을 해결해보세요.

[commitlint-bot](https://github.com/kooku94/commit-message-guide/blob/master/commitlint-bot.md)

# **Reference**

- [좋은 git 커밋 케시지를 작성하기 위한 7가지 약속 :: TOAST Meetup!](https://meetup.toast.com/posts/106)
- [Udacity Git Commit Message Style Guide :: udacity](https://udacity.github.io/git-styleguide)
- [Git 사용 규칙 - Git commit 메시지 :: h3ngss0](https://tttsss77.tistory.com/58)
- [커밋 메시지 가이드 :: RomuloOliveria](https://github.com/RomuloOliveira/commit-messages-guide/blob/master/README_ko-KR.md)
- [style-git-commit-message :: slashsbin](https://github.com/slashsbin/styleguide-git-commit-message)