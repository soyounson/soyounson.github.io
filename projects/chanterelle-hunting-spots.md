---
layout: project
title: Chanterelle hunting spots
slug: chanterelle-hunting-spots
permalink: /projects/chanterelle-hunting-spots/
---

## The question

Chanterelle season seems to start at very different times depending on where people post their finds from. *When does it actually peak where I live, and does rain explain it?*

The map answers that from public records: where and in which month people logged golden chanterelles in Europe, the USA and Canada, next to the rain and temperature of the same place.

## Data

- **Records**: GBIF.org occurrence records for the genus *Cantharellus* (taxonKey 9623860), about 113,000 across Europe (88,088), the USA (22,956) and Canada (2,093), counted in 1° × 1.5° grid cells (about 110 km) with a month breakdown. Each cell is credited to the largest city of 150,000+ people (60,000+ in Canada) within about 110 km.
- **Rain contours**: monthly normals from 86 weather stations (mostly 1991–2020), blended by distance (about 180 km reach) and left blank beyond 450 km from a station.
- **Spot climate**: one weather station per highlighted spot, from Wikipedia climate tables (national weather services).

Records show where people found and logged chanterelles, so busy areas also reflect where more people look. Grouping into ~110 km cells also keeps anyone's own patch private.

## What the data shows

- Europe peaks in **August–September**; the USA overall in **July–August**.
- Coastal California runs the other way: records around San Jose peak in **January**.
- Monthly charts per spot put rain, temperature and records on one axis, so the lag between wet months and fruiting is easy to see.

## Design

- **Map first**: one mushroom per big city, sized by records. Pick a country, a city and a month and the map zooms to the 25 km around it, with rivers, mountains and blue rain bands.
- **Harvest outlook**: an illustrated fox fills a net bag with the chosen month's records; the bag is full in the busiest month.
- **Climate × Fruiting**: Apache ECharts bars and lines per spot.
- Light and dark themes in the same Apple-style look as this site. The page is a single HTML file that also works offline.

## Stack

Python (GBIF API, standard library only) builds the grid file; D3 draws the map from Natural Earth and US Census outlines; Apache ECharts draws the charts. Hosted on GitHub Pages.

## Next

- Predict this year's chance of chanterelles from the previous months' weather
- Year-by-year weather instead of long-term normals

Check with a local expert before eating anything you pick.
