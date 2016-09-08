# RemoteBase API

The official API of [RemoteBase](https://remotebase.io).

**Currently not versioned. The API is still experimental and can change.**


## What is RemoteBase?

RemoteBase is an open database of remote companies and jobs, made by a developer.


## Honor code

* Access the API at a reasonable rate.
* Make something of your own. I don't mind if you build a clone of RemoteBase, but
the world needs to hear your voice, not mine.

## Current version

Access the endpoints at `http://api.remotebase.io/`. `v1` is coming soon.


## Endpoints

### Companies

* List companies

  List all companies, or ones that match the filter.

  `GET /companies`

  *Parameters*

  * name [string] - name of the company
  * has_retreats [bool]
  * technologies [string] - single value for a technology
  * collaboration_methods [string] - A name of a collaboration method. Can supply multiple.
  * communication_methods [string] - A name of a communication method. Can supply multiple.
  * bootstrapped [bool]
  * is_standalone [bool]
  * team_size_min [number]
  * team_size_max [number]
  * page [int]
  * per_page [int]


  *Response*
  ```
  Status: 200 OK
  Link: <http://api.remotebase.io/v1/companies?page=2>; rel=next"

  [
    {
      name: "RemoteBase"
      ...
    },
    {
      ...
    },
    ...
  ]
  ```

### jobs

* List jobs

  List all jobs on RemoteBase

  `GET /jobs`

## License

MIT
