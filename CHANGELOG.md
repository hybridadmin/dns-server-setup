# Changelog

All notable changes to this project will be documented in this file.  
Type of changes can be `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`.

## [2.0.0] - 2020-12-12

### Fixed

- Fixed issue where certbot could not renew certificates due to permissions & nginx binding on port 80
  - Requires complete re-install of certificates

### Changed

- Tuning of Unbound, increased number of file descriptors
- Set static cache size for Unbound, might be changed to dynamic later when stability is confirmed
- Made golang version upgradable by always re-installing golang on each deploy
- Updated m13253 DoH server to 2.2.4

## [1.1.0] - 2020-12-06

### Fixed

- Fixed issue with files potentially having Windows CR/LF line endings, making custom cron job in /etc/cron.d/ to not execute

## [1.0.2] - 2020-12-05

### Fixed

- Fixed issue with accidental spaces in ahadns cron.d file making custom cron jobs to not execute

## [1.0.1] - 2020-12-04

### Fixed

- Fixed issue where /etc/resolv.conf wasn't updated properly making all DNS lookups fail
- Added explicit listen directive in unbound for IPv6 address

### Changed

- Increased unbound cache memory usage by tweaking parameter unbound_rrset_cache_mb in playbook

## [1.0.0] - 2020-12-02

### Added

- Initial version of automated AhaDNS DNS server setup
- A CHANGELOG file to this project
- Initial version of a PR template
