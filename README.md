# Ruby

Master: [![Build Status](https://travis-ci.org/sansible/ruby.svg?branch=master)](https://travis-ci.org/sansible/ruby)  
Develop: [![Build Status](https://travis-ci.org/sansible/ruby.svg?branch=develop)](https://travis-ci.org/sansible/ruby)

* [Installation and Dependencies](#installation-and-dependencies)
* [Tags](#tags)
* [Examples](#examples)

This roles installs ruby and bundler globally.




## Installation and Dependencies

To install run `ansible-galaxy install sansible.ruby` or add this to your
`roles.yml`

```YAML
- name: sansible.ruby
  version: v2.0
```

and run `ansible-galaxy install -p ./roles -r roles.yml`




## Tags

This role uses one tag: **build**

* `build` - Installs Ruby all it's dependencies.





## Examples

To install:

```YAML
- name: Some app
  hosts: "{{ hosts }}"

  roles:
    - role: sansible.ruby
```

To install without default config:

```YAML
- name: Some app
  hosts: "{{ hosts }}"

  roles:
    - role: sansible.ruby
      ruby_version: "2.3"
      ruby_gems:
          - bundler
          - sass
```
