---
layout: post
title: "Static and serverless with Jekyll and AWS Amplify"
---
# Moving from EC2
This site was hosted on an AWS EC2 instance running RHEL and Apache.
The Jekyll builds were performed locally with deployment of the static content
being managed via git hooks.

The git remote repository was located on the EC2 instance with git hooks used to
replace the static content being served by Apache with the latest website build.

# AWS Amplify
AWS Amplify allows me to manage the content of this site in much the same manner
but with builds being performed remotely. Amplify accesses the the repository of 
markdown hosted on Github and performs a new Jekyll build anytime changes are pushed.

# Thoughts
The performance has been disappointing: both builds and access to the website are slow.
Anytime changes are pushed to the repo, Amplify recreates the Jekyll build environment,
including download the necessary dependencies. This ends up leading to a massive 
increase in build and deployment turnaround time compared to the old setup on EC2.

The upside? A rich workflow that includes the ability to test and stage changes made to
the markdown without having to touch SSH is really appealing. I never have to worry about
updating the EC2 instance to cover security vulrerabilities, the odd chance that something
might have broken without me knowing.
