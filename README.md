### Markov Project

1. Fork this to your own Github account
1. Clone it into your virtual machine's `/vagrant/projects` directory
1. Change to the right directory (`cd img240-markov`)
1. Create the database: `bin/rake db:create`
1. Run it: `bin/rails server -b 0.0.0.0`

## Reading JSON

```ruby
require 'open-uri'
require 'json'

# read the output from the website
raw_data = open('http://127.0.0.1:3000/stories.json').read

# parse the data and turn it into a regular Ruby hash
json_data = JSON.parse(raw_data)

# now you can use the hash however you like

puts json_data['authors'].first

# =>
{
      "key" => "poe",
     "name" => "Edgar Allan Poe",
      "url" => "http://127.0.0.1:3000/stories/poe",
    "story" => "Merely this and nothing more .\n\n\n\n..."
}

```
