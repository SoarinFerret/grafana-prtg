# Change Log

As of July, 2017, all significant changes will be logged in this document.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).

## [4.0.1] - 2017-07-24

- **Query Editor**: Fixed color highlighting. Addresses [#48](https://github.com/neuralfraud/grafana-prtg/issues/48)
- **Query Editor**: Added option to include a device's name in an item's label. Addresses [#47](https://github.com/neuralfraud/grafana-prtg/issues/47)
- **API**: Added query string parameter "&count=9999" to group, device, and sensor queries to resolve issues for larger deployments. Addresses [#49](https://github.com/neuralfraud/grafana-prtg/issues/49)
- **API**: Updated method to retrieve historic data, fixes an issue where no values are returned if the channel display name differes from the name in the API XML response. For instance, SSL Security sensors display the channel "Security Rating", when the actual value contains additional descriptive text. 
- **API**: Performance improvements in the collection of historic data, the array index to retrieve the channel value from is determined using the first result record instead of being determined for each result, which has a noticable impact with multiple-channel queries and thousands of data points. 

## [4.0.0] - 2017-07-17

### Fixed

- PRTG Logo filename case, closed [#36](https://github.com/neuralfraud/grafana-prtg/issues/36).
- Fixed condition where some queries that fail cause Grafana to display an error message like "Cannot read property 'match' of undefined, closed [#44](https://github.com/neuralfraud/grafana-prtg/issues/44)

### Changed

- **Templating**: Proper support for multiple-value template items.
- All code is ES6 compliant.

### Added

- **Query Editor**: Mutiple items can be selected from a single query.
- **Query Editor**: Select from Raw JSON, Metrics, or Text property query mode.
- **Query Editor**: Full regular expression support for all query filters.