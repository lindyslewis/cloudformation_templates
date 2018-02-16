# cloudformation_templates

# apache_website_cf_template.json

- LaunchConfig UserData - Installs git
- LaunchConfig UserData - Installs apache
- LaunchConfig UserData - Downloads Github repo with index.html
- ASG - Size 1

# wordpress_cf_template.json

- LaunchConfig - specifies pre-created ami
- ASG - Size 1
- Prebuilt AMI - includes Wordpress, Divi, plugins


# sinatra_elb_cf_template.json
