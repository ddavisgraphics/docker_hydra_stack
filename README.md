# HYDRA DOCKER SETUP

Note this is for Hydra Version 10.0.0

## Create a new rails 4.2.6

- Using docker we are going to create a temporary box to run first so that we can generate our application. In our main host folder use the following command `docker run --rm -v $(pwd):/usr/src -w /usr/src -ti djdaviswvu/ruby_node bash`
  - `--rm` removes the vm from production right after you close and deletes all of its contents so essentially makes it known as a temporary project
  - `-v` declares the current volume to sync to in this example it is syncing the usr/src files with the current directory in your host folder
  - `-w` starts the container in the specific, our case is the usr/src directory
  - `-ti` enables you to interact with the VM
  - `ruby:2.3.3` is the image we are using
  - `bash` opens a bash window for giving the commands used to generate the application

- `rails 4.2.6 new hydra-demo`  This creates a rails 4.2.6 application named hydra-demo you can change this name to whatever it needs to be for the specific project. Ideally this would be a git repo that gets pulled into the hydra stack during development, but this way explains exactly how to create a new hydra head from the start.     

### Run Hydra Specific Dependencies

- add `gem 'hydra', '10.0.0'` to the gemfile.
- run `bundle install` so that all hydra dependencies get installed
- Run the hydra generator `rails generate hydra:install`

### Be Sure Solr 6.x

-
