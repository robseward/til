#Disable printing objects in the Rails console after every command

1. Add a nil statement at the end of your command, the console only prints the value of the last statement: `Objects.all.each { |x| puts x.name }; nil`
2. Temporarily disable echoing in the console configuration  `conf.echo = false`
