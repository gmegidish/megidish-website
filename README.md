#### Megidish.net

This repo has all code for megidish.net website. Forever a work-in-progress.

Deploy with:
```
aws s3 sync --acl public-read --exclude README.md --exclude .gitignore --exclude ".idea/*" --exclude ".git/*" --exclude .gitmodules . s3://megidish.net/ 
aws configure set preview.cloudfront true
aws cloudfront create-invalidation --distribution-id E1WFTDMWWGU12N --paths '/*'
```

