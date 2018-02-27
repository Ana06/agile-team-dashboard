[![codecov](https://codecov.io/gh/openSUSE/agile-team-dashboard/branch/master/graph/badge.svg)](https://codecov.io/gh/openSUSE/agile-team-dashboard)

# Agile Team Dashboard project

This project is used to develop [OBS](http://openbuildservice.org) team Dashboard. The production instance can be found here: https://bs.suse.de

The Dashboard include the following features:

- Today meetings
- Today absences
- Calendar
- Team related open PRs
- ...

## CONTRIBUTING

### Running the project in development

We are using [Vagrant](https://www.vagrantup.com/) to create our development environment. You need to install [Vagrant](https://software.opensuse.org/package/vagrant) and [VirtualBox](https://en.opensuse.org/VirtualBox). After installing it:

1. Clone the repository:

    ```
    git clone https://github.com/openSUSE/agile-team-dashboard.git
    ```

2. Execute Vagrant in the cloned directory:

    ```
    vagrant up
    ```

3. Start the app:

    ```
    vagrant exec foreman start
    ```

4. Access the Rails app at [localhost:3001](http://localhost:3001). You can just sign up!


### Contribute code

To contribute code open pull requests.

Ensure that RSpec, Rubocop, Slim-Lint and JSHint pass locally before sending your PR and always that you add new changes.

Ensure you write good commit message.
You may want to read this [Commit messages guide](https://github.com/RomuloOliveira/commit-messages-guide).


## To run RSpec test

To run all the RSpec test:

```
vagrant exec bundle exec rspec
```

To run all the test in one spec file, for example `spec/models/user_spec.rb`:

```
vagrant exec bundle exec rspec spec/models/user_spec.rb
```

To only run the test in the line 10 of the file:

```
vagrant exec bundle exec rspec spec/models/user_spec.rb:10
```


## To run rubocop

To run Rubocop displaying cop names in offense messages:

```
vagrant exec bundle exec rubocop -D
```

To **autocorrect** Rubocop offenses, displaying also cop names in offense messages:

```
vagrant exec bundle exec rubocop -aD
```


## To run Slim-Lint

To run Slim-Lint in the current directory:

```
vagrant exec bundle exec slim-lint .
```


## To run JSHint

To run JSHint in the current directory:

```
vagrant exec jshint .
```


## Licence

Code published under MIT license (see [LICENSE](LICENSE)).



