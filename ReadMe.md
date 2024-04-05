# Description #

NGINX Docker. Make is easy to run a custom nginx locally to associate simple host names to internal web applications running on a local system or network.

# Instructions #

1.  Clone repository - use one of these methods:
    * With a git client: `cd ~/docker && git clone https://bitbucket.org/bob_swift/nginx nginx`
    * With Sourcetree enabled: Go to https://bitbucket.org/bob_swift/nginx and clone to `~/docker/nginx`
1.  `cd nginx`
1.  Customize __nginx.conf__.
1.  Add server names to **etc/hosts** - on OSX use `sudo nano /private/etc/hosts` or equivalent. Example addition: 127.0.0.1 example.examplegear.com
1.  Customize html/index.html (optional).

# Operations #

1.  `./up`        - when instance is needed
1.  `./down`      - when done
1.  `docker ps`   - docker status

# Notes #

*  Restart the container after any configuration changes
*  Access: **http://localhost**
*  Debug:   `docker build -t nginx . && docker run --name nginx --rm  -p 80:80 nginx nginx-debug -g 'daemon off;' `

# Links #
* [NGINX docker image](https://hub.docker.com/_/nginx/)
* [Virtual Hosts](https://gist.github.com/soheilhy/8b94347ff8336d971ad0)