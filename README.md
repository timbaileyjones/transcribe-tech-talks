<img src="https://github.com/stelligent/mu/wiki/img/mu.png" width="150">
<br/>

# Transcribing Tech Talks with `mu` on EC2

This project uses [mu-minimal-ec2](https://github.com/timbaileyjones/mu-minimal-ec2) as a starting point, which is documented in [another Stelligent Blog post](https://wordpress.com/post/stelligent.com/17746)


# Technologies used

# Prerequisites
  * An AWS Account
  * a Github Account
  * a Github Token - [create one here](https://github.com/settings/tokens)
  * Stelligent [`mu`](https://github.com/stelligent/mu) 
  * AWS Access keys set up in $HOME/.aws 

# Instructions

## Make your own repository
  * Fork this repository in github.
  * Clone your forked repository to your workstation:  

    `git clone git@github.com:<your-github-name>/transcribe-tech-talks.git`

  * Go to the newly cloned directory
    `cd transcribe-tech-talks`

  * Edit the `repo:` line 17 of `mu.yml`, to match your new repository's URL.
  * Commit and push your changes
    ```bash
    git commit -a -m "modify the repo: attribute in mu.yml" 
    git push 
    ```
  * Create the mu pipeline
    `mu pipeline up -t <your-github-token>`
