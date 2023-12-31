# AWS::RDS::OptionGroup OptionConfiguration<a name="aws-properties-rds-optiongroup-optionconfiguration"></a>

The `OptionConfiguration` property type specifies an individual option, and its settings, within an `AWS::RDS::OptionGroup` resource\.

## Syntax<a name="aws-properties-rds-optiongroup-optionconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rds-optiongroup-optionconfiguration-syntax.json"></a>

```
{
  "[DBSecurityGroupMemberships](#cfn-rds-optiongroup-optionconfiguration-dbsecuritygroupmemberships)" : [ String, ... ],
  "[OptionName](#cfn-rds-optiongroup-optionconfiguration-optionname)" : String,
  "[OptionSettings](#cfn-rds-optiongroup-optionconfiguration-optionsettings)" : [ OptionSetting, ... ],
  "[OptionVersion](#cfn-rds-optiongroup-optionconfiguration-optionversion)" : String,
  "[Port](#cfn-rds-optiongroup-optionconfiguration-port)" : Integer,
  "[VpcSecurityGroupMemberships](#cfn-rds-optiongroup-optionconfiguration-vpcsecuritygroupmemberships)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-rds-optiongroup-optionconfiguration-syntax.yaml"></a>

```
  [DBSecurityGroupMemberships](#cfn-rds-optiongroup-optionconfiguration-dbsecuritygroupmemberships): 
    - String
  [OptionName](#cfn-rds-optiongroup-optionconfiguration-optionname): String
  [OptionSettings](#cfn-rds-optiongroup-optionconfiguration-optionsettings): 
    - OptionSetting
  [OptionVersion](#cfn-rds-optiongroup-optionconfiguration-optionversion): String
  [Port](#cfn-rds-optiongroup-optionconfiguration-port): Integer
  [VpcSecurityGroupMemberships](#cfn-rds-optiongroup-optionconfiguration-vpcsecuritygroupmemberships): 
    - String
```

## Properties<a name="aws-properties-rds-optiongroup-optionconfiguration-properties"></a>

`DBSecurityGroupMemberships`  <a name="cfn-rds-optiongroup-optionconfiguration-dbsecuritygroupmemberships"></a>
A list of DBSecurityGroupMembership name strings used for this option\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionName`  <a name="cfn-rds-optiongroup-optionconfiguration-optionname"></a>
The configuration of options to include in a group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionSettings`  <a name="cfn-rds-optiongroup-optionconfiguration-optionsettings"></a>
The option settings to include in an option group\.  
*Required*: No  
*Type*: List of [OptionSetting](aws-properties-rds-optiongroup-optionsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionVersion`  <a name="cfn-rds-optiongroup-optionconfiguration-optionversion"></a>
The version for the option\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-rds-optiongroup-optionconfiguration-port"></a>
The optional port for the option\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupMemberships`  <a name="cfn-rds-optiongroup-optionconfiguration-vpcsecuritygroupmemberships"></a>
A list of VpcSecurityGroupMembership name strings used for this option\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-rds-optiongroup-optionconfiguration--examples"></a>



### <a name="aws-properties-rds-optiongroup-optionconfiguration--examples--"></a>

The following example template uses `OptionName` and `OptionVersion` parameters when creating an `AWS::RDS::OptionGroup` resource\. 

#### JSON<a name="aws-properties-rds-optiongroup-optionconfiguration--examples----json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "APEX has a dependency on XMLDB, so, there must be at least one XMLDB when there is an APEX",
    "Parameters": {
        "OptionName": {
            "Type": "String"
        },
        "OptionVersion": {
            "Type": "String"
        }
    },
    "Resources": {
        "myOptionGroup": {
            "Type": "AWS::RDS::OptionGroup",
            "Properties": {
                "EngineName": "oracle-ee",
                "MajorEngineVersion": "11.2",
                "OptionGroupDescription": "testing creating optionGroup with APEX version",
                "OptionConfigurations": [
                    {
                        "OptionName": "XMLDB"
                    },
                    {
                        "OptionName": {
                            "Ref": "OptionName"
                        },
                        "OptionVersion": {
                            "Ref": "OptionVersion"
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-rds-optiongroup-optionconfiguration--examples----yaml"></a>

```
--- 
AWSTemplateFormatVersion: 2010-09-09
Description: "APEX has a dependency on XMLDB, so, there must be at least one XMLDB when there is an APEX"
Parameters: 
  OptionName: 
    Type: String
  OptionVersion: 
    Type: String
Resources: 
  myOptionGroup: 
    Properties: 
      EngineName: oracle-ee
      MajorEngineVersion: "11.2"
      OptionConfigurations: 
        - 
          OptionName: XMLDB
        - 
          OptionName: OptionName
          OptionVersion: OptionVersion
      OptionGroupDescription: "testing creating optionGroup with APEX version"
    Type: "AWS::RDS::OptionGroup"
```