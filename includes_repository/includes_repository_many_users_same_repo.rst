.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


It is possible for multiple users to access the |chef server| using the same |knife rb| file. (A user can even access multiple organizations if, for example, each instance of the |chef repo| contained the same copy of the |knife rb| file.) This can be done by adding the |knife rb| file to the |chef repo|, and then using environment variables to handle the user-specific credential details and/or sensitive values. For example:

.. code-block:: ruby

   current_dir = File.dirname(__FILE__)
     user = ENV['OPSCODE_USER'] || ENV['USER']
     node_name                user
     client_key               "#{ENV['HOME']}/.chef/#{user}.pem"
     validation_client_name   "#{ENV['ORGNAME']}-validator"
     validation_key           "#{ENV['HOME']}/.chef/#{ENV['ORGNAME']}-validator.pem"
     chef_server_url          "https://api.opscode.com/organizations/#{ENV['ORGNAME']}"
     cache_type               'BasicFile'
     cache_options( :path => "#{ENV['HOME']}/.chef/checksums" )
     cookbook_path            ["#{current_dir}/../cookbooks"]
     cookbook_copyright "Your Company, Inc."
     cookbook_license "apachev2"
     cookbook_email "cookbooks@yourcompany.com"
   
     # all your credentials are belong to us
   
     # Amazon AWS
     knife[:aws_access_key_id] = "#{ENV['AWS_ACCESS_KEY_ID']}"
     knife[:aws_secret_access_key] = "#{ENV['AWS_SECRET_ACCESS_KEY']}"
   
     # Rackspace Cloud
     knife[:rackspace_api_username] = "#{ENV['RACKSPACE_USERNAME']}"
     knife[:rackspace_api_key] = "#{ENV['RACKSPACE_API_KEY']}"   









