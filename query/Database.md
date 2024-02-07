# Databaseそのものに対するクエリ

## データベース作成

```sql
CREATE DATABASE [データベース名];
```

以下のようにDatabaseに対するOWNER、エンコード、最大コネクション数は最低指定すること。

```sql
CREATE DATABASE SampleDatabase
    WITH
    OWNER = adam
    ENCODING = 'UTF8'
    CONNECTION LIMIT = -1
    IS_TEMPLATE = False;
```

## データベース削除

```sql
DROP DATABASE IF EXISTS [データベース名];
```

IF EXISTSはオプションだが、SQLエラーを避けるために基本的には付与する。
データベース削除はデータベースのOWNERもしくはスーパーユーザーのみが実行できる。