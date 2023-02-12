# Git超入門

## git init

### ディレクトリを作って移動

```
mkdir techtechkochi_git
cd techtechkochi_git
```

### gitを初期化する

```
git init
```

### 作成されたディレクトリを確認

```
ls -la
```

## git add

```
touch sample.txt
git add sample.txt
```

## git diff

### 差分を確認

```
echo '初めてのdiff' > sample.txt
git diff
```

### stagingエリアに上げた差分を確認

```
git add sample.txt
git diff --cached
```

## git status

### ワーキングツリーの状態を表示する

```
touch sample2.txt
git status
```

```
git add sample2.txt
git status
```

## git restore

### stagingエリアに上げた変更を取り消す

```
git restore --staged sample2.txt
git status
```

下記でもできる
```
git rm --cached sample2.txt
```

```
git reset sample2.txt
```

## git commit

```
touch commit.txt
echo '初めてのコミット' > commit.txt
git status
git add commit.txt
git status
git commit -m '初めてのコミット'
```

## git log

### コミットを振り返る

```
git log
```

## git show

### コミットの中身を確認する

```
git show
```

### 特定のコミットの中身を確認する

```
git show <commit-hash>
```

## git reset

### 直前のコミットを削除する

```
touch dame_commit.txt
git add dame_commit.txt
git commit -m 'ほんとはコミットしちゃダメなやつ'
git reset --hard HEAD^
git log
```

### 特定のコミットまで戻す

```
git reset --hard <commit-hash>
git log
```

## git remote

### リモートリポジトリとローカルリポジトリを紐付ける

```
git remote add origin https://github.com/<username>/<repository_name>.git
git remote -v
```

## git branch

### 今いるブランチ名を変更する

```
git branch -M main
```

### ローカルリポジトリのブランチ一覧を表示

```
git branch
```

## git push

### ローカルリポジトリで用意した修正をリモートリポジトリに追加する

```
git log
git push origin main
```

## git switch

### ブランチ作成と移動をする

```
git switch -c first_branch
```

### 下記でもブランチ作成可能

```
git branch first_branch
git switch first_branch
```

```
git checkout -b first_branch
```

### すでにあるブランチに移動する場合

```
git switch main
```
