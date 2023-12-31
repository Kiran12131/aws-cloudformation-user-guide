# AWS::ElasticBeanstalk::Environment OptionSetting<a name="aws-properties-elasticbeanstalk-environment-optionsetting"></a>

The `OptionSetting` property type specifies an option for an AWS Elastic Beanstalk environment\.

The `OptionSettings` property of the [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html) resource contains a list of `OptionSetting` property types\.

For a list of possible namespaces and option values, see [Option Values](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.

## Syntax<a name="aws-properties-elasticbeanstalk-environment-optionsetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticbeanstalk-environment-optionsetting-syntax.json"></a>

```
{
  "[Namespace](#cfn-elasticbeanstalk-environment-optionsetting-namespace)" : String,
  "[OptionName](#cfn-elasticbeanstalk-environment-optionsetting-optionname)" : String,
  "[ResourceName](#cfn-elasticbeanstalk-environment-optionsetting-resourcename)" : String,
  "[Value](#cfn-elasticbeanstalk-environment-optionsetting-value)" : String
}
```

### YAML<a name="aws-properties-elasticbeanstalk-environment-optionsetting-syntax.yaml"></a>

```
  [Namespace](#cfn-elasticbeanstalk-environment-optionsetting-namespace): String
  [OptionName](#cfn-elasticbeanstalk-environment-optionsetting-optionname): String
  [ResourceName](#cfn-elasticbeanstalk-environment-optionsetting-resourcename): String
  [Value](#cfn-elasticbeanstalk-environment-optionsetting-value): String
```

## Properties<a name="aws-properties-elasticbeanstalk-environment-optionsetting-properties"></a>

`Namespace`  <a name="cfn-elasticbeanstalk-environment-optionsetting-namespace"></a>
A unique namespace that identifies the option's associated AWS resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionName`  <a name="cfn-elasticbeanstalk-environment-optionsetting-optionname"></a>
The name of the configuration option\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceName`  <a name="cfn-elasticbeanstalk-environment-optionsetting-resourcename"></a>
A unique resource name for the option setting\. Use it for a time–based scaling configuration option\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-elasticbeanstalk-environment-optionsetting-value"></a>
The current value for the configuration option\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-elasticbeanstalk-environment-optionsetting--seealso"></a>
+  [ConfigurationOptionSetting](https://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_ConfigurationOptionSetting.html) in the *AWS Elastic Beanstalk API Reference* 
+  [Configuration Options](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide* 