TextFormatType:
==
TextFormatType defines the information for describing a full range of text formats and may place restrictions on the values of the other attributes, referred to as "facets".  

Attributes: 
--
textType?, isSequence?, interval?, startValue?, endValue?, timeInterval?, startTime?, endTime?, minLength?, maxLength?, minValue?, maxValue?, decimals?, pattern?, isMultiLingual?

Content:
--
SentinelValue*

Attribute Documentation: 
--
| Name | Type	| Documentation |
| :---- | :---- | :------------- |
| textType (default: String) | DataType | The textType attribute provides a description of the datatype. If it is not specified, any valid characters may be included in the text field (it corresponds to the xs:string datatype of W3C XML Schema) within the constraints of the facets.|
| isSequence | [xs:boolean](https://www.w3.org/TR/xmlschema-2/#boolean) | The isSequence attribute indicates whether the values are intended to be ordered, and it may work in combination with the interval, startValue, and endValue attributes or the timeInterval, startTime, and endTime, attributes. If this attribute holds a value of true, a start value or time and a numeric or time interval must supplied. If an end value is not given, then the sequence continues indefinitely.| 
| interval | [xs:decimal](https://www.w3.org/TR/xmlschema-2/#decimal) | The interval attribute specifies the permitted interval (increment) in a sequence. In order for this to be used, the isSequence attribute must have a value of true.|
| startValue | [xs:decimal](https://www.w3.org/TR/xmlschema-2/#decimal) | The startValue attribute is used in conjunction with the isSequence and interval attributes (which must be set in order to use this attribute). This attribute is used for a numeric sequence, and indicates the starting point of the sequence. This value is mandatory for a numeric sequence to be expressed. |
| endValue | [xs:decimal](https://www.w3.org/TR/xmlschema-2/#decimal) | The endValue attribute is used in conjunction with the isSequence and interval attributes (which must be set in order to use this attribute). This attribute is used for a numeric sequence, and indicates that ending point (if any) of the sequence. |
| timeInterval | [xs:duration](https://www.w3.org/TR/xmlschema-2/#duration) | The timeInterval attribute indicates the permitted duration in a time sequence. In order for this to be used, the isSequence attribute must have a value of true.| 
| startTime | StandardTimePeriodType | The startTime attribute is used in conjunction with the isSequence and timeInterval attributes (which must be set in order to use this attribute). This attribute is used for a time sequence, and indicates the start time of the sequence. This value is mandatory for a time sequence to be expressed. |
| endTime | StandardTimePeriodType | The endTime attribute is used in conjunction with the isSequence and timeInterval attributes (which must be set in order to use this attribute). This attribute is used for a time sequence, and indicates that ending point (if any) of the sequence. |
| minLength | [xs:positiveInteger](https://www.w3.org/TR/xmlschema-2/#positiveInteger) | The minLength attribute specifies the minimum and length of the value in characters.|
| maxLength | [xs:positiveInteger](https://www.w3.org/TR/xmlschema-2/#positiveInteger) | The maxLength attribute specifies the maximum length of the value in characters.|
| minValue | [xs:decimal](https://www.w3.org/TR/xmlschema-2/#decimal) | The minValue attribute is used for inclusive and exclusive ranges, indicating what the lower bound of the range is. If this is used with an inclusive range, a valid value will be greater than or equal to the value specified here. If the inclusive and exclusive data type is not specified (e.g. this facet is used with an integer data type), the value is assumed to be inclusive. |
| maxValue | [xs:decimal](https://www.w3.org/TR/xmlschema-2/#decimal) | The maxValue attribute is used for inclusive and exclusive ranges, indicating what the upper bound of the range is. If this is used with an inclusive range, a valid value will be less than or equal to the value specified here. If the inclusive and exclusive data type is not specified (e.g. this facet is used with an integer data type), the value is assumed to be inclusive.| 
| decimals | [xs:positiveInteger](https://www.w3.org/TR/xmlschema-2/#positiveInteger) | The decimals attribute indicates the number of characters allowed after the decimal separator.|
| pattern | [xs:string](https://www.w3.org/TR/xmlschema-2/#string) | The pattern attribute holds any regular expression permitted in the similar facet in W3C XML Schema.|
| isMultiLingual (default: true) | [xs:boolean](https://www.w3.org/TR/xmlschema-2/#boolean) | The isMultiLingual attribute indicates for a text format of type "string", whether the value should allow for multiple values in different languages.|

Element Documentation:
--
| Name | Type	| Documentation |
| :---- | :---- | :------------- |
| SentinelValue | [SentinelValueType](SentinelValueType.md) |SentinelValue defines a value that has a special meaning within the text format representation of a component.|
