# Contributing to the BCD REST API Guidelines
The BCD REST API Guidelines is a company-wide initiative to develop consistent design guidelines for REST APIs. The initiative requires input and feedback from a variety of individuals both inside and outside of BCD.

To provide feedback, please follow the guidance in this document. Please note that these are just guidelines, not rules. Use your best judgment and feel free to propose changes to anything in this repository, including the contribution guidelines.

- [Creating issues](#creating-issues)
- [Recommended setup for contributing](#recommended-setup-for-contributing)
- [Documentation styleguide](#documentation-styleguide)
- [Commit messages](#commit-messages)
- [Pull requests](#pull-requests)

## Creating issues
- You can [create an issue][new-issue], but before doing that please read the bullets below and include as many details as possible.
- Perform a [cursory search][issue-search] to see if a similar issue has already been submitted.
- Reference the version of the BCD REST API Guidelines you are using.
- Include the guidance you expected and other places you've seen that guidance, e.g. [White House Web API Standards][white-house-api-guidelines].
- Include sample requests and responses whenever possible.

### Related repositories
This is the repository for BCD REST API Guidelines documentation only. Please ensure that you are opening issues in the right repository.

## Recommended setup for contributing
- Fork this repository on GitHub
- Install [Git][git] to your computer and clone your new forked repository
- Install [Atom][atom], [VS Code][vscode], or your favorite editor
- Install [markdown-toc package][markdown-toc]

## Documentation styleguide
- Use [GitHub-flavored markdown][gfm]
- Use syntax-highlighted examples liberally
- Trim trailing empty lines from HTTP requests
- Retain only essential headers for understanding the example
- Use valid (e.g., member names quoted), pretty-printed JSON with a 2 space indent
- Minimize JSON payloads by using ellipses
- Write one sentence per line

### Example
#### Request

```http
GET https://api-hotels.tripsource.com/hotels/get_list/?destination=Region%3A48.224147%2C16.350547&search_radius=5&search_radius_unit=km&limit=5&order=-star_rating&page=1&chains=HS%2CRT&star_rating_filter=3%2C4%2C5&hotel_name_keyword=mozart&checkin=2018-10-28&is_multi_traveler_mode=false&suggest_alternative=&entity_id=42904&system=obt&api_key=testkey&customer_ip=192.168.31.116&locale=en_US&nonce=1543353502645&session_id=71IxqHT8mgMe5ohsZ25e5P&timestamp=1388774110&user_agent=Mozilla%2F5.0%20(Linux%3B%20Android%207.0%3B%20SM-G930V%20Build%2FNRD90M)%20AppleWebKit%2F537.36%20(KHTML%2C%20like%20Gecko)%20Chrome%2F59.0.3071.125%20Mobile%20Safari%2F537.36 HTTP/1.1
Accept: application/json
```

#### Response

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "customer_ip": null,
  "errors": [],
  "locale": "en_US",
  "session_id": "7c54yHqPA5FulQJVxbwlUT",
  "user_agent": "MOBAPICLIENTv1",
  "current_page": 1,
  "hotels_data": [
    {
      "address": "Schottenring 24",
      "airport_code": "VIE",
      "amenities": {
        "property_amenities": [
          "AIRSH",
          "BAR",
          "BCNT",
          "BFST",
          "CCNT",
          "CLNG",
          "FWIFI",
          "GOLF",
          "GYM",
          "INTT",
          "KIDAC",
          "LIFT",
          "LNDR",
          "MTNG",
          "NSMK",
          "PARK",
          "PETS",
          "POOL",
          "RSTR",
          "RSVC",
          "SAUNA",
          "TENN",
          "WCHR"
        ],
        "room_amenities": [
          "ACND",
          "MBAR",
          "SAFE",
          "TV"
        ]
      },
      "chain_info": [
        {
          "chain_code": "KI",
          "chain_name": "Kempinski Hotels",
          "master_chain_code": "GL",
          "master_chain_name": "Globalhotel Alliance"
        }
      ]
      ...
      "tmc_preference_tier": 2,
      "tmc_preferred": true,
      "trip_advisor_rating": 5,
      "is_on_request_hotel": false,
      "is_cash_only_hotel": false
    }
  ],
  "hotels_found_total": 466,
  "hotels_returned": 2,
  "more_results_available": true,
  "page_results": 233
}
```

## Commit messages
- Use the present tense: "Change ...", not "Changed ..."
- Use the imperative mood: "Change ...", not "Changes ..."
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally

## Pull requests
Pull requests serve as the primary mechanism by which contributions are proposed and accepted. We recommend creating a [topic branch][topic-branch] and sending a pull request to the `vNext` branch from the topic branch. For additional guidance, read through the [GitHub Flow Guide][github-flow-guide].

Be prepared to address feedback on your pull request and iterate if necessary.

[new-issue]: https://github.com/chmarz/API-guidelines/issues/new
[issue-search]: https://github.com/chmarz/API-guidelines/issues
[white-house-api-guidelines]: https://github.com/WhiteHouse/api-standards/blob/master/README.md
[topic-branch]: http://www.git-scm.com/book/en/v2/Git-Branching-Branching-Workflows#Topic-Branches
[gfm]: https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown
[github-flow-guide]: https://guides.github.com/introduction/flow/
[atom-beautify]: https://atom.io/packages/atom-beautify
[atom]: http://atom.io
[markdown-toc]: https://atom.io/packages/markdown-toc
[vscode]: https://code.visualstudio.com/
[git]: https://git-scm.com/
