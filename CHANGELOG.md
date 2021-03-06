# PHP 5 (`php5`) - Change log

All notable changes to this role will be documented in this file.
This role adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

Note: Developers - make sure to set the `php5_barc_role_version` variable when releasing new versions of this role.

## [Unreleased][unreleased]

## 0.2.0 - 11/05/2016

### Added

* Local facts to record this role has been applied to a system and its version, plus supporting documentation sections
* Missing 'system-core' role application in test playbooks
* Guidance on compatibility with PHP 7
* Temporary fix to use Ansible Galaxy in CI

### Fixed

* Change log formatting
* Incorrect role name-space in test playbook
* Miss-spelling of `.gitkeep` in `/files`
* Wrong extension was checked for when testing if the PDO extension is installed on CentOS
* Minor README typos
* Incorrect variable name in reminder to change the role manifest version variable in the change log
* Incorrect test for determining if the correct PHP package is installed on CentOS when using non-system sources
* Repeating playbook run before idempotence test in CI to fix strange problem with change event on only the first replay

### Changed

* Migrating from old Ansible Galaxy namespace, 'BARC', to 'bas-ansible-roles-collection'
* Migrating from old Ansible Galaxy 'categories' to new 'tags' meta-data
* Migrating from old Repository in 'antarctica' to 'bas-ansible-roles-collection'
* Migrating from old Semaphore 'antarctica' organisation to 'bas-ansible-roles-collection'
* Simplifying CI setup tasks
* Switching from general to CLI only PHP packages to prevent dependency on Apache web-server
* Adding CLI SAPI configuration file for CentOS to allow configuration options to be per-SAPI - fixes [BARC-100]
* Reducing the number of configuration options set for the CLI SAPI by this role

## 0.1.0 - 03/02/2016

### Added

* Initial version - based on existing PHP role but with additional extensions and bundled Composer support
