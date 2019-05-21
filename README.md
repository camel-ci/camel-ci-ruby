# Camel CI Ruby Test Project

## Usage

### Prerequisites

You must have Ruby with debkit installed on your machine to use this project.

You can check if you already have it installed with the command: `mvn -v`.

Otherwise, you can get it with those steps:

- Download the ruby with debkit 2.5.5-1 installer [here](hhttps://rubyinstaller.org/downloads/)
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
rails db:migrate RAILS_ENV=development
bundle update
```

### Running Tests

```bash
rails test
```

### Running the application

```bash
rails server
```
