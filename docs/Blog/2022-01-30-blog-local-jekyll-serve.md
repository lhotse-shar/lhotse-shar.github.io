---
layout: post
title:  "로컬에서 jekyll 블로그(github.io 블로그) 돌려보기 on Windows"
parent: Blog
nav_order: 1
---

* content
{:toc}

<br>

# 요약
1. 루비 설치
2. gem으로 필요한 패키지 설치
3. bundle install을 통해 gemfile내 패키지들 설치하기
4. 로컬서버 실행

<br>
<br>

# 1. 루비 설치

루비 설치는 [홈페이지](https://rubyinstaller.org/downloads/archives/) 에서 본인이 원하는 버전을 다운받으면 된다. <br>

본인은 2.5.5-1 버전을 다운로드했다. <br>
(Gemfile에서 jekyll 은 4.0.0 이상이 필요해서 루비가 2.5이상 버전이 필요했고, public_suffix가 4.0.3 가 필요해서 루비가 2.7이하 버전이 필요했다.) <br>

![1_1_download_ruby_version](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/18d270c7-b452-4ab1-912c-62b4c5e4bbdd) 

<br>
<br>

# 2. gem으로 필요한 패키지 설치

gem은 루비에서 패키지를 관리하는 툴이다. (파이썬에서 pip 느낌) <br>

필요한 패키지 설치에 앞서, 루비 전용 프롬프트를 설치해서 진행해야한다. <br>

![2_1_run_command_prompt_with_ruby](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/d390c783-abf1-42ca-a136-cc3a6680472f)

<br>

![2_2_run_command_on_ruby_prompt](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/9137e217-4de8-477c-8340-7d073131d20b)
<br>

그리고 ***<span style="color:rgb(201, 0, 22)"> git repository 경로에서 패키지 설치를 진행 </span>*** 해야한다.

필요한 패키지 설치 리스트는 다음과 같다. <br>
1. \> gem install jekyll
2. \> gem install bundler

<br>
<br>

# 3. bundle install을 통해 gemfile내 패키지들 설치하기

git repository 경로(gemfile 있는 경로)에서 bundle install 실행하면, 쭉 설치되고, 에러가 나면 메세지에 따라 해결한다.

![3_1_install_gem_packages](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/685bfba9-83f3-42c0-b74e-b520f614aecb) 

<br>
<br>

# 4. 로컬서버 실행

git repository 경로에서 다음 명령어 실행 <br>

> ```shell
> F:\Workspace\github\dayday-kim-101.github.io> bundle exec jekyll serve --port 5000 --trace 
> ```

<br>

포트는 기본 포트보다 5000번을 추천합니다. 4000번이 기본인데 이상하게 어떤 프로세스가 잡고있는지 서버가 뜨질 않았다. <br>

![4_1_run_local_jekyll_server](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/9c1f37d9-5e4a-4d02-b703-e66ff9dc2dfd)

<br>

http://127.0.0.1:5000 로 들어가면 다음과 같이 접속된다. <br>
(이렇게하면, push 안하고도 결과를 바로 확인 할 수 있다.) <br>

![4_2_result_run_local_jekyll_server](https://github.com/lhotse-shar/lhotse-shar.github.io/assets/134792669/e7a2fafd-0b9a-4e36-94ba-43dbdac1bde7)

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