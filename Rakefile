

namespace:greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'ouptuts hola ot the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc "migrate changes to the db"
namespace :db do
  task migrate: [:environment] do
    Student.create_table
  end
  desc "seed the database with dummy data"
  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :environment do
  require_relative './config/environment'
end

desc 'drop into the pry console'
task console: [:environment] do
  Pry.start
end
