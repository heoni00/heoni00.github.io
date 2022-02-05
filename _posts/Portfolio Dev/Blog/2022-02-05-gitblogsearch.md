---
published: true
title:  "[Github Blog] 블로그 검색 등록" 
excerpt: "깃헙 블로그는 무엇이고 왜 쓰는 걸까?"

categories:
  - Blog
tags:
  - [Blog, Github]

toc: true
toc_sticky: true
 
date: 2022-02-05
last_modified_at: 2022-02-05

---

안녕하세요, 방문자 여러분. 허니테크입니다. 😊😊 이번 게시물은 깃블로그 검색 등록 과정을 고.스.란.히 담아보려 합니다. 그 과정이 상당히 고통스럽고 인내심이 필요했기 때문에 독백하듯 글을 작성하겠습니다 ㅎㅎ. 여러분에게 도움이 될만한 부분은 후에 정리해서 다시 올리도록 하겠습니다!!

-----

22년 1월 목표 중 하나가 내 피,땀 그리고 눈물이 담겨있는 내 소오중한 깃블로그를 검색엔진에 등록하여 방문자를 만드는 것이다. 많은 깃블로그가 구글, 네이버 등 검색엔진에 등록 되었기에 ,, 나 또한 남들이 한 방식대로 옴삭옴삭 진행하면 쉽게 등록할 줄 알았는데 벌써 이 짓만 ,, 2주째인 것 같다. 앞이 깜깜하고 또 코딩이라는 거대한 산에 부딪힌 것 같지만 ,, 내가 반드시 헤쳐나가서 남들이 내 블로그를 방문할 수 있도록 할 것이다. 컴퓨터는 논리적이고 거짓말을 하지 않는다. 즉! 문제의 원인을 힘껏 쳐다보고 그에 대한 해결 방법을 계란으로 바위치듯 계속 시도해 나간다면? 언젠간 해결할 것이다. 늘 그래왔듯. 나? 해내고 말 것이야. 

## 현재까지 진행했던 것들. 

1_ 가장 우선적으론 깃허브 블로그를 모두 완성하였다. 특히 config 파일에서 url를 정확하게 설정하였다. 

2_ 네이버, 다음 각각의 웹 마스터 도구에 내 블로그를 등록했다. -> 블로그 홈은 검색이 되지만 게시물 각각은 검색이 되진 않는다. (하지만 별 중요하지 않다.)

3_ 구글 검색 엔진에 깃헙 블로그를 등록하기 위해 3가지 파일을 만들었다. 

[**sitemap.xml**](https://github.com/heoni00/heoni00.github.io/blob/main/sitemap.xml), [**robots.txt**](https://github.com/heoni00/heoni00.github.io/blob/main/robots.txt), [**feed.xml**](https://github.com/heoni00/heoni00.github.io/blob/main/feed.xml) 각각은 검색 엔진에 자동으로 블로그 홈, 게시물 경로를 크롤링하여 연결해주는 역할을 하고 그것을 제어하는 역할을 수행한다. 각 파일에 대한 자세한 용도는 이해하진 않았다. 

4_ 각 파일에 대한 문제가 없다는 것을 확인했다. 

특히 [**sitemap.xml**](https://heoni00.github.io/sitemap.xml)파일은 서버 상으로 크롤링이 잘 되었는지도 확인하였다. 이 과정도 매우 고단했다. 우선 가장 중요한건 게시물 파일이름에 한글, 특수기호, 언더바, 띄어쓰기를 쓰지 않고 최대한 간단하게 커밋하는 것이다. 이 사실을 알기 위해 매우 고생했다 ^^

5_ 구글 웹마스터 도구 - 서치 콘솔에 내 heoni00.github.io url을 등록하였고 그 html 파일을 다운 받아 블로그 레파지토리 root파일에 커밋하였다. 

해당 파일이 커밋되서 잘 등록되는지 확인하는 방법이 있는데 ,, 나는 "127.0.0.1에서 연결을 거부했습니다."라고 떴다. 이게 문제일까? 하지만 서치 콘솔에는 블로그가 문제없이 등록된 것 같다. 

6_ 관리창에서 sitemaps부분에서 sitemap.xml을 제출했다! 근데 망했다. 

![image](https://user-images.githubusercontent.com/67791317/152639259-f3cff4e9-d9ce-4f46-b0a1-8d6a776e01a7.png){: .align-center}
![image](https://user-images.githubusercontent.com/67791317/152639278-b1f2f1e9-0e98-41e1-8dca-8a9a3af00d74.png){: .align-center}

구문분석!!!!! 구문분석 오류가 도데체 뭐길래 ,, 문제의 437행이 뭔지도 사실 잘 모르겠다. 이에 대해 구글 서치 콘솔 고객센터의 게시판에 질문을 올렸다. 언더바가 문제인 것을 확인했지만 해당 행을 정확하게 확인하는 방법은 알아내지 못했다. 

7_ 게시물 파일 이름을 모두 단순화하여 커밋하고 sitemap을 다시 제출했지만 여전히 해당행의 구문분석 오류가 뜬다. 











필요한 url 

https://yenarue.github.io/tip/2020/04/30/Search-SEO/
https://theorydb.github.io/envops/2019/05/11/envops-blog-tipue-search/
https://blog.slarea.com/git/blog/register-to-search/
https://sanghyuk.dev/blog/2/
https://mi-nya.tistory.com/188

