# passenger-apache role

This is for use on NCSU Libraries servers that are setup using Puppet.

## Usage

 * Values for the following variables must be set in the ini files with the playbooks running this role: `/confs/{{web_server_name}}/{{vhost_shortname}}.conf`. The `web_server_name` is the fully qualified domain name and the `vhost_shortname` is the short name given to the vhost in the puppet configuration for this server.