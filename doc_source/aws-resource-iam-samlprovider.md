# AWS::IAM::SAMLProvider<a name="aws-resource-iam-samlprovider"></a>

Creates an IAM resource that describes an identity provider \(IdP\) that supports SAML 2\.0\.

The SAML provider resource that you create with this operation can be used as a principal in an IAM role's trust policy\. Such a policy can enable federated users who sign in using the SAML IdP to assume the role\. You can create an IAM role that supports Web\-based single sign\-on \(SSO\) to the AWS Management Console or one that supports API access to AWS\.

When you create the SAML provider resource, you upload a SAML metadata document that you get from your IdP\. That document includes the issuer's name, expiration information, and keys that can be used to validate the SAML authentication response \(assertions\) that the IdP sends\. You must generate the metadata document using the identity management software that is used as your organization's IdP\.

**Note**  
 This operation requires [Signature Version 4](https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html)\.

 For more information, see [Enabling SAML 2\.0 federated users to access the AWS Management Console](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_enable-console-saml.html) and [About SAML 2\.0\-based federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html) in the *IAM User Guide*\.

## Syntax<a name="aws-resource-iam-samlprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-samlprovider-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::SAMLProvider",
  "Properties" : {
      "[Name](#cfn-iam-samlprovider-name)" : String,
      "[SamlMetadataDocument](#cfn-iam-samlprovider-samlmetadatadocument)" : String,
      "[Tags](#cfn-iam-samlprovider-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iam-samlprovider-syntax.yaml"></a>

```
Type: AWS::IAM::SAMLProvider
Properties: 
  [Name](#cfn-iam-samlprovider-name): String
  [SamlMetadataDocument](#cfn-iam-samlprovider-samlmetadatadocument): String
  [Tags](#cfn-iam-samlprovider-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iam-samlprovider-properties"></a>

`Name`  <a name="cfn-iam-samlprovider-name"></a>
The name of the provider to create\.  
This parameter allows \(through its [regex pattern](http://wikipedia.org/wiki/regex)\) a string of characters consisting of upper and lowercase alphanumeric characters with no spaces\. You can also include any of the following characters: \_\+=,\.@\-  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w._-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SamlMetadataDocument`  <a name="cfn-iam-samlprovider-samlmetadatadocument"></a>
An XML document generated by an identity provider \(IdP\) that supports SAML 2\.0\. The document includes the issuer's name, expiration information, and keys that can be used to validate the SAML authentication response \(assertions\) that are received from the IdP\. You must generate the metadata document using the identity management software that is used as your organization's IdP\.  
For more information, see [About SAML 2\.0\-based federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html) in the *IAM User Guide*   
*Required*: Yes  
*Type*: String  
*Minimum*: `1000`  
*Maximum*: `10000000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iam-samlprovider-tags"></a>
A list of tags that you want to attach to the new IAM SAML provider\. Each tag consists of a key name and an associated value\. For more information about tagging, see [Tagging IAM resources](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.  
If any one of the tags is invalid or if you exceed the allowed maximum number of tags, then the entire request fails and the resource is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-samlprovider-return-values"></a>

### Ref<a name="aws-resource-iam-samlprovider-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iam-samlprovider-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iam-samlprovider-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::IAM::SAMLProvider` resource\.