# HAE data stuff
Couple of notebooks here:

* [fetch\_evictions.ipynb](fetch_evictions.ipynb) (wait for it)
  fetches eviction records from from Harris County, TX, courts public
  data extracts API.  It's mostly cleaned up for conversion to a
  standalone retrieval script, except for two things: there are still
  some interactive bits from exploring the interface to remove, and it
  needs a main routine to accept query parameters.
* [geocode_evictions.ipynb](geocode_evictions.ipynb) dedups addresses
  (roughly halves the number of addresses) and tries to geocode them
  using the Census Bureau's free bulk geocoding service.  This works
  fairly well:
  
| | count |
|-|-|
|total cases | 207818 |
|unique addresses | 96752 |
|geocoding matches | 84414 |
|exact matches | 52896 |
