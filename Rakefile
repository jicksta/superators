# -*- ruby -*-

require 'rubygems'
require 'hoe'
require './lib/superators.rb'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new do |opts|
  opts.rspec_opts = %w'-c'
end

desc "Generate a HTML report of the RSpec specs"
RSpec::Core::RakeTask.new "report" do |opts|
  opts.rspec_opts = %w'--format html:report.html'
end

Hoe.spec 'superators' do
  self.version = Superators::VERSION
  self.rubyforge_name = 'superators'
  self.author = 'Jay Phillips'
  self.email = 'jay -at- codemecca.com'
  self.summary = 'Superators add new sexy operators to your Ruby objects.'
  self.description = paragraphs_of('README.txt', 2..5).join("\n\n")
  self.url = paragraphs_of('README.txt', 0).first.split(/\n/)[1..-1]
  self.changes = paragraphs_of('History.txt', 0..1).join("\n\n")
end

# vim: syntax=Ruby
