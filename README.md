## Deployment for S3

1. install s3-website
```
npm install -g s3-website
```

2. create bucket by the packege

```
s3-website create [your-bucket-name]
```

3. deploy directory to the bucket

```
s3-website deploy dist
```

## Deployment for github-pages

git hub makes use of a very specially-named branch called "gh-pages"
Automatically served on https://[ Username ].github.io/< RepoName >

1. create branch & push the bundled assets dir into gh-pages
```
git subtree push --prefix dist origin gh-pages
```