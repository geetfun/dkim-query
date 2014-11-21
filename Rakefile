# encoding: utf-8
require 'rubygems'

begin
  require 'bundler/setup'
rescue LoadError => e
  warn e.message
  warn "Run `gem install bundler` to install Bundler."
  exit -1
end

require 'rake'
require 'bundler/gem_tasks'

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new

namespace :spec do
  desc "Tests DMARC::Parser against Alexa Top 500"
  # RSpec::Core::RakeTask.new(:gauntlet) do |t|
    # t.rspec_opts = '--tag gauntlet'
  # end
end

task :test    => :spec
task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new  
task :doc => :yard
