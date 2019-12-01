---
title: vim
date: 2019-11-17 15:59:47
thumbnail: /image/post/vim.png
categories:
- 02_언어
- vim

tags: 
- vim

---

vim에디터는 터미널에서 파일을 수정할수 있는 좋은 도구입니다 하지만 터미널에서 수정을 한다는것 자체가 어색한 일이고 자주 쓸일이 없다보니 .. 사용을 안하게 되는것이 사실입니다 

본 포스팅에서는 vim에디터의 방대한(?) 명령어를 레벨별로 이해할 수 있도록 추려볼가 합니다 


![vim단축키극혐 -_-;;]( /image/post/vim-cheat.png )

현재이 블로그는 구름ide컨테이너를 ssh로 접속해서 작성을 하고 있습니다 
ssh 접속방법이 궁금하다면 [링크](https://youtu.be/JslmImgP4Os) 

**레벨1**
상황: 터미널로만 접속해서 오타수정을 살짝하고 저장해야하는경우 

**vi [파일명]
i : insert 모드
esc > :wd > enter**

![vim사용법 레벨1]( /image/post/gif/vimlevel1.GIF)



**레벨2**
상황 : 라인을 확인해서 수정을 해야하함
문제가 생기면 undo도 해야함
복사해서 붙여넣기를 햐야할 소스가 있음

vim라인 표시해주는 명령어
```markdown
:set number 
# 또는
:set num
```

원하는 라인으로 이동
```markdown
:[라인숫자]
```
u : undo

복사해서 붙여넣기
v : 복사하고 싶은 범위 선택( 방향키로 선택 가능 )
y : 복사하기 ( c : 잘라내기 )
p : 붙여넣기

![라인표시&라인으로이동](/image/post/gif/vimlevel2-1.GIF)


![복사&붙여넣기](/image/post/gif/vimlevel2-2.GIF)

**레벨3**
1. 검색해서 필요한 부분만 변경
1. 한줄 선택줄잘라내서 붙여넣기
1. 실행취소 재실행
1. 저장하지 않고 닫기

/[찾으려는단어] : n N 으로 단어사이 이동
V > c > p & dd > p: 한줄잘라내서 붙여넣기
u & ctrl + r : 실행취소 & 재실행
:q! : 저장하지 않고 닫기






