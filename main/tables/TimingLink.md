# TimingLink

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | TimingLink | expected | 1..1 | unknown | An ordered pair of TIMING POINTs for which run times may be recorded. Timing links are directional - there will be separate links for each direction of a route. | A timing link is basically defined between two ScheduledStopPoints. However, there may be different timing behaviours and then multiple TimingLinks between the same ScheduledStopPoint might be necessary |
| + | FromPointRef | mandatory | 1..1 | VehicleMeetingPointRefStructure | Identifier of VEHICLE MEETING POINT from which Link starts. |  |
| + | ToPointRef | mandatory | 1..1 | VehicleMeetingPointRefStructure | Identifier of VEHICLE MEETING POINT at which Link ends. |  |
| + | OperationalContextRef | optional | 1..1 | OperationalContextRefStructure | Reference to an OPERATIONAL CONTEXT. | This is "Betriebszweig". Switzerland does not use it currently, but it might become interesting at some point |
