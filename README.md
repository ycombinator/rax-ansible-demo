# Demo playbook for Rackspace Cloud
This Ansible playbook sets up 1 Cloud Load Balancer and 2 Cloud Servers behind it.

# Setup
1. [Sign in](https://mycloud.rackspace.com/) to your Rackspace Cloud account and make note of your username and API key.


1. Install [Ansible](http://www.ansible.com/).
   * If you are running Mac OSX and using [Homebrew](http://brew.sh/), you can run:
   
     ```
     $ brew install ansible
     ```
     
1. Install pyrax. This is used by the Ansible `rax*` modules to connect to the Rackspace Cloud.

   ```
   $ pip install pyrax
   ```
   
1. Setup your Rackspace Cloud credentials.

   ```
   $ cat > ~/.rackspace_cloud_credentials <<EOT
   [rackspace_cloud]
   username = YOUR_RACKSPACE_CLOUD_USERNAME
   api_key = YOUR_RACKSPACE_CLOUD_API_KEY
   EOT
   ```

1. Clone this repo.

   ```
   $ git clone https://github.com/ycombinator/rax-ansible-demo.git
   ```

1. Run the Ansible playbook.

   ```
   $ cd rax-ansible-demo
   $ ansible-playbook -i inventory/prod site.yml
   ```