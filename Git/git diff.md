#  Command [[git diff]] :

***

## About:

### - show differents in files between commits
***


## Use Cases:

### - use show difference (row was deleted)
```sh
[bohdan@fedora gittest]$ git diff Dockerfile
diff --git a/Dockerfile b/Dockerfile
index 8d72e40..f29b675 100644
--- a/Dockerfile
+++ b/Dockerfile
@@ -1,5 +1,4 @@
 FROM python
-
 WORKDIR /app/bot
 COPY . .
 RUN pip install -r requirements.txt
[bohdan@fedora gittest]$ 
```

### - use to 
```sh

```


## Keys:
```sh

```

### --help
```sh

```

***

## [[category]]

***
