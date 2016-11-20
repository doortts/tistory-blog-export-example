tistory backup 이동 샘플
---

https://github.com/doortts/tistory-backup-extractor 를 이용해서 github wiki 로 백업을 이동시킨 샘플

See: https://github.com/doortts/tistory-blog-export-example/wiki


이동방법
---

- github 에 프로젝트를 하나 만듭니다. 지금은 tistory-blog-export-example 라고 가정하겠습니다.
- wiki 메뉴로 이동해서 New Page 생성을 누르고 바로 저장합니다. (내용무관)
- 이제 Home 파일이 생성되고 우측 하단쯤에 git 주소가 보입니다.

```
예) https://github.com/doortts/tistory-blog-export-example.wiki.git
```

로컬에서 git clone 을 실행합니다.

```
git clone https://github.com/doortts/tistory-blog-export-example.wiki.git wikida

```

- 이제 tistory-backup-extractor 를 이용해서 tistory backup 파일을 분해합니다.
  - https://github.com/doortts/tistory-backup-extractor  를 참조

- tistory-backup-extractor 를 사용하면 하위로 blog 폴더가 생깁니다.

해당 폴더로 커맨드 라인으로 이동합니다.

```
cd blog
```

- 이제 아까 생성한 github 프로젝트(https://github.com/doortts/tistory-blog-export-example.wiki.git)로 파일들을 추가해서 넣습니다. 
   - git remote add 할때 주소 지정 유의!!

예)
```
git init
git add .
git commit -m 'Move move~'
git remote add https://github.com/doortts/tistory-blog-export-example.wiki.git origin
git push origin master -u -f

```

이제 https://github.com/doortts/tistory-blog-export-example/wiki 로 가서 확인해 봅니다.

