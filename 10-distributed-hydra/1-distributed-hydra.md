!SLIDE
# Distributed Hydra

!SLIDE
# Hydra
### If you can ssh in to another machine and run your tests
### why can't it help?

!SLIDE
# SSH Messaging System

!SLIDE
# hydra.yml 
    @@@ yaml
    workers:
      - type: local
        runners: 4
      - type: ssh
        connect: user@example.com
        directory: /absolute/path/to/project
        runners: 4
    sync:
      directory: /my/local/project/dir
      exclude:
        - tmp
        - log

