---
layout: post
title: "Still static and serverless with Github Pages"
---
# Why move?
I'm now using Github Pages to host this site. Performance on Amplify
was too slow, builds were even slower. Github Pages allows for a near
identical workflow, but without the aforementioned issues.

The transition was very smooth. All that needed to be done was:
1. Rename the repository to make it a Github Pages repo.
2. Specify a Custom Domain in the repository Settings on Github.
3. Replace the CNAME in the Namecheap settings to point to the new page.
4. Wait for the HTTPS certificates to be generated after the DNS changes
have propagated.

So here we are, still static and serverless, enjoying all of the benefits
that come with that.
