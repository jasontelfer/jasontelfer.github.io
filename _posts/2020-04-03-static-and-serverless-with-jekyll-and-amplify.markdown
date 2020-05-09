---
layout: post
title: "Static and serverless with Jekyll and AWS Amplify"
---
# Moving from EC2
The first iteration of this site was hosted on an EC2 instance running Apache.
The Jekyll builds were performed locally with deployment of the static content
being managed via git hooks.

The git remote repository is located on the EC2 instance with git hooks used to
replace the static content being served by Apache with the latest website build.