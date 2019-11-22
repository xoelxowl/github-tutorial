# github-tutorial
깃허브 사용법 튜토리얼

## 사용자 정보 설정
``` shell
$ git config --global user.name "example"
$ git config --global user.email example@example.com
```
## 깃허브에 SSH 키 등록하기
https://syung05.tistory.com/20

## 깃허브 repository fork하기
Beyond_Imagination github 에서 github-tutorial repository를 fork한다  
![No Image](/images/fork.png)

## 포크된 repository clone하기
본인의 계정으로 포크된 repository를 clone하여 로컬에 내려받는다  
![No Image](/images/clone_1.png)
![No Image](/images/clone_2.png)

## 이슈 생성하기
수정하기 전 필요한 수정내용에 대한 이슈를 생성한다  
![No Image](/images/create_issue_1.png)
![No Image](/images/create_issue_2.png)
![No Image](/images/create_issue_3.png)

## branch 만들기
수정을 위한 새로운 branch를 만든다  
![No Image](/images/branch.png)

## 수정하기
members.md 파일을 수정한다  
![No Image](/images/update.png)

## add 하기
수정한 members.md 파일을 git에 add한다  
![No Image](/images/add.png)

## commit 하기
수정한 내용을 commit 한다  
![No Image](/images/commit.png)

## push 하기
커밋한 사항을 본인의 repository에 push 한다  
![No Image](/images/push.png)

## pull request
본인의 repository에 올린 브랜치를 Beyond_Imagination repository에 합치기 위해 pull request 를 만든다  
![No Image](/images/pull_request_1.png)
생성시 repository와 branch가 제대로 설정되었는지 확인한다. 확인후 본인이 원하는 pr 의 title 과 pr에 대한 설명을 적는다. pr 작성이 완료 되었을시 오른쪽에 있는 Reviewers에 원하는 사람들을 등록하고 Assignees 에 본인, labels 에 pr이 해당하는 label들을 등록한다. 모두 등록 한 후 create pull request 버튼을 눌러 pr 을 만든다
![No Image](/images/pull_request_2.png)
생성이 완료된 pr 을 확인할 수 있다.
![No Image](/images/pull_request_3.png)

## pr review
다른 사람들이 본인에게 pr review를 요청 할 수 있다. pr review를 요청 받았을 경우 성심성의껏 다른 사람의 코드를 확인하고 문제가 생길 수 있는 부분이 있는지 확인한다.
문제가 있을경우 comment 를 남기고 없을 경우 approve를 하면된다.
![No Image](/images/pr_review_1.png)
![No Image](/images/pr_review_2.png)

## pr merge
reviewer에게 approve를 받으면 merge를 할 수 있다. merge 시에는 Squash and merge를 이용한다
![No Image](/images/merge_1.png)
merge시 원하는 메시지를 입력한다. 그 후 이메일을 확인하고 Squash and merge 버튼을 클릭한다
![No Image](/images/merge_2.png)
merge 완료 후에는 Delete branch를 이용하여 pr을 마무리 한다
![No Image](/images/merge_3.png)

## upstream 추가
로컬의 master branch와 개인 repository의 master branch의 최신화를 위해 upstream 을 remote에 추가한다
![No Image](/images/upstream.png)
``` shell
git remote add upstream git@github.com:Beyond-Imagination/github-tutorial.git
```

## pull upstream
로컬의 최신화를 위해 upstream repository에 있는 최신 데이터를 가져온다 이때 현재 branch는 master branch 이어야 한다.
![No Image](/images/refresh_local.png)