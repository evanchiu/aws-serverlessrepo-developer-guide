# Applications applicationId<a name="applications-applicationid"></a>

## URI<a name="applications-applicationid-url"></a>

 /applications/ *applicationId* 

## HTTP Methods<a name="applications-applicationid-http-methods"></a>

### GET<a name="applications-applicationidget"></a>

Operation ID: GetApplication 

Gets the specified application\.


**Path Parameters**  

| Name | Type | Required | Description | 
| --- |--- |--- |--- |
|  applicationId  | String | True |  The Amazon Resource Name \(ARN\) of the application\.  | 


**Query Parameters**  

| Name | Type | Required | Description | 
| --- |--- |--- |--- |
|  semanticVersion  | String | False |  The semantic version of the application to get\.  | 


**Responses**  

| Status Code | Response Model | Description | 
| --- |--- |--- |
|  200  |   [Application](#applications-applicationid-response-body-application-example)   |  Success  | 
|  400  |   [BadRequestException](#applications-applicationid-response-body-badrequestexception-example)   |  One of the parameters in the request is invalid\.  | 
|  500  |   [InternalServerErrorException](#applications-applicationid-response-body-internalservererrorexception-example)   |  The AWS Serverless Application Repository service encountered an internal error\.  | 
|  403  |   [ForbiddenException](#applications-applicationid-response-body-forbiddenexception-example)   |  The client is not authenticated\.  | 
|  404  |   [NotFoundException](#applications-applicationid-response-body-notfoundexception-example)   |  The resource \(for example, an access policy statement\) specified in the request doesn't exist\.  | 
|  429  |   [TooManyRequestsException](#applications-applicationid-response-body-toomanyrequestsexception-example)   |  The client is sending more than the allowed number of requests per unit of time\.  | 

### DELETE<a name="applications-applicationiddelete"></a>

Operation ID: DeleteApplication 

Deletes the specified application\.


**Path Parameters**  

| Name | Type | Required | Description | 
| --- |--- |--- |--- |
|  applicationId  | String | True |  The Amazon Resource Name \(ARN\) of the application\.  | 


**Responses**  

| Status Code | Response Model | Description | 
| --- |--- |--- |
|  400  |   [BadRequestException](#applications-applicationid-response-body-badrequestexception-example)   |  One of the parameters in the request is invalid\.  | 
|  500  |   [InternalServerErrorException](#applications-applicationid-response-body-internalservererrorexception-example)   |  The AWS Serverless Application Repository service encountered an internal error\.  | 
|  204  | None |  Success  | 
|  403  |   [ForbiddenException](#applications-applicationid-response-body-forbiddenexception-example)   |  The client is not authenticated\.  | 
|  404  |   [NotFoundException](#applications-applicationid-response-body-notfoundexception-example)   |  The resource \(for example, an access policy statement\) specified in the request doesn't exist\.  | 
|  429  |   [TooManyRequestsException](#applications-applicationid-response-body-toomanyrequestsexception-example)   |  The client is sending more than the allowed number of requests per unit of time\.  | 
|  409  |   [ConflictException](#applications-applicationid-response-body-conflictexception-example)   |  The resource already exists\.  | 

### PATCH<a name="applications-applicationidpatch"></a>

Operation ID: UpdateApplication 

Updates the specified application\.


**Path Parameters**  

| Name | Type | Required | Description | 
| --- |--- |--- |--- |
|  applicationId  | String | True |  The Amazon Resource Name \(ARN\) of the application\.  | 


**Responses**  

| Status Code | Response Model | Description | 
| --- |--- |--- |
|  200  |   [Application](#applications-applicationid-response-body-application-example)   |  Success  | 
|  400  |   [BadRequestException](#applications-applicationid-response-body-badrequestexception-example)   |  One of the parameters in the request is invalid\.  | 
|  500  |   [InternalServerErrorException](#applications-applicationid-response-body-internalservererrorexception-example)   |  The AWS Serverless Application Repository service encountered an internal error\.  | 
|  403  |   [ForbiddenException](#applications-applicationid-response-body-forbiddenexception-example)   |  The client is not authenticated\.  | 
|  404  |   [NotFoundException](#applications-applicationid-response-body-notfoundexception-example)   |  The resource \(for example, an access policy statement\) specified in the request doesn't exist\.  | 
|  429  |   [TooManyRequestsException](#applications-applicationid-response-body-toomanyrequestsexception-example)   |  The client is sending more than the allowed number of requests per unit of time\.  | 
|  409  |   [ConflictException](#applications-applicationid-response-body-conflictexception-example)   |  The resource already exists\.  | 

## Schemas<a name="applications-applicationid-schemas"></a>

### Request Bodies<a name="applications-applicationid-request-examples"></a>

#### Example PATCH<a name="applications-applicationid-request-body-patch-example"></a>

```
{
  "description": "string",
  "author": "string",
  "readmeBody": "string",
  "readmeUrl": "string",
  "labels": [
    "string"
  ],
  "homePageUrl": "string"
}
```

### Response Bodies<a name="applications-applicationid-response-examples"></a>

#### Example Application<a name="applications-applicationid-response-body-application-example"></a>

```
{
  "applicationId": "string",
  "name": "string",
  "description": "string",
  "author": "string",
  "spdxLicenseId": "string",
  "licenseUrl": "string",
  "readmeUrl": "string",
  "labels": [
    "string"
  ],
  "creationTime": "string",
  "homePageUrl": "string",
  "version": {
    "applicationId": "string",
    "semanticVersion": "string",
    "sourceCodeUrl": "string",
    "templateUrl": "string",
    "creationTime": "string",
    "parameterDefinitions": [
      {
        "name": "string",
        "defaultValue": "string",
        "description": "string",
        "type": "string",
        "noEcho": boolean,
        "allowedPattern": "string",
        "constraintDescription": "string",
        "minValue": integer,
        "maxValue": integer,
        "minLength": integer,
        "maxLength": integer,
        "allowedValues": [
          "string"
        ],
        "referencedByResources": [
          "string"
        ]
      }
    ]
  }
}
```

#### Example BadRequestException<a name="applications-applicationid-response-body-badrequestexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

#### Example ForbiddenException<a name="applications-applicationid-response-body-forbiddenexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

#### Example NotFoundException<a name="applications-applicationid-response-body-notfoundexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

#### Example ConflictException<a name="applications-applicationid-response-body-conflictexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

#### Example TooManyRequestsException<a name="applications-applicationid-response-body-toomanyrequestsexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

#### Example InternalServerErrorException<a name="applications-applicationid-response-body-internalservererrorexception-example"></a>

```
{
  "message": "string",
  "errorCode": "string"
}
```

## Properties<a name="applications-applicationid-properties"></a>


**Application**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   applicationId  |  string  | True |  The application Amazon Resource Name \(ARN\)\.  | 
|   name  |  string  | True |  The name of the application\. Minimum length=1\. Maximum length=140 Pattern: "\[a\-zA\-Z0\-9\\\\\-\]\+";  | 
|   description  |  string  | True |  The description of the application\. Minimum length=1\. Maximum length=256  | 
|   author  |  string  | True |  The name of the author publishing the app\. Minimum length=1\. Maximum length=127\. Pattern "^\[a\-z0\-9\]\(\(\[a\-z0\-9\]\|\-\(?\!\-\)\)\*\[a\-z0\-9\]\)?$";  | 
|   spdxLicenseId  |  string  | False |  A valid identifier from https://spdx\.org/licenses/\.  | 
|   licenseUrl  |  string  | False |  A link to a license file of the app that matches the spdxLicenseID value of your application\. Maximum size 5 MB  | 
|   readmeUrl  |  string  | False |  A link to the readme file in Markdown language that contains a more detailed description of the application and how it works\. Maximum size 5 MB  | 
|   labels  |  Array of type string   | False |  Labels to improve discovery of apps in search results\. Minimum length=1\. Maximum length=127\. Maximum number of labels: 10 Pattern: "^\[a\-zA\-Z0\-9\+\\\\\-\_:\\\\/@\]\+$";  | 
|   creationTime  |  string  | False |  The date and time this resource was created\.  | 
|   homePageUrl  |  string  | False |  A URL with more information about the application, for example the location of your GitHub repository for the application\.  | 
|   version  |   [Version](#applications-applicationid-version)   | False |  Version information about the application\.  | 


**BadRequestException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  One of the parameters in the request is invalid\.  | 
|   errorCode  |  string  | False |  400  | 


**ConflictException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  The resource already exists\.  | 
|   errorCode  |  string  | False |  409  | 


**ForbiddenException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  The client is not authenticated\.  | 
|   errorCode  |  string  | False |  403  | 


**InternalServerErrorException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  The AWS Serverless Application Repository service encountered an internal error\.  | 
|   errorCode  |  string  | False |  500  | 


**NotFoundException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  The resource \(for example, an access policy statement\) specified in the request doesn't exist\.  | 
|   errorCode  |  string  | False |  404  | 


**ParameterDefinition**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   name  |  string  | True |  The name of the parameter\.  | 
|   defaultValue  |  string  | False |  A value of the appropriate type for the template to use if no value is specified when a stack is created\. If you define constraints for the parameter, you must specify a value that adheres to those constraints\.  | 
|   description  |  string  | False |  A string of up to 4,000 characters that describes the parameter\.  | 
|   type  |  string  | False |  The type of the parameter\. Valid values: `String \| Number \| List<Number> \| CommaDelimitedList`   `String`: A literal string\. For example, users can specify `"MyUserName"`\.  `Number`: An integer or float\. AWS CloudFormation validates the parameter value as a number\. However, when you use the parameter elsewhere in your template \(for example, by using the `Ref` intrinsic function\), the parameter value becomes a string\. For example, users might specify `"8888"`\.  `List<Number>`: An array of integers or floats that are separated by commas\. AWS CloudFormation validates the parameter value as numbers\. However, when you use the parameter elsewhere in your template \(for example, by using the `Ref` intrinsic function\), the parameter value becomes a list of strings\. For example, users might specify "80,20", and then `Ref` results in `["80","20"]`\.  `CommaDelimitedList`: An array of literal strings that are separated by commas\. The total number of strings should be one more than the total number of commas\. Also, each member string is space\-trimmed\. For example, users might specify "test,dev,prod", and then `Ref` results in `["test","dev","prod"]`\.  | 
|   noEcho  |  boolean  | False |  Whether to mask the parameter value whenever anyone makes a call that describes the stack\. If you set the value to true, the parameter value is masked with asterisks \(\*\*\*\*\*\)\.  | 
|   allowedPattern  |  string  | False |  A regular expression that represents the patterns to allow for `String` types\.  | 
|   constraintDescription  |  string  | False |  A string that explains a constraint when the constraint is violated\. For example, without a constraint description, a parameter that has an allowed pattern of `[A-Za-z0-9]+` displays the following error message when the user specifies an invalid value:  `Malformed input-Parameter MyParameter must match pattern [A-Za-z0-9]+`  By adding a constraint description, such as "must contain only uppercase and lowercase letters and numbers," you can display the following customized error message:  `Malformed input-Parameter MyParameter must contain only uppercase and lowercase letters and numbers.`   | 
|   minValue  |  integer  | False |  A numeric value that determines the smallest numeric value that you want to allow for `Number` types\.  | 
|   maxValue  |  integer  | False |  A numeric value that determines the largest numeric value that you want to allow for `Number` types\.  | 
|   minLength  |  integer  | False |  An integer value that determines the smallest number of characters that you want to allow for `String` types\.  | 
|   maxLength  |  integer  | False |  An integer value that determines the largest number of characters that you want to allow for `String` types\.  | 
|   allowedValues  |  Array of type string   | False |  An array containing the list of values allowed for the parameter\.  | 
|   referencedByResources  |  Array of type string   | True |  A list of AWS SAM resources that use this parameter\.  | 


**TooManyRequestsException**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   message  |  string  | False |  The client is sending more than the allowed number of requests per unit of time\.  | 
|   errorCode  |  string  | False |  429  | 


**UpdateApplicationInput**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   description  |  string  | False |  The description of the application\. Minimum length=1\. Maximum length=256  | 
|   author  |  string  | False |  The name of the author publishing the app\. Minimum length=1\. Maximum length=127\. Pattern "^\[a\-z0\-9\]\(\(\[a\-z0\-9\]\|\-\(?\!\-\)\)\*\[a\-z0\-9\]\)?$";  | 
|   readmeBody  |  string  | False |  A text readme file in Markdown language that contains a more detailed description of the application and how it works\. Maximum size 5 MB  | 
|   readmeUrl  |  string  | False |  A link to the readme file in Markdown language that contains a more detailed description of the application and how it works\. Maximum size 5 MB  | 
|   labels  |  Array of type string   | False |  Labels to improve discovery of apps in search results\. Minimum length=1\. Maximum length=127\. Maximum number of labels: 10 Pattern: "^\[a\-zA\-Z0\-9\+\\\\\-\_:\\\\/@\]\+$";  | 
|   homePageUrl  |  string  | False |  A URL with more information about the application, for example the location of your GitHub repository for the application\.  | 


**Version**  

| Property | Type | Required | Description | 
| --- |--- |--- |--- |
|   applicationId  |  string  | True |  The application Amazon Resource Name \(ARN\)\.  | 
|   semanticVersion  |  string  | True |  The semantic version of the application:  [https://semver\.org/](https://semver.org/)   | 
|   sourceCodeUrl  |  string  | False |  A link to a public repository for the source code of your application\.  | 
|   templateUrl  |  string  | True |  A link to the packaged AWS SAM template of your application\.  | 
|   creationTime  |  string  | True |  The date and time this resource was created\.  | 
|   parameterDefinitions  |  Array of type  [ParameterDefinition](#applications-applicationid-parameterdefinition)    | True |  An array of parameter types supported by the application\.  | 