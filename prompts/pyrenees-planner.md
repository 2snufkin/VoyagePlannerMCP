# Pyrenees Hendaye Trip Planner Prompt

Plan a point-to-point walking trip in the French Pyrenees, starting from Hendaye or a nearby practical TER/SNCF-accessible departure point.

## User Constraints

- Date window: flexible between 14 July 2026 and 20 July 2026.
- Start: Hendaye or nearby.
- End: another SNCF/TER-accessible station, not the same as the start.
- Maximum walking distance: 20 km per day.
- Accommodation: prioritize gite d'etape, refuge, hostel, or simple mountain lodging.
- Return format: write a Markdown file.

## Required Research

Use browser/search/scraping tools to find:

- feasible walking route stages
- distance per stage in km
- elevation gain/loss where available
- estimated walking time
- sites/views/points of interest
- sleeping option for each night
- price per person/night
- online availability for the relevant date, if available
- booking/contact link
- nearby train/bus access for arrival and return

## Search Strategy

Start with route options around:

- Hendaye
- Sare
- Ainhoa
- Saint-Jean-Pied-de-Port
- Bidarray
- Saint-Etienne-de-Baigorry
- Cambo-les-Bains

Prefer routes that can end at or near:

- Saint-Jean-Pied-de-Port station
- Cambo-les-Bains station
- Saint-Jean-de-Luz/Ciboure station
- Bayonne station

Useful search terms:

- "GR10 Hendaye Saint Jean Pied de Port gite etape"
- "gite d'etape Sare availability July 2026"
- "gite d'etape Ainhoa tarifs"
- "refuge gite Bidarray tarifs disponibilites"
- "Hendaye to Sare walking distance GR10"
- "Saint Jean Pied de Port TER station"

## Output File

Write the result to:

```text
itineraries/pyrenees-hendaye-2026.md
```

## Markdown Structure

```md
# Pyrenees Hiking Itinerary: Hendaye Area, 14-20 July 2026

## Summary

- Recommended route:
- Date range:
- Total walking days:
- Total distance:
- Start transport:
- Return transport:
- Main uncertainty:

## Day 1: ...

- Date:
- From:
- To:
- Distance:
- Elevation:
- Estimated walking time:
- Route notes:
- Sites/views:
- Accommodation:
  - Name:
  - Type:
  - Price:
  - Availability:
  - Booking/contact:
  - Source:
  - Confidence:

## Transport

## Alternatives

## Sources Checked

## Items Requiring Manual Confirmation
```

## Quality Rules

- Do not invent prices or availability.
- If availability cannot be verified online, say so clearly.
- Include source links for every price and availability claim.
- Prefer official accommodation pages over third-party summaries.
- If a stage is over 20 km, reject it or split it.
- If train details are uncertain, include the station and source link but mark timetable as needing confirmation.

