# ServiceNow Steps

This step allows you to get a record from a table in ServiceNow.

---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [ServiceNowSteps.zip](ServiceNowSteps.zip) - Workflow zip file with the step and example flow
* [servicenow.jpg](/servicenow.jpg) - ServiceNow logo

# How it works
This step uses a ServiceNow endpoint to get a specific record from a table in ServiceNow. Inputs can be specified for specific fields of the record to be returned. Invalid inputs will produce output in the log.


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
| sys_id | Yes | 0 | 2000 | ID of record | | No |
| table | Yes | 0 | 2000 | Name of the ServiceNow table | | No |
| input_0 | No | 0 | 2000 | Name of field to return to output_0 | | No |
| input_1 | No | 0 | 2000 | Name of field to return to output_1 | | No |
| input_2 | No | 0 | 2000 | Name of field to return to output_2 | | No |
| input_3 | No | 0 | 2000 | Name of field to return to output_3 | | No |
| input_4 | No | 0 | 2000 | Name of field to return to output_4 | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| record | JSON representation of all data associated with record |
| output_0 | output from input_0 value of request |
| output_1 | output from input_1 value of request |
| output_2 | output from input_2 value of request |
| output_3 | output from input_3 value of request |
| output_4 | output from input_4 value of request |


## Example
This is an example of getting a certain ServiceNow Record on an HTTP Trigger.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

