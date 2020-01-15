# Chef
#### CheckDK includes:
  * a built-in Ruby runtime
  * Ohai(tool use to get attributes of nodes including OS details, list of hostname, networking details, etc) and chef-client
  * Testing tools:
    * Test Kitchen: An integration-testing framework tool that tests cookbooks across platforms
    * ChefSpec
    * Rubocop: Ruby style-checking tool
    * Foodcritic: A lint tool for static analysis of recipe code
  * Chef provisioning
  * Everything else needed to author cookbooks and upload them to the Chef server
  
#### The Chef Workstation
  * A computer with ChefDK installed on it is called a Chef Workstation.
  Each organization is comprised of:
    * One or more workstations
    * A single server
    * Every node that will be configured and maintained by the chef-client
  * Cookbooks and recipes tell chef-client how each node in your organization will be configured
    * chef-client does the actual configuration
 
 
 WORKSTATION(.Chef/) ----->> uploadingdata using knife ----->> Chef-server
 Chef-server----------->> Privatekey (.pem and knife.rb file) ---------->> WORKSTATION
