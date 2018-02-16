# cloudformation_templates

# apache_website_cf_template.json

Used to launch an ASG with instances that have git, apache, and a basic
index.html file in the web root.

- LaunchConfig UserData - Installs git
- LaunchConfig UserData - Installs apache
- LaunchConfig UserData - Downloads Github repo with index.html
- ASG - Size 1

# wordpress_cf_template.json

Used to launch an ASG with instances that have and empty Wordpress
installation with the Divi theme and select plugins installed.

- LaunchConfig - specifies pre-created ami
- ASG - Size 1
- Prebuilt AMI - includes Wordpress, Divi, plugins



# elb_cf_template.json

Used to launch an ASG with multiple instances that will run on an Elastic
Load Balanceer.

- LaunchConfig with empty UserData

- ElasticLoadBalancer with instance port listening at 80

- ASG of size 2

- Output ELB URL 



# sinatra_elb_cf_template.json

Used to launch an ASG with multiple instances that will run a Sinatra Ruby web
application that can be cloned from Github.  The ASG will run on an Elastic
Load Balancer.  

- LaunchConfig with UserData

- UserData installs git
- UserData clones github repo containing application
- UserData downloads and installs rvm
- UserData installs Sinatra gem
- UserData logs app.rb to rubyApp.log

- ElasticLoadBalancer with instance port listening at 4567

- ASG of size 2

- Output ELB URL
