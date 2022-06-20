# freeform-api

入力フォームからメール配信までのアプリケーションロジック

## Work

ローカル開発時の起動方法など

app サーバー起動の場合

```zsh
perl -I ./local/lib/perl5 ./local/bin/morbo -l "http://*:3050" ./script/freeform.cgi
```

## Memo

### Environment

アプリケーションの全体像メモ - <https://docs.google.com/presentation/d/1dbeq_OUtOLlIBz8AsuaMdNOD0JPZGN0dP75L4ZhFiWk/edit?usp=sharing>

初動時の環境構築に関するメモ

ignore

```zsh
echo 'local' >> .gitignore
```

Perl

```zsh
echo '5.32.1' > .perl-version
echo "requires 'Email::Sender';" >> cpanfile
echo "requires 'Email::MIME';" >> cpanfile
echo "requires 'Email::Stuffer';" >> cpanfile
```

Module

```zsh
curl -L https://cpanmin.us/ -o cpanm
chmod +x cpanm
./cpanm -l ./local --installdeps .
```

Dir

```zsh
mkdir script
touch script/freeform
chmod +x script/freeform
```
