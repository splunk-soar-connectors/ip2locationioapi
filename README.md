# IP2Location IO

Publisher: IP2Location.io <br>
Connector Version: 1.0.3 <br>
Product Vendor: IP2Location.io <br>
Product Name: IP2Location.io <br>
Minimum Product Version: 6.3.0

Query IP geolocation data from IP2Location.io API

\[comment\]: # File: manual_readme_content.md
\[comment\]: #
\[comment\]: # Copyright (c) IP2Location.io, 2024
\[comment\]: #
\[comment\]: # Licensed under the Apache License, Version 2.0 (the "License");
\[comment\]: # you may not use this file except in compliance with the License.
\[comment\]: # You may obtain a copy of the License at
\[comment\]: #
\[comment\]: # http://www.apache.org/licenses/LICENSE-2.0
\[comment\]: #
\[comment\]: # Unless required by applicable law or agreed to in writing, software distributed under
\[comment\]: # the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
\[comment\]: # either express or implied. See the License for the specific language governing permissions
\[comment\]: # and limitations under the License.

Query IP geolocation data from IP2Location.io API.

Get free IP2Location.io API from from https://www.ip2location.io/pricing for basic geolocation data.
Below is an example output if you're subscribed to the Security plan.

JSON

<pre>{
  "ip": "8.8.8.8",
  "country_code": "US",
  "country_name": "United States of America",
  "region_name": "California",
  "district": "Santa Clara County",
  "city_name": "Mountain View",
  "latitude": 37.38605,
  "longitude": -122.08385,
  "zip_code": "94035",
  "time_zone": "-07:00",
  "asn": "15169",
  "as": "Google LLC",
  "as_info": {
    "as_number": "15169",
    "as_name": "Google LLC",
    "as_domain": "google.com",
    "as_usage_type": "DCH",
    "as_cidr": "8.8.8.0/24"
  },
  "isp": "Google LLC",
  "domain": "google.com",
  "net_speed": "T1",
  "idd_code": "1",
  "area_code": "650",
  "weather_station_code": "USCA0746",
  "weather_station_name": "Mountain View",
  "mcc": "-",
  "mnc": "-",
  "mobile_brand": "-",
  "elevation": 32,
  "usage_type": "DCH",
  "address_type": "Anycast",
  "ads_category": "IAB19-11",
  "ads_category_name": "Data Centers",
  "continent": {
    "name": "North America",
    "code": "NA",
    "hemisphere": [
      "north",
      "west"
    ],
    "translation": {
      "lang": "ko",
      "value": "북아메리카"
    }
  },
  "country": {
    "name": "United States of America",
    "alpha3_code": "USA",
    "numeric_code": 840,
    "demonym": "Americans",
    "flag": "https://cdn.ip2location.io/assets/img/flags/us.png",
    "capital": "Washington, D.C.",
    "total_area": 9826675,
    "population": 339665118,
    "currency": {
      "code": "USD",
      "name": "United States Dollar",
      "symbol": "$"
    },
    "language": {
      "code": "EN",
      "name": "English"
    },
    "tld": "us",
    "translation": {
      "lang": "ko",
      "value": "미국"
    }
  },
  "region": {
    "name": "California",
    "code": "US-CA",
    "translation": {
      "lang": "ko",
      "value": "캘리포니아주"
    }
  },
  "city": {
    "name": "Mountain View",
    "translation": {
      "lang": null,
      "value": null
    }
  },
  "time_zone_info": {
    "olson": "America/Los_Angeles",
    "current_time": "2026-04-29T23:36:52-07:00",
    "gmt_offset": -25200,
    "is_dst": true,
    "abbreviation": "PDT",
    "dst_start_date": "2026-03-08",
    "dst_end_date": "2026-11-01",
    "sunrise": "06:12",
    "sunset": "19:58"
  },
  "geotargeting": {
    "metro": "807"
  },
  "is_proxy": false,
  "fraud_score": 0,
  "proxy": {
    "last_seen": 1,
    "proxy_type": "DCH",
    "threat": "-",
    "provider": "-",
    "is_vpn": false,
    "is_tor": false,
    "is_data_center": true,
    "is_public_proxy": false,
    "is_web_proxy": false,
    "is_web_crawler": false,
    "is_ai_crawler": false,
    "is_residential_proxy": false,
    "is_consumer_privacy_network": false,
    "is_enterprise_private_network": false,
    "is_spammer": false,
    "is_scanner": false,
    "is_botnet": false,
    "is_bogon": false
  }
}
</pre>

### Configuration variables

This table lists the configuration variables required to operate IP2Location IO. These variables are specified when configuring a IP2Location.io asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api_key** | required | password | IP2Location.io API key |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration <br>
[geolocate ip](#action-geolocate-ip) - Queries IP2Location.io API for geolocation info

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** <br>
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'geolocate ip'

Queries IP2Location.io API for geolocation info

Type: **investigate** <br>
Read only: **True**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** | required | IP to lookup | string | `ip` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip | string | `ip` | |
action_result.status | string | | success failed |
action_result.data | string | | |
action_result.summary | string | | |
action_result.message | string | | |
summary.total_objects | numeric | | |
summary.total_objects_successful | numeric | | |

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2026 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
