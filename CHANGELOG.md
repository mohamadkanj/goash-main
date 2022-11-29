# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased] 

### Fixed

 * issue with `CRUD` and zero values
 * issue with `apollo-client` and new refetch queries

### Added

 - administrator component generation
 - translation prefix for all language keys
 - persistence of plc structs with database objects and startup writing
 - default database objects to `config`
 - one-time listener to the `plc` with filter function
 - `gql.Uint64` a graphql type for uint64
 - `sntp` for a simple ntp server

### Updated

 * golang dependencies

## 0.0.5

### Changed

 * `handleGraphql` to use `SetBodyStreamWriter` instead of `c.JSON()`
 * `*CRUDHandler` to have a `TTL()` for time to live of database objects
 * `ShellRedirect` access via database object
 * updated `examples/main.go`

### Added

 * `CRUD` interfaces to persistence
 * `AppDirectory` to config
 * config loading from `AppDirectory`
 * `ReadWrite` interfaces to persistence
 * support for additional web-message
 
### Fixed

 * `graphiql.ps1` and `package.ps1` to use `go install` with `@latest` instead of the deprecated `go get`
 * issue with subfolder and meta files on template generation
 * issue with `webserver.EmptyFileSystem`
 * issue with multiline comments

## 0.0.1

### Added

  * added `async` from `github.com/automation-gmbh/goads/pkg/async`
  * added `gql` package to place graphql utils
  * support for `chartjs-plugin-zoom`
  * `createBarDataset` to show bar charts
  
### Fixed

  * issue with same structs in different components 
  * issue with graphql input objects
  * issue with moving `github.com/automation-gmbh/goads/pkg/async`
  * issue with log level

### Changed
 
 * component lookup via ads symbol 
 * `async` from `github.com/automation-gmbh/goads/pkg/async`
 * `GetLogger(name)` to get a logger from a logger for depper loging configuration
 * `Test-Logger` to log based on the given `log-level`
 * overwrite order of connection options for plc observables

### Updated

 * golang dependencies

### Removed