> **:truck: moved to https://github.com/NordicSemiconductor/cell-geolocation-helpers-js**  
> :information_source: [more info](https://github.com/bifravst/bifravst/issues/56)

# Cell Geolocation Helpers [![npm version](https://img.shields.io/npm/v/@bifravst/cell-geolocation-helpers.svg)](https://www.npmjs.com/package/@bifravst/cell-geolocation-helpers)

[![GitHub Actions](https://github.com/bifravst/cell-geolocation-helpers/workflows/Test%20and%20Release/badge.svg)](https://github.com/bifravst/cell-geolocation-helpers/actions)
[![Known Vulnerabilities](https://snyk.io/test/github/bifravst/cell-geolocation-helpers/badge.svg)](https://snyk.io/test/github/bifravst/cell-geolocation-helpers)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Renovate](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com)
[![Mergify Status](https://img.shields.io/endpoint.svg?url=https://dashboard.mergify.io/badges/bifravst/cell-geolocation-helpers&style=flat)](https://mergify.io)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier/)
[![ESLint: TypeScript](https://img.shields.io/badge/ESLint-TypeScript-blue.svg)](https://github.com/typescript-eslint/typescript-eslint)

Helper functions for the cell geolocation feature.

## Installation

    npm i --save-dev @bifravst/cell-geolocation-helpers

## `cellId`

Simple formatter to create identifier strings from cell information. This is
used to unify the way these ids are generated between frontend and backend.

## `cellFromGeolocations`

![Demo of cellFromGeolocations results](./map.gif)

_(Demo and above GIF are using 5km min cell radius and P=0.9.)_

Calculates a cell geo location based on a list of geo locations:

- the center is the average of all given locations (within a configurable
  percentile)
- the diameter returned is a circle that includes all given locations (within a
  configurable percentile), but at least `minCellDiameterInMeters`.

Check out the live demo on
<https://bifravst.github.io/cell-geolocation-helpers>.
