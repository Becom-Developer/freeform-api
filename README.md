# freeform-api

入力フォームからメール配信までのアプリケーションロジック

## Memo

### Environment

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
