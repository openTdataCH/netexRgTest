# ServiceJourneyInterchange_UMSTEIGZ

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | ServiceJourneyInterchange | mandatory | 1..1 | unknown | The scheduled possibility for transfer of passengers between two SERVICE JOURNEYs at the same or different STOP POINTs. | Transfer time between two specific ServiceJourneys at a given stop (UMSTEIGZ). StaySeated=false: passenger must change vehicles. Replaces InterchangeRule in RG 2.0. One element per journey pair required. |
| + | validityConditions | expected | 1..1 | validityConditions_RelStructure | VALIDITY CONDITIONs conditioning entity. |  |
| ++ | AvailabilityConditionRef | expected | 1..1 | AvailabilityConditionRefStructure | Reference to an AVAILABILITY CONDITION. A VALIDITY CONDITION defined in terms of temporal attributes. |  |
| + | Description | optional | 0..1 | MultilingualString | Description of contents. |  |
| + | StaySeated | mandatory | 0..1 | xsd:boolean | Whether the passenger can remain in vehicle (i.e. block linking). Default is false: the passenger must change vehicles for this INTERCHANGE.
Default is false. |  |
| + | CrossBorder | optional | 0..1 | xsd:boolean | Whether interchanging crosses a border. |  |
| + | Planned | mandatory | 0..1 | xsd:boolean | Whether INTERCHANGE is planned in a timetable. Default is true. |  |
| + | Guaranteed | optional | 0..1 | xsd:boolean | Whether INTERCHANGE is guaranteed. Default is false. |  |
| + | MaximumWaitTime | optional | 0..1 | xsd:duration | Maximum wait time for JOURNEY MEETING. | If not set or PT0M, connection is considered guaranteed. |
| + | MinimumTransferTime | expected | 0..1 | xsd:duration | Maximum transfer duration for INTERCHANGE. |  |
| + | MaximumTransferTime | expected | 0..1 | xsd:duration | Maximum transfer duration for INTERCHANGE. |  |
| + | FromPointRef | mandatory | 1..1 | VehicleMeetingPointRefStructure | Identifier of VEHICLE MEETING POINT from which Link starts. | ScheduledStopPoint at which the feeder journey arrives. Replaces StopPlaceRef+FeederFilter from InterchangeRule. |
| + | ToPointRef | mandatory | 1..1 | VehicleMeetingPointRefStructure | Identifier of VEHICLE MEETING POINT at which Link ends. | ScheduledStopPoint at which the distributor journey departs. Same stop as FromPointRef for same-stop transfers. |
| + | FromServiceJourneyRef | mandatory | 1..1 | ServiceJourneyRefStructure | SERVICE JOURNEY that feeds the INTERCHANGE. +v2.0 | Reference to the specific feeder ServiceJourney. Replaces FeederFilter/ServiceJourneyRef from InterchangeRule. |
| + | ToServiceJourneyRef | mandatory | 1..1 | ServiceJourneyRefStructure | SERVICE JOURNEY that distributes from the INTERCHANGE. +v2.0 | Reference to the specific distributor ServiceJourney. Replaces DistributorFilter/ServiceJourneyRef from InterchangeRule. |
