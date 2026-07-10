# ch-profile_NETWORK_OFFER

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | PublicationDelivery | mandatory | 1..1 | PublicationDeliveryStructure | A set of NeTEx objects as assembled by a publication request or other service. Provides a general purpose wrapper for NeTEx data content. |  |
| + | PublicationTimestamp | mandatory | 1..1 | xsd:dateTime | Time of output of data. |  |
| + | ParticipantRef | mandatory | 1..1 | siri:ParticipantCodeType | Identifier of system requesting Data. |  |
| + | dataObjects | mandatory | 0..1 | unknown | NeTEx Entities of any type. |  |
| ++ | CompositeFrame | mandatory | 1..1 | unknown | A container VERSION FRAME that groups a set of content VERSION FRAMsE to which the same VALIDITY CONDITIONs have been assigned. |  |
| +++ | frames | mandatory | 0..1 | frames_RelStructure | Content frames in COMPOSITE FRAME. |  |
| ++++ | [ResourceFrame](ResourceFrame.md) | mandatory | 1..1 | unknown | A coherent set of reference values for TYPE OF VALUEs , ORGANISATIONs, VEHICLE TYPEs etc that have a common validity, as specified by a set of frame VALIDITY CONDITIONs. Used to define common resources that will be referenced by other types of FRAME. |  |
| ++++ | [SiteFrame](SiteFrame.md) | optional | 1..1 | unknown | A coherent set of SITE data to which the same frame VALIDITY CONDITIONs have been assigned. | Only for elements that are NOT in the SITE_OFFER and only during importation. |
| ++++ | ServiceFrame | mandatory | 1..1 | unknown | A coherent set of Service data to which the same frame VALIDITY CONDITIONs have been assigned. | Doesn't contain DefaultConnection and SiteConnection |
| ++++ | [ServiceCalendarFrame](ServiceCalendarFrame.md) | mandatory | 1..1 | unknown | A SERVICE CALENDAR. A coherent set of OPERATING DAYS and DAY TYPES comprising a Calendar. That may be used to state the temporal VALIDITY of other NeTEx entities such as Timetables, STOP PLACEs, etc. Covers a PERIOD with a collection of assignments of OPERATING DAYS to DAY TYPES. |  |
| ++++ | [TimetableFrame](TimetableFrame.md) | mandatory | 1..1 | unknown | A coherent set of timetable data (VEHICLE JOURNEYs and BLOCKs) to which the same VALIDITY CONDITIONs have been assigned. |  |
