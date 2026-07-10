# ServiceFacilitySet

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | ServiceFacilitySet | expected | 1..1 | unknown | Service FACILITY. Set of enumerated FACILITY values (Where available names are based on TPEG classifications, augmented with UIC etc.). | List of ServiceFacility. Be careful: not all are supported. Consult profile. Make sure to not generate identical ServiceFacilitySets. Reuse them. |
| + | Extensions | expected | 1..1 | ExtensionsStructure | User defined Extensions to ENTITY in schema. (Wrapper tag used to avoid problems with handling of optional 'any' by some validators). | Two elements used in HRDF for ordering facilities |
| ++ | Priority | expected | 0..1 | InterchangePriorityType | Priority to assign to this INTERCHANGE. |  |
| + | Description | expected | 0..1 | MultilingualString | Description of contents. |  |
| ++ | Text | optional | 0..1 | MultilingualString | Text content of NOTICe. |  |
| + | FareClasses | optional | 1..1 | FareClassListOfEnumerations | List of FARE CLASSes. |  |
| + | NuisanceFacilityList | optional | 1..1 | NuisanceFacilityListOfEnumerations | List of NUISANCE FACILITies. |  |
| + | SanitaryFacilityList | optional | 1..1 | SanitaryFacilityListOfEnumerations | List of SANITARY FACILITies. |  |
| + | CouchetteFacilityList | optional | 1..1 | CouchetteFacilityListOfEnumerations | List of COUCHETTE FACILITies. |  |
| + | GroupBookingFacility | optional | 1..1 | GroupBookingEnumeration | Classification of GROUP FACILITY type - TPEG pti23. |  |
