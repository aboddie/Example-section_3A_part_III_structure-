SentinelValueType
==
SentinelValueType defines the structure of a sentinel value. A sentinel is a value that has a special meaning within the text format representation of a component. The value is associated with a multi-lingual name and description.  

Attributes:
--
value  

Content:  
--
Name+, Description*  

Attribute Documentation:
--
| Name | Type	| Documentation |
| :---- | :---- | :------------- |
| value	| [xs:anySimpleType](https://www.w3.org/TR/xmlschema-2/#rf-defn) | The sentinel value being described. |  

Element Documentation: 
--
| Name | Type	| Documentation |
| :---- | :---- | :------------- |
| Name	| TextType |	Name is a reusable element, used for providing a human-readable name for an object. |
|Description | TextType |	Description is a reusable element, used for providing a longer human-readable description of an object. |
