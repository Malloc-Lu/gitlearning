# git commend

### Modify

查看具体的修改

```shell
git diff filename.txt
```

撤销修改

- 修改了文件，但是还没有`git add`和`git commit`

  ```shell
  git checkout -- filename.txt
  ```

- 修改了文件，执行了`git add`

  执行下面命令，撤回暂存区的修改，重新放回工作区。

  ```shell
  git reset HEAD filename.txt
  ```

  再执行上面的命令。

  ```shell
  git checkout -- filename.txt
  ```

----

**<mark>`git`为分布式版本控制系统，如果把错误的修改提交到远程版本库，就很难修改了！！</mark>**

### Version traceback

查看从近到远的提交日志

```shell
git log
```

回退到上一个版本

```shell
git reset --hard HEAD^
```

> 一个^代表一个版本，上上个版本就是HEAD^^。
>
> 往上100个版本可以写成HEAD～100。

回退到一个具体的版本

```shell
git reset --hard version_code
```

`version_code`可以在日志中查看。

也可以通过下面这条命令查看。

```shell
git reflog			# 记录你的每一次命令
```

