# Instructions on how to set up various Thoth bots in your project

## Kebechet

* [Kebechet](https://github.com/thoth-station/kebechet#kebechet) is the bot that you can use to automatically update your project dependencies.

* Kebechet can be configured using a yaml configuration file ([.thoth.yaml](https://github.com/thoth-station/kebechet/blob/master/.thoth.yaml)) in the root of your repo.

  ```yaml
  host: khemenu.thoth-station.ninja
  tls_verify: false
  requirements_format: pipenv

  runtime_environments:
    - name: rhel:8
      operating_system:
        name: rhel
        version: "8"
      python_version: "3.6"
      recommendation_type: latest

  managers:
    - name: pipfile-requirements
    - name: update
      configuration:
        labels: [bot]
    - name: info
    - name: version
      configuration:
        maintainers:
          - goern   # Update this list of project maintainers
          - fridex
        assignees:
          - sesheta
        labels: [bot]
        changelog_file: true
  ```

## Zuul (Sesheta)

* You can use the [zuul](https://github.com/thoth-station/zuul-config) bot to set up automatic testing and merging for your PRs.

* Zuul can be configured using a yaml configuration file ([.zuul.yaml](https://github.com/thoth-station/zuul-config#integration-of-zuul-with-github-repos))

  ```yaml
  - project:
      check:
        jobs:
          - "noop"
      gate:
        jobs:
          - "noop"
      kebechet-auto-gate:
        jobs:
          - "noop"
  ```

* You can add different types of jobs:
  * `thoth-coala` job - It uses [Coala](https://coala.io/#/home?lang=Python) for code linting, it can be configured using a [.coafile](http://docs.coala.io/en/latest/Users/coafile.html#project-wide-coafile). in the root of your repo.
  * `thoth-pytest` job - It uses the pytest module to run tests in your repo.

* Zuul will not merge any PRs for which any of the specified jobs have failed.

* If there are no jobs specified in the zuul config (only `noops`), zuul will merge any PR as long as it has been approved by an authorized reviewer.
