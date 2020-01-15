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
 
 
 #### WORKSTATION(.Chef/) ----->> uploadingdata using knife ----->> Chef-server
 #### Chef-server----------->> Privatekey (.pem and knife.rb file) ---------->> WORKSTATION


#### Data Bags
  * Data bags are containers for information about your infrastructures that are not associated with the node.
  * Data bags is a global variable that is stored as json data, and is accessible via a chef server. Because the data bag is on the Chef server, it acts as a shared resource which Chef clients can reference.
  * Data bags can also be used to encrypt sensitive information with a shared key; anyone with the shared key can decrypt the data in the data bag. This provides one method to keep secrets off of nodes.
  
#### Chef Vault
  * Vault allows the secure distribution of secrets as an alternative to encrypted data bags. Vault allows limiting which users and nodes have access to secrets.
