require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "it"
    gem.summary = %Q{minimal task management for hackers}
    gem.description = %Q{minimalist console-based task management for hackers}
    gem.email = "self@cloudhead.net"
    gem.homepage = "http://github.com/cloudhead/it"
    gem.authors = ["cloudhead"]
    gem.add_development_dependency "rspec"
    gem.add_dependency "mutter", ">= 0.3.7"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

task :spec => :check_dependencies

task :default => :spec

