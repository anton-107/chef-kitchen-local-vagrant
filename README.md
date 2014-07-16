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