desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do 
  desc 'say hello'
  task :hello do 
    puts "hello from Rake!"
  end 

  desc 'say hola'
  task :hola do 
    puts "hola de Rake!"
  end 
end 

desc 'drop into Pry console'
task :console => :environment do 
  Pry.start 
end 

task :environment do
  require_relative './config/environment'
end

namespace :db do 
  desc 'migrate changes to database'
  task :migrate => :environment do 
    Student.create_table
  end 

  desc 'seed database with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end 
  
end 