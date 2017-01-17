# HYDRA DOCKER SETUP

Note this is for Hydra Version 10.0.0

## Create a new rails 4.2.6

- `rails _4.2.6_ new hydra-demo`  This creates a rails 4.2.6 application named hydra-demo you can change this name to whatever it needs to be for the specific project. Ideally this would be a git repo that gets pulled into the hydra stack during development.   

### Run Hydra Specific Dependencies

- add `gem 'hydra', '10.0.0'` to the gemfile.
- run `bundle install` so that all hydra dependencies get installed
- Run the hydra generator `rails generate hydra:install`

### Be Sure Solr 6.x
