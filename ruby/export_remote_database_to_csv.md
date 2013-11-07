# Export_Remote_Database_to_CSV
<!--- desc --->
This command can be used in the Rails console to export the data to a CSV. I use this command to generate small CSV's for analysis or what have you.
<!--- end_desc --->
```
model = User.all
@csv = File.new('Filename.csv','w')

@csv << User.last.attributes.keys.join(", ") + "\n" # "header" row with attribute names
model.each do |t|
  @csv << t.attributes.values.join(", ") + "\n"
end
```
#### Tags
<!--- tags --->
tag:csv tag:rails tag:console
<!--- end_tags --->