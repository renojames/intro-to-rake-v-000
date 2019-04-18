

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

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

desc 'depency task, provides access to environment file'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'creates a table and migrates it to the db'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the bd with dummy data'
  task :seed do
    require_relative './db/seeds'
    puts "The db has been seeded."
  end
end
