# AWS::ApiGateway::BasePathMapping<a name="aws-resource-apigateway-basepathmapping"></a>

The `AWS::ApiGateway::BasePathMapping` resource creates a base path that clients who call your API must use in the invocation URL\.

## Syntax<a name="aws-resource-apigateway-basepathmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-basepathmapping-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::BasePathMapping",
  "Properties" : {
      "[BasePath](#cfn-apigateway-basepathmapping-basepath)" : String,
      "[DomainName](#cfn-apigateway-basepathmapping-domainname)" : String,
      "[Id](#cfn-apigateway-basepathmapping-id)" : String,
      "[RestApiId](#cfn-apigateway-basepathmapping-restapiid)" : String,
      "[Stage](#cfn-apigateway-basepathmapping-stage)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-basepathmapping-syntax.yaml"></a>

```
Type: AWS::ApiGateway::BasePathMapping
Properties: 
  [BasePath](#cfn-apigateway-basepathmapping-basepath): String
  [DomainName](#cfn-apigateway-basepathmapping-domainname): String
  [Id](#cfn-apigateway-basepathmapping-id): String
  [RestApiId](#cfn-apigateway-basepathmapping-restapiid): String
  [Stage](#cfn-apigateway-basepathmapping-stage): String
```

## Properties<a name="aws-resource-apigateway-basepathmapping-properties"></a>

`BasePath`  <a name="cfn-apigateway-basepathmapping-basepath"></a>
The base path name that callers of the API must provide as part of the URL after the domain name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainName`  <a name="cfn-apigateway-basepathmapping-domainname"></a>
The domain name of the BasePathMapping resource to be described\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Id`  <a name="cfn-apigateway-basepathmapping-id"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RestApiId`  <a name="cfn-apigateway-basepathmapping-restapiid"></a>
The string identifier of the associated RestApi\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-apigateway-basepathmapping-stage"></a>
The name of the associated stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-resource-apigateway-basepathmapping--seealso"></a>
+ [basepathmapping:create](https://docs.aws.amazon.com/apigateway/latest/api/API_CreateBasePathMapping.html) in the *Amazon API Gateway REST API Reference*

