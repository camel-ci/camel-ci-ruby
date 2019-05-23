# Camel CI Ruby Test Project

## Usage

### Prerequisites

You must have Ruby with debkit installed on your machine to use this project.

You can check if you already have it installed with the command: `gem -v`.

Otherwise, you can get it with those steps:

- Download the ruby with debkit 2.5.5-1 installer [here](https://rubyinstaller.org/downloads/)
- Run it and make sure to have "Add Ruby executables to your PATH" checked
- When installing MSYS2, Install all 3 steps (1, 2 & 3)

### Installing dependencies

```bash
gem install bundler
gem install sqlite3 -v '1.4.1' --source 'https://rubygems.org/'
```

### Building/Rebuilding the project

```bash
bundle install
rake app:update:bin
```

### Running Tests

```bash
rails db:migrate RAILS_ENV=test
bundle update
rails test
```

### Running the application

```bash
rails db:migrate RAILS_ENV=development
bundle update
rails server
```
