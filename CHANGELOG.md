# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).
## [1.1.0] - TBD

### Added
- ReadOnlyAuth Pre Event Listener to manage Hive database whitelist in read-only metastores [apiary-metastore-extensions](https://github.com/ExpediaGroup/apiary-extensions/tree/master/apiary-metastore-auth).
- Support for `_` in `HIVE_DB_NAMES` variable. Fixes [#5] (https://github.com/ExpediaGroup/apiary/issues/5).

### Changed
- Updated apiary-metastore-listener to 3.0.0 (was 1.1.0).
- Updated apiary-gluesync-listener to 3.0.0 (was 1.1.0).
- Updated apiary-ranger-plugin to 3.0.0 (was 1.1.0).
- Updated apiary-metastore-metrics to 3.0.0 (was 1.1.0).
- Updated apiary-metastore-auth to 3.0.0 (was 1.1.0).

## [1.0.1] - 2019-02-15

### Added
- Auto configure Hive metastore heapsize when running on ECS.

### Changed
- Replace EMRFS with hadoop-aws S3A libraries.

## [1.0.0] - 2018-10-31

### Added
- Option to send metastore metrics to CloudWatch - see [#4](https://github.com/ExpediaGroup/apiary-metastore-docker/issues/4).
- Refactor Environment variable names.
- Migrate secrets from Hashicorp Vault to AWS SecretsManager.
- Update startup script to configure Log4j, to fix sending Hive Metastore logs to CloudWatch.

### Changed
- Deploy RangerAuth Pre Event Listener from [apiary-metastore-extensions](https://github.com/ExpediaGroup/apiary-extensions/tree/master/apiary-ranger-metastore-plugin).
- Deploy GlueSync Listener from [apiary-metastore-extensions](https://github.com/ExpediaGroup/apiary-extensions/tree/master/apiary-gluesync-listener).
- Deploy SNS Listener from [apiary-metastore-extensions](https://github.com/ExpediaGroup/apiary-extensions/tree/master/apiary-metastore-listener).
- Additional check to support external MySQL database for Hive Metastore, required to implement [#48](https://github.com/ExpediaGroup/apiary-metastore/issues/48).

### Fixed
- Fix to update cacerts for Java.
- Fix Hive Metastore logging.
