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

## Node And Webpack Integration

1. install webpack-dev-middleware(only for development)

webpack-Middleware only serves to intercept incoming requests and hand it off to webpack.  
webpack exists to compile all of our app assets, and webpackConfig is what instructs webpack on how to run correctly.  


```
npm install --save-dev webpack-dev-middleware
```

2. deploy for EB

```
brew install awsebcli
```

```bash
eb init
# select a default region
# Enter AWS Credentials
# Enter Application Name
# 
```
```bash
# provisioning apps
eb create
```
```bash
# set the environment variable
eb setenv NODE_ENV=production
```

```bash
# kill the entire environment 
eb terminate
```