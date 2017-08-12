# HAE data stuff
Couple of notebooks here:

* [01-fetch_evictions.ipynb](01-fetch_evictions.ipynb) (wait for it)
  fetches eviction records from from Harris County, TX, courts public
  data extracts API and saves them without postprocessing.  It's
  mostly cleaned up for conversion to a standalone retrieval script,
  except for two things: there are still some interactive bits from
  exploring the interface to remove, and it needs a main routine to
  accept query parameters.
* [02-clean_evictions.ipynb](02-clean_evictions.ipynb) Normalizes the
  results from notebook 1, particularly column names and types.
  Minimal exporation (plot) to ensure data looks ok.
* [03-geocode_evictions.ipynb](03-geocode_evictions.ipynb) Takes the
  unique addresses (roughly half the number of eviction records) from
  notebook 2 and geocodes addresses to lon/lat, FIPS state & county,
  and Census tract and block using the Census Bureau's bulk geocoder
  API.
* [04-explore_evictions.ipynb](04-explore_evictions.ipynb) (in
  progress). Plots to explore temporal and geographic
  patterns/variation/clustering of evictions.

* [05-explore-fema.ipynb](05-explore-fema.ipynb) Plots and simplifies
  the FEMA FRIS (Flood Risk Insurance System) geographies in Harris
  County where building owners must purchase flood insurance.
  
| | count |
|-|-|
|total cases | 207818 |
|unique addresses | 96752 |
|geocoding matches | 84414 |
|exact matches | 52896 |
