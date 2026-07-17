# ch-profile_export_psa_file_deprecated

*Table: PublicationDelivery*

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | PublicationTimestamp | mandatory | 1..1 | xsd:dateTime | Time of output of data. |  |
|  | ParticipantRef | mandatory | 1..1 | siri:ParticipantCodeType | Identifier of system requesting Data. |  |
|  | dataObjects | mandatory | 0..1 | dataObjects | NeTEx Entities of any type. |  |
| + | CompositeFrame | mandatory | 1..1 | CompositeFrame | A container VERSION FRAME that groups a set of content VERSION FRAMsE to which the same VALIDITY CONDITIONs have been assigned. |  |
| ++ | frames | mandatory | 0..1 | frames_RelStructure | Content frames in COMPOSITE FRAME. |  |
| +++ | ServiceFrame | mandatory | 1..* | ServiceFrame | A coherent set of Service data to which the same frame VALIDITY CONDITIONs have been assigned. |  |
| ++++ | stopAssignments | mandatory | 0..1 | stopAssignmentsInFrame_RelStructure | STOP ASSIGNMENTs in frame. | currently only PassengerStopAssigments allowed |
