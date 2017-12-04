desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc 'prints out hello from Rake!'
    task :hello do
      puts "hello from Rake!"
    end
  desc 'prints out hola'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'invokes environment as dependency'
    task :migrate => :environment do
    Student.create_table
  end
  desc 'seeds with dummy data from seed file'
    task :seed do
      require_relative './db/seeds.rb'
    end
end

task :environment do
  require_relative './config/environment'
end
