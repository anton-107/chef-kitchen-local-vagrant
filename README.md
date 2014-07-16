Using chef solo example

Initial steps:
- mkdir chef-kitchens/local-vagrant
- cd !$
- create Gemfile
- $ sudo gem install bundler
- $ sudo gem install dep_selector -v '1.0.3'
- $ bundle
- $ knife solo init .
- create Berksfile
- sudo gem install berkshelf-api-client
- berks install
- create nodes/web1.example.com.json
- $ vagrant box add precise64 http://files.vagrantup.com/precise64.box
- $ vagrant init precise64
- $ vagrant up
- $ knife solo prepare vagrant@127.0.0.1 -i ~/.vagrant.d/insecure_private_key -p 2222 -N web1.example.com
- modify Vagrantfile
- create environments/development.json
- $ vagrant plugin install chef
- $ rm -rf cookbooks
- $ berks vendor cookbooks
- $ vagrant provision