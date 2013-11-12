task :create_class_dirs do
	File.open("names") do |f|
		dir_name = "#{f.gets.chomp}.git"
		Dir.mkdir(dir_name) unless Dir.exists? dir_name
		Dir.chdir(dir_name)
		system('git init --bare')
		Dir.chdir('..')
		system("chown git:git #{dir_name}")
	end
end	
