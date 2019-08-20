# passenger-rhel7-apache role

This is for use with Ruby on Rails on NCSU Libraries servers that are setup using Puppet. This role will add apache configuration to a standard location in our server setup to configure serving the Rails application with Passenger. Additional app-specific Apache configuration can also be added here.

## Usage

### Required variables

Values for the following variables must be set when running this role.

`web_server_name` is the fully qualified domain name
`vhost_shortname` is the short name given to the vhost in the puppet configuration for this server

### Optional variables

You can add additional Apache config to the VirtualHost by setting the `apache_virtualhost_lines` variable to include string or text block:

    apache_virtualhost_lines: '<SomeApacheConfig>Here</SomeApacheConfig'

or

    apache_virtualhost_lines: |+
      <Directory />
        Options Indexes FollowSymLinks Includes Multiviews
        ...
      </Directory>

You can also specify the docroot if needed in the
`apache_virtualhost_docroot` variable.
