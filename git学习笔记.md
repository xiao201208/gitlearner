##### д��ǰ��
- [��ҳѧϰgit](https://try.github.io/levels/1/challenges/1)
- ���ĵ���ѧϰ [��ѩ��Git�̳�](http://t.cn/zQ6LFwE) �������ıʼǣ��̳̰�æ�ܴ󣬷ǳ���л��
- ���ʼ���Ҫ��¼�˽̳������õ�����������ݲ��������ڡ�
- ���鿴��̳̺��ٿ�Git������ [Pro Git](https://git-scm.com/book/zh/v2) һ�顣
- ����ϱ��˵� [GitHub](https://github.com/caozhiqiango) ����л���߷���׾��,���븫����

##### �����汾��
```
git init  #��ʼ������Ŀ¼ΪGit�ֿ�
```
> ��ʼ����Ŀ¼���Բ�Ϊ��

##### ����ļ����汾��
```
git add <file> ...  #����ļ����ݴ�����stage��
        -f <file> ...  #ǿ����ӵ��ݴ�������������Ӻ����ļ���
git commit -m "�ύ˵��"  #���ݴ����ύ���汾��
```
> git add ����ɶ��ִ�У�Ȼ��commitһ�Ρ�

##### ʱ�������
- �鿴״̬������

```
git status  #�鿴�ֿ⵱ǰ״̬
git diff [file]  #�ȽϹ��������ݴ����Ĳ���
git diff --cached [file]  #�Ƚ��ݴ����Ͱ汾��Ĳ���
git diff HEAD -- [file]  #�ȽϹ������Ͱ汾��Ĳ���
```
- �汾�л�

```
git log  #�鿴�ύ��ʷ
git log -1  #�鿴���һ���ύ��Ϣ��-2 ����������Σ�
git log --pretty=oneline  #���и�ʽ��ʾ�ύ��ʷ
        --graph  #��ʾ��֧�ϲ�ͼ
        --abbrev-commit  #��д��commit_id
git reflog  #�鿴���в�����¼������ɾ����commit��¼
git reset --hard HEAD^  #���˵���һ�汾
# HEAD ��ǰ�汾�� HEAD^ ����һ�汾��HEAD^^ �������汾��HEAD~99 ����99�汾��
git reset --hard commit_id  #�л���ָ���汾
```
> Git���ٹ�������޸ģ������ļ�

- �����޸�

```
git checkout -- <file>  #�������������޸�
git reset HEAD <file>  #�����ݴ������޸�
```
> ����commit��û�ύ��Զ�̿⣬���ð汾���˽��г���

- ɾ���ļ�
  - ����һ��������ɾ���ļ���Ȼ�������ύ
  
  ```
  rm <file> ...  #������ɾ��
  git add <file> ...  #���޸��ύ���ݴ���
  git commit -m "˵��"  #�ύ���汾��
  ```
  - ��������ֱ������ɾ�����������ݴ�����Ȼ���ύ�汾��
  
  ```
  git rm <file> ...  #ɾ�����������ݴ����ļ�
  git commit -m "˵��"  #�ύ���汾��
  ```
> ɾ���������ļ�Ҳ�������޸�

##### Զ�ֿ̲�
- ����SSH Key

```
ssh-keygen -t rsa -C "youremail@example.com"  #���ɵ�Key�ڼ�Ŀ¼.ssh�ļ������棬pub��׺�ǹ�Կ����һ����˽Կ��
```

- ���Զ�̿�

```
git remote add origin git@server-name:path/repo-name.git  #���Զ�ֿ̲�
git remote  #�鿴Զ�̿���Ϣ
           -v  #��ʾ��ϸ��Ϣ
git push -u origin <branch>  #���Ͳ�����ָ����֧��Զ�̿�
```
> ����һ�ι�����֮��push���ü�-uѡ��

- ��Զ�̿��¡

```
git clone git@server-name:path/repo-name.git  #��Զ�ֿ̲��¡����ǰĿ¼
git pull  #��ȡԶ�ֿ̲�����
```

##### ��֧����
```
git branch <branch>  #������֧
git checkout <branch>  #�л���ָ����֧
git checkout -b <branch>  #�������л����÷�֧
git branch  #�鿴���з�֧
git branch -d <branch>  #ɾ��ָ����֧
git branch --set-upstream <branch_local> <branch_remote>  #ָ�����ط�֧��Զ�̷�֧������
git merge <branch>  #�ϲ�ָ����֧����ǰ��֧
          --no-ff <branch>  #���ÿ��ٺϲ�
git merge --no-ff -m "�ύ˵��" <branch>  #��ͨ��ʽ�ϲ��������ύ˵��
git stash  #���浱ǰ�����������������������ݴ�����
git stash list  #�鿴����Ĺ����б�
git stash apply [stash@{X}]  #�ָ�����״̬������ɾ��stash����
git stash pop [stash@{X}]  #�ָ�����״̬����ɾ��stash����
git stash drop [stash@{X}]  #ɾ��stash����
git branch -D <branch>  #ǿ��ɾ����֧��������δ�ϲ��ķ�֧��
```
> HEAD����ֱ��ָ���ύ�㣬����ָ���֧����֧��ָ���ύ��

- ����Э��

```
##error: failed to push some refs to ...
1. git pull Զ�̿�
2. �����ͻ�����У�����push
```

- ��֧�������ͼ

![image](http://www.liaoxuefeng.com/files/attachments/001384909239390d355eb07d9d64305b6322aaf4edac1e3000/0)

##### ��ǩ����
```
git tag  #�鿴���б�ǩ
git tag <tag_name>  #����ǰ���ڵ�commit���ǩ
git tag <tag_name> <commit_id>  #��ָ��commit���ǩ
git tag -a <tag_name> -m "��ǩ˵��" <commit_id>  #��ָ��commit���ǩ������˵��
        -s <tag_name> -m "��ǩ˵��" <commit_id>  #��gpg˽Կǩ��
        -d <tag_name>  #ɾ����ǩ
git show <tag_name>  #��ʾ��ǩ��Ϣ
git push origin <tag_name>  #���ͱ�ǩ��Զ�̿�
git push origin --tags  #��������δ���͵ı�ǩ��Զ�̿�
git push origin :refs/tags/<tag_name>  #ɾ��Զ�̱�ǩ����ɾ�����أ���ʹ�ø�����ɾ����
```

##### �Զ���Git
```
git config --global user.name "you_name"  #����ȫ���û���
git config --global user.email "email@example.com"  #����ȫ������
git config --global color.ui true  #����ȫ����ɫ��ʾ
git config --global alias.<alias_name> <'command_name'>  #���ñ���
```
- ���������ļ�

  1. ����������`.gitignore`�ļ�
  2. ���ݾ��������£�

  ```
  #Windows:
  Thumbs.db
  ehthumbs.db
  Desktop.ini

  #Python:
  *.py[cod]
  *.so
  *.egg
  *.egg-info
  dist
  build
  #My configurations:
  db.ini
  deploy_key_rsa
  ```

```
git check-ignore -v <file>  #�鿴���Ը��ļ��Ĺ���
```
> �����д�ʱ��������������Ҷ�λ

- ���ñ����б�

```
git config --global alias.confg 'config --global'
git confg alias.st status
git confg alias.co checkout
git confg alias.ci commit
git confg alias.br branch
git confg alias.unstage 'reset HEAD'
git confg alias.last 'log -1'
git confg alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
- �Git������ [�̵̳�ַ](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137583770360579bc4b458f044ce7afed3df579123eca000)