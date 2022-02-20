# UpStarMusic
Starter Repo for a Webpack course on Udemy

You can download this repository by using the green `Clone or Download` button on the right hand side of this page.  This will present you with the option to either clone the repository using Git, or to download it as a zip file.

If you want to download it using git, copy paste the link that is presented to you, then run the following at your terminal:

```
git clone https://github.com/StephenGrider/WebpackProject.git
cd WebpackProject
npm install
```

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
