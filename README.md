[comment]: # "Auto-generated SOAR connector documentation"
# IP2Location IO

Publisher: IP2Location.io  
Connector Version: 1.0.1  
Product Vendor: IP2Location.io  
Product Name: IP2Location.io  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 6.1.1  

Query IP geolocation data from IP2Location.io API

# IP2Location IO

Publisher: IP2Location.io
Contributors: IP2Location.io
App Version: 1.0.0
Product Vendor: IP2Location.io
Product Name: IP2Location.io
Product Version Supported (regex): ".*"

Query IP geolocation data from IP2Location.io API.

Get free IP2Location.io API from from https://www.ip2location.io/pricing for basic geolocation data.
Below is an example output if you're subscribed to the Security plan.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a IP2Location.io asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api_key** |  required  | password | IP2Location.io API key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[geolocate ip](#action-geolocate-ip) - Queries IP2Location.io API for geolocation info  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'geolocate ip'
Queries IP2Location.io API for geolocation info

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP to lookup | string |  `ip` 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip | string |  `ip`  |  
action_result.status | string |  |   success  failed 
action_result.data | string |  |  
action_result.summary | string |  |  
action_result.message | string |  |  
summary.total_objects | numeric |  |  
summary.total_objects_successful | numeric |  |  