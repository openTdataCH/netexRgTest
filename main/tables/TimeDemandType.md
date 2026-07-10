# TimeDemandType

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | TimeDemandType | expected | 1..1 | unknown | An indicator of traffic conditions or other factors which may affect vehicle run or wait times. It may be entered directly by the scheduler or defined by the use of TIME BANDs. | TimeDemandType assigns a timing behaviour to a ServiceJourney |
| + | Description | optional | 0..1 | MultilingualString | Description of contents. | Can be used, if a decription exists what this pattern doe |
| + | runTimes | expected | 0..1 | vehicleJourneyRunTimes_RelStructure | Run times for VEHICLE JOURNEY over different TIMING LINKs. | The run time on the TimingLinks |
| ++ | JourneyRunTime | expected | 1..1 | unknown | The time taken to traverse a TIMING LINK in a particular JOURNEY PATTERN, for a specified TIME DEMAND TYPE. If it exists, it will override the DEFAULT SERVICE JOURNEY RUN TIME and DEFAULT DEAD RUN RUN TIME. |  |
| +++ | TimingLinkRef | mandatory | 1..1 | TimingLinkRefStructure | Reference to a TIMING LINK. | The timing link that is ued here and that that does have a given run time |
| +++ | RunTime | the run time | 1..1 | xsd:duration | Run time as interval. |  |
| + | waitTimes | expected | 0..1 | vehicleJourneyWaitTimes_RelStructure | WAIT TIMEs for VEHICLE JOURNEY at different TIMING POINTs. | we only need the wait times, when they are >0 |
| ++ | JourneyWaitTime | expected | 1..1 | unknown | The time a vehicle has to wait at a specific TIMING POINT IN JOURNEY PATTERN, for a specified TIME DEMAND TYPE. This wait time can be superseded by a VEHICLE JOURNEY WAIT TIME. | Relevant waiting times at the stop |
| +++ | ScheduledStopPointRef | mandatory | 0..1 | ScheduledStopPointRefStructure | Specific SCHEDULED STOP POINT at end of CONNECTION. | Which Quay is referenced |
| +++ | WaitTime | mandatory | 0..1 | xsd:duration | Timetabled waiting interval. |  |
