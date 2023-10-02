Hi, I'm Marcello Novak.

I'm currently a college freshman at ERAU prescott, majoring in Computer Engineering Robotics.

Here's a brief list of the things I like to tinker with:\
&emsp; - Arduino Microelectronics and creating my own projects from scratch\
&emsp; - Designing, wiring, and soldering PCBs for my Arduino projects\
&emsp; - Designing parts for/using my 3D printer\
&emsp; - Intermediate stuff using Python, JavaScript, SQL, and C++\
&emsp; - Discord Bots and other APIs\
&emsp; - Linux/VMs and running a Minecraft server on a dedicated machine using Ubuntu\
&emsp; - GNS3/Wireshark/Putty once in a while, I took Cisco CCNA/CCNP in high school

Feel free to sift through the snippets of code I've posted on here!

- uses: Platane/snk@v3
  with:
    # github user name to read the contribution graph from (**required**)
    # using action context var `github.repository_owner` or specified user
    github_user_name: ${{ github.repository_owner }}

    # list of files to generate.
    # one file per line. Each output can be customized with options as query string.
    #
    #  supported options:
    #  - palette:     A preset of color, one of [github, github-dark, github-light]
    #  - color_snake: Color of the snake
    #  - color_dots:  Coma separated list of dots color.
    #                 The first one is 0 contribution, then it goes from the low contribution to the highest.
    #                 Exactly 5 colors are expected.
    outputs: |
      dist/github-snake.svg
      dist/github-snake-dark.svg?palette=github-dark
      dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9

  env:
    # a github token is required to fetch the contribution calendar from github API
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
