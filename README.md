# ServiceNow Steps

This step allows you to get an incident from a table in ServiceNow.

---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [ServiceNowSteps.zip](ServiceNowSteps.zip) - Workflow zip file with the step and example flow
* [servicenow.png](/servicenow.png) - ServiceNow logo

# How it works
This step uses a ServiceNow endpoint to get a specific incident from a table in ServiceNow.


# Installation

## xMatters Setup
1. Download the [ServiceNowSteps.zip](ServiceNowSteps.zip) file onto your local computer
2. Navigate to the Developer tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
The **ServiceNow - Get Record** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **ServiceNow Steps** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| sys_id | Yes | 0 | 2000 | ID of incident | | No |
| table | Yes | 0 | 2000 | Name of the ServiceNow table | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| sys_id | ID of incident |
| record | JSON representation of all data associated with incident |


## Example
This is an example of getting a certain ServiceNow Record on an HTTP Trigger.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

