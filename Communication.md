# Communication Vocabulary
**Namespace: [com.sap.vocabularies.Communication.v1](Communication.xml)**

Terms for annotating communication-relevant information


These terms are inspired by
- RFC6350 vCard (http://tools.ietf.org/html/rfc6350)
- RFC5545 iCalendar (http://tools.ietf.org/html/rfc5545)
- RFC5322 Internet Message Format (http://tools.ietf.org/html/rfc5322)
- RFC6351 xCard: vCard XML Representation (https://tools.ietf.org/html/rfc6351)
        


## Terms

Term|Type|Description
:---|:---|:----------
[Contact](Communication.xml#L42)|[ContactType](#ContactType)|<a name="Contact"></a>Address book entry
[Address](Communication.xml#L126)|[AddressType](#AddressType)|<a name="Address"></a>Address
[IsEmailAddress](Communication.xml#L280)|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/master/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsEmailAddress"></a>Property contains an email address
[IsPhoneNumber](Communication.xml#L284)|[Tag](https://github.com/oasis-tcs/odata-vocabularies/blob/master/vocabularies/Org.OData.Core.V1.md#Tag)|<a name="IsPhoneNumber"></a>Property contains a phone number
[Event](Communication.xml#L288)|[EventData](#EventData)|<a name="Event"></a>Calendar entry
[Task](Communication.xml#L331)|[TaskData](#TaskData)|<a name="Task"></a>Task list entry
[Message](Communication.xml#L356)|[MessageData](#MessageData)|<a name="Message"></a>Email message

## <a name="ContactType"></a>[ContactType](Communication.xml#L45)


Property|Type|Description
:-------|:---|:----------
[fn](Communication.xml#L46)|String|Full name
[n](Communication.xml#L49)|[NameType](#NameType)|Name
[nickname](Communication.xml#L52)|String|Nickname
[photo](Communication.xml#L55)|URL|Image or photograph
[bday](Communication.xml#L59)|Date|Birthday
[anniversary](Communication.xml#L62)|Date|Date of marriage, or equivalent
[gender](Communication.xml#L65)|[GenderType](#GenderType)|Sex and gender identity
[title](Communication.xml#L69)|String|Position or job title
[role](Communication.xml#L72)|String|Function or part played in a particular situation
[org](Communication.xml#L75)|String|Organization Name defined by X.520
[orgunit](Communication.xml#L78)|String|Organization Unit defined by X.520
[kind](Communication.xml#L82)|[KindType](#KindType)|Kind of contact
[note](Communication.xml#L86)|String|Supplemental information or a comment associated with the contact
[adr](Communication.xml#L90)|\[[AddressType](#AddressType)\]|Addresses
[tel](Communication.xml#L93)|\[[PhoneNumberType](#PhoneNumberType)\]|Phone numbers
[email](Communication.xml#L96)|\[[EmailAddressType](#EmailAddressType)\]|Email addresses
[geo](Communication.xml#L99)|\[[GeoDataType](#GeoDataType)\]|Geographic locations
[url](Communication.xml#L102)|\[[UrlType](#UrlType)\]|URLs

## <a name="NameType"></a>[NameType](Communication.xml#L108)


Property|Type|Description
:-------|:---|:----------
[surname](Communication.xml#L109)|String|Surname or family name
[given](Communication.xml#L112)|String|Given name
[additional](Communication.xml#L115)|String|Additional names
[prefix](Communication.xml#L118)|String|Honorific prefix(es)
[suffix](Communication.xml#L121)|String|Honorific suffix(es)

## <a name="AddressType"></a>[AddressType](Communication.xml#L129)


Property|Type|Description
:-------|:---|:----------
[building](Communication.xml#L130)|String|Building identifier
[street](Communication.xml#L133)|String|Street address
[district](Communication.xml#L136)|String|Territorial administrative organization in a large city
[locality](Communication.xml#L139)|String|City or similar
[region](Communication.xml#L142)|String|State, province, or similar
[code](Communication.xml#L145)|String|Postal code
[country](Communication.xml#L148)|String|Country name
[pobox](Communication.xml#L152)|String|Post office box
[ext](Communication.xml#L155)|String|Extended address (e.g., apartment or suite number)
[careof](Communication.xml#L158)|String|An intermediary who is responsible for transferring a piece of mail between the postal system and the final addressee
[label](Communication.xml#L162)|String|Delivery address label; plain-text string representing the formatted address, may contain line breaks
[type](Communication.xml#L166)|[ContactInformationType](#ContactInformationType)|Address type

## <a name="PhoneNumberType"></a>[PhoneNumberType](Communication.xml#L171)


Property|Type|Description
:-------|:---|:----------
[uri](Communication.xml#L172)|URL|This SHOULD use the tel: URL schema defined in RFC3966
[type](Communication.xml#L176)|[PhoneType](#PhoneType)|Telephone type

## <a name="EmailAddressType"></a>[EmailAddressType](Communication.xml#L181)


Property|Type|Description
:-------|:---|:----------
[address](Communication.xml#L182)|String|Email address
[type](Communication.xml#L185)|[ContactInformationType](#ContactInformationType)|Address type

## <a name="GeoDataType"></a>[GeoDataType](Communication.xml#L190)


Property|Type|Description
:-------|:---|:----------
[uri](Communication.xml#L191)|URL|This SHOULD use the geo: URL schema defined in RFC5870 which encodes the same information as an Edm.GeographyPoint
[type](Communication.xml#L196)|[ContactInformationType](#ContactInformationType)|Address type

## <a name="UrlType"></a>[UrlType](Communication.xml#L201)


Property|Type|Description
:-------|:---|:----------
[uri](Communication.xml#L202)|URL|This MUST use the URL schema defined in RFC3986
[type](Communication.xml#L206)|[ContactInformationType](#ContactInformationType)|URL type

## <a name="KindType"></a>[KindType](Communication.xml#L211)


Member|Value|Description
:-----|----:|:----------
[individual](Communication.xml#L212)|0|A single person or entity
[group](Communication.xml#L215)|1|A group of persons or entities
[org](Communication.xml#L218)|2|An organization
[location](Communication.xml#L221)|3|A named geographical place

## <a name="ContactInformationType"></a>[ContactInformationType](Communication.xml#L226)


Flag Member|Value|Description
:-----|----:|:----------
[work](Communication.xml#L227)|1|Related to an individual's work place
[home](Communication.xml#L230)|2|Related to an indivdual's personal life
[preferred](Communication.xml#L233)|4|Preferred-use contact information

## <a name="PhoneType"></a>[PhoneType](Communication.xml#L238)


Flag Member|Value|Description
:-----|----:|:----------
[work](Communication.xml#L239)|1|Work telephone number
[home](Communication.xml#L242)|2|Private telephone number
[preferred](Communication.xml#L245)|4|Preferred-use telephone number
[voice](Communication.xml#L248)|8|Voice telephone number
[cell](Communication.xml#L251)|16|Cellular or mobile telephone number
[fax](Communication.xml#L254)|32|Facsimile telephone number
[video](Communication.xml#L257)|64|Video conferencing telephone number

## <a name="GenderType"></a>[GenderType](Communication.xml#L262)


Member|Value|Description
:-----|----:|:----------
[M](Communication.xml#L263)|0|male
[F](Communication.xml#L266)|1|female
[O](Communication.xml#L269)|2|other
[N](Communication.xml#L272)|3|not applicable
[U](Communication.xml#L275)|4|unknown

## <a name="EventData"></a>[EventData](Communication.xml#L292)


Property|Type|Description
:-------|:---|:----------
[summary](Communication.xml#L293)|String|Short description of the event
[description](Communication.xml#L296)|String|More complete description
[categories](Communication.xml#L299)|\[String\]|Categories or subtypes of the event
[dtstart](Communication.xml#L302)|DateTimeOffset|Start date and time of the event
[dtend](Communication.xml#L305)|DateTimeOffset|Date and time by which the event ends, alternative to duration
[duration](Communication.xml#L308)|Duration|Duration of the event, alternative to dtend
[class](Communication.xml#L311)|String|Access classification, e.g. PUBLIC, PRIVATE, CONFIDENTIAL
[status](Communication.xml#L314)|String|Confirmation status, e.g. CONFIRMED, TENTATIVE, CANCELLED
[location](Communication.xml#L317)|String|Intended venue of the event
[transp](Communication.xml#L320)|Boolean|Time transparency for busy time searches, true = free, false = blocked
[wholeday](Communication.xml#L323)|Boolean|Wholeday event
[fbtype](Communication.xml#L326)|String|Free or busy time type, e.g. FREE, BUSY, BUSY-TENTATIVE

## <a name="TaskData"></a>[TaskData](Communication.xml#L335)


Property|Type|Description
:-------|:---|:----------
[summary](Communication.xml#L336)|String|Short description of the task
[description](Communication.xml#L339)|String|More complete description of the task
[due](Communication.xml#L342)|DateTimeOffset|Date and time that a to-do is expected to be completed
[completed](Communication.xml#L345)|DateTimeOffset|Date and time that a to-do was actually completed
[percentcomplete](Communication.xml#L348)|Byte|Percent completion of a to-do, e.g. 50 for half done
[priority](Communication.xml#L351)|Byte|Relative priority, 0 = undefined, 1 = highest, 9 = lowest

## <a name="MessageData"></a>[MessageData](Communication.xml#L360)


Property|Type|Description
:-------|:---|:----------
[from](Communication.xml#L361)|String|Author(s) of the message
[sender](Communication.xml#L364)|String|Agent responsible for the actual transmission of the message, e.g. a secretary
[to](Communication.xml#L368)|\[String\]|List of primary recipients
[cc](Communication.xml#L371)|\[String\]|List of other recipients (carbon copy)
[bcc](Communication.xml#L374)|\[String\]|List of recipients whose addresses are not to be revealed (blind carbon copy)
[subject](Communication.xml#L378)|String|Topic of the message
[body](Communication.xml#L381)|String|Main part of the message
[keywords](Communication.xml#L384)|\[String\]|List of important words and phrases that might be useful for the recipient
[received](Communication.xml#L387)|DateTimeOffset|Date and time the message was received