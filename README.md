# ServiceNow Steps

---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [ServiceNowSteps.zip](ServiceNowSteps.zip) - Workflow zip file with the step and example flow
* [ServiceNow_Logo.png](ServiceNow_Logo.png) - ServiceNow logo

# How it works
These steps can be used to perform various actions against ServiceNow
- Get Record - get a specific record from a table and output specified column values
- Get Recent Incidents - get recent incidents that match certain criteria
- Get Recent Changes - get recent changes that match certain criteria

# Installation

## xMatters Setup
1. Download the [ServiceNowSteps.zip](ServiceNowSteps.zip) file onto your local computer
2. Navigate to the Workflows in your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
### ServiceNow - Get Record
The **ServiceNow - Get Record** step can be used to query for a record in a specified table and return several values from the specified table columns.

#### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| sys_id | Yes | 0 | 2000 | ID of record | | No |
| Table | Yes | 0 | 2000 | Name of the ServiceNow table | | No |
| Output 1 Column Name | No | 0 | 2000 | Name of field to return to Output 1 | | No |
| Output 2 Column Name | No | 0 | 2000 | Name of field to return to Output 2 | | No |
| Output 3 Column Name | No | 0 | 2000 | Name of field to return to Output 3 | | No |
| Output 4 Column Name | No | 0 | 2000 | Name of field to return to Output 4 | | No |
| Output 5 Column Name | No | 0 | 2000 | Name of field to return to Output 5 | | No |

#### Outputs

| Name | Description |
| ---- | ----------  |
| Raw Record | Raw value of returned record |
| Output 1 | output value from column set in *Output 1 Column Name* |
| Output 2 | output value from column set in *Output 2 Column Name* |
| Output 3 | output value from column set in *Output 3 Column Name* |
| Output 4 | output value from column set in *Output 4 Column Name* |
| Output 5 | output value from column set in *Output 5 Column Name* |

---

### ServiceNow - Get Recent Incidents
The **ServiceNow - Get Recent Incidents** step can be used to query ServiceNow for incidents that match a value in a porperty like *cmdb_ci.name* in the last X days. 

#### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| ServiceNow Property Name | No | 0 | 20000 |The ServiceNow incident property you want to search like cmdb_ci.name | cmdb_ci.name | No |
| ServiceNow Property Value | No | 0 | 20000 | The value of the ServiceNow incident property you want to match | | No |
| Max Incidents | No | 0 | 3 | Max number of incidents to return | 5 | No |
| Days Back | No | 0 | 3 | Number of days back to search for related incidents | 30 | No |
| Exclude Incident | No | 0 | 2000 | Incident number to exclude from the results | | No |
| ServiceNow URL | No | 0 | 20000 | Base URL for the ServiceNow instance used to build the links to the incident records (https://<instance_name>.service-now.com) | | No |

#### Outputs

| Name | Description |
| ---- | ----------  |
| Recent Incidents | Text representation of recent incidents that were found |

---

### ServiceNow - Get Recent Changes
The **ServiceNow - Get Recent Changes** step can be used to query ServiceNow for changes that match a value in a porperty like *cmdb_ci.name* in the last X days. 

#### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| ServiceNow Property Name | No | 0 | 20000 |The ServiceNow incident property you want to search like cmdb_ci.name | cmdb_ci.name | No |
| ServiceNow Property Value | No | 0 | 20000 | The value of the ServiceNow incident property you want to match | | No |
| Max Changes | No | 0 | 3 | Max number of changes to return | 5 | No |
| Days Back | No | 0 | 3 | Number of days back to search for related changes | 30 | No |
| ServiceNow URL | No | 0 | 20000 | Base URL for the ServiceNow instance used to build the links to the changes records (https://<instance_name>.service-now.com) | | No |

#### Outputs

| Name | Description |
| ---- | ----------  |
| Recent Changes | Text representation of recent changes that were found |