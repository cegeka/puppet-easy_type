source 'https://rubygems.org'

group :development, :test do
  gem 'rake',    :require => false
  gem 'rspec-its'
  gem "puppet-blacksmith"
  platform :ruby_19, :ruby_20, :ruby_21 do
    gem 'byebug'
    gem 'rubocop', :git => 'https://github.com/bbatsov/rubocop',  :require => false
    gem 'travis'
    gem 'travis-lint'
    gem 'ruby_gntp'
  end
end

group :development do
  platform :ruby_19, :ruby_20, :ruby_21 do
    gem 'guard-rspec'
    gem 'pry-byebug'
    gem 'pry'
  end
end


group :test do
  platform :ruby_19, :ruby_20, :ruby_21 do
    gem 'coveralls',               :require => false
    gem 'simplecov',               :require => false
  end
  gem 'puppet-lint'
  gem 'rspec-puppet', '~> 1.0.0'
  gem 'rspec-system-puppet'
  gem 'puppetlabs_spec_helper'
  gem 'puppet-syntax'
end

if puppetversion = ENV['PUPPET_GEM_VERSION']
  gem 'puppet', puppetversion, :require => false
else
  gem 'puppet', :require => false
end
