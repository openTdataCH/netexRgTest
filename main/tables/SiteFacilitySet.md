# SiteFacilitySet

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | SiteFacilitySet | mandatory | 1..1 | unknown | Set of enumerated FACILITY values that are relevant to a SITE (names based on TPEG classifications, augmented with UIC etc.). | List of SiteFacility. Be careful: not all are supported. Consult profile. Make sure to not generate identical SiteFacilitySets. Reuse them. There might be an overlap to ServiceFacilitySet, but they are used for different purposes. |
| + | validityConditions | optional | 1..1 | validityConditions_RelStructure | VALIDITY CONDITIONs conditioning entity. |  |
| ++ | [AvailabilityCondition](AvailabilityCondition.md) | optional | 1..1 | unknown | VALIDITY CONDITION stated in terms of DAY TYPES and PROPERTIES OF DAYs. |  |
| + | Description | optional | 0..1 | MultilingualString | Description of contents. | Description is optional |
| ++ | Text | optional | 0..1 | MultilingualString | Text content of NOTICe. |  |
| + | AssistanceFacilityList | optional | 1..1 | AssistanceFacilityListOfEnumerations | List of ASSISTANCE FACILITies. |  |
| + | AccessibilityToolList | optional | 0..1 | AccessibilityToolListOfEnumerations |  |  |
| + | SanitaryFacilityList | optional | 1..1 | SanitaryFacilityListOfEnumerations | List of SANITARY FACILITies. |  |
| + | TicketingServiceFacilityList | optional | 1..1 | TicketingServiceFacilityListOfEnumerations | List of TICKETING SERVICE FACILITies, e.g. purchase, collection. top up. |  |
| + | EmergencyServiceList | optional | 0..1 | EmergencyServiceListOfEnumerations | Emergency service assistance available. |  |
| + | LuggageLockerFacilityList | optional | 1..1 | LuggageLockerFacilityListOfEnumerations | List of LUGGAGE LOCKER FACILITies. |  |
| + | ParkingFacilityList | optional | 1..1 | ParkingFacilityListOfEnumerations | List of PARKING FACILITies. |  |
