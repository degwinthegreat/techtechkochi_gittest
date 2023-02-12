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
