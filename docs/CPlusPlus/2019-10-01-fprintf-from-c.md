---
layout: default
title:  "C언어에서 fprintf(stderr, ... 구문 의미"
parent: C++
nav_order: 1
---

* content
{:toc}

<br>

# 요약
1. stderr 의미
2. stdxxx 의 출력 장치

<br>
<br>

# 1. stderr 의미

stderr은 에러메세지를 출력할 장치라는 뜻입니다. 그것이 기본적으로 스크린으로 설정되어 있을 따름이죠.

이것을 파일이라던가. 아니면 프린터라던가로 바꿔주면 바로 stderr 이 파일로 연결되어 에러메세지만 따로 출력이 가능하겠죠

같은 종류로 stdin stdout 이 있는데

기본값으로 stdin은 키보드 stdout 은 스크린으로 설정되어 있습니다.

stderr 과 stdout 이 모두 기본이 스크린으로 되어 있기 때문에 같이 화면으로 출력되는 것입니다.

<br>
<br>

# 2. stdxxx 의 출력 장치

**stderr**은 기본 출력장치인 모니터로 only연결되 있습니다.

stdin,stdout 같은경우는 명령어 프롬프트상에서 리디렉션을 이용해서 출력또는 입력을 재지정이 가능하지만 **stderr**은 리디렉션을 써도 모니터로 출력이 됩니다.

stdin 기본 입력장치(키보드) <br>
stdout 기본 출력장치(모니터) <br>
**stderr** 기본 출력장치(모니터) <br>
stdprn 프린터 <br>
stdaux 통신포트 <br>

그리고 파일닫을때 실패할 경우는 거의 없구요.. 하드에 용량이 부족할때나 실패할 겁니다.(파일을 열고 작업을 할때에는 메모리와 가상메모리상에서 하게 됩니다.)

<br>
<br>

# 3. fprintf 함수

『 printf() 함수는 무조건 표준 출력 장치 즉, 모니터로만 데이터를 출력할 수 있는 함수입니다.

그런데 **fprintf() 함수는 스트림을 지정해줄 수 있는 함수**입니다. 스트림을 표준 줄력 장치(모니터)로 지정하면 모

니터로 출려고되고 특정 파일로 지정하게 된다면 그 대상으로 데이터가 전송 되는 것입니다.

예를 들어 스트림을 파일로 지정하고 함수호출을 하게되면 데이터를 특정 형식에 맞춰서 파일에 저장하게 됩니다. 』 

<br>

---

<script src="https://utteranc.es/client.js"
        repo="lhotse-shar/lhotse-shar.github.io"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>