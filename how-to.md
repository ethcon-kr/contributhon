---
layout: page
title: /how-to
permalink: /how-to/
---

1. Accomplish contribution by the contributhon guide line

    [Contributhon guide line - Korean ver](https://docs.google.com/presentation/d/15dLVXqLfTVABvEF6S3F4JvTECIDFfGhQfqyyAyCiTXo/edit#slide=id.g60773feab9_1_0)

1. Fork this repository & clone it

    ```shell
    git clone https://github.com/YOUR_GITHUB_ID/contributhon
    cd contributhon
    ```

1. Choose right template according to the kind of your contribution and copy it to `_posts` directory. You must name it with the following format `YYYY-MM-DD-TITLE.md`.
    ```shell
    cp _templates/bounty-hunt.md _posts/2019-09-08-status-issue-38.md
    vim _posts/2019-09-08-resolve-status-issue-38.md
    ...
    ```

1. Commit and [make PR](https://github.com/ethcon-kr/contributhon/pulls) to the `master` branch when you complete to fill out the template
