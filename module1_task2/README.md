## Prerequisites:
    - sudo apt install hugo
    - hugo new site quickstart
    - cd quickstart
    - git init
    - git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
    - echo "theme = 'ananke'" >> config.toml
    - hugo server

## Lifecycle:
    - hugo
    - hugo server -D
    - Clean:
        The clean target removes any generated files and restores the repository to its original state.
    - build:
        The build target generates the website based on the repository settings.
    - post:
        The post target creates a post inside of our website.
    - help:
        The help target generates a help screen.