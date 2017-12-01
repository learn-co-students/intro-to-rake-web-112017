
namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end


namespace :db do
  desc 'migrate changes to your databse'
  task :migrate => :environment do
    Student.create_table
  end
  task :environment do
    require_relative './config/environment'
  end

  desc 'seeds the databse with dummy data from a seed file'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into pry repl'
task :console do
  pry.start
end
