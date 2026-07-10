# CheckConstraint

| Sub | Element | Usage | Card | Type | Description | Note |
|-----|---------|-------|------|------|-------------|------|
|  | CheckConstraint | optional | 1..1 | unknown | Characteristics of a SITE COMPONENT representing a process, such as check-in, security
screening, ticket control or immigration, that may potentially incur a time penalty that should be allowed for when journey planning. Used to mark PATH LINKs to determine transit routes through interchanges. | CheckConstraints are used for different use cases |
| + | CheckDirection | optional | 0..1 | CheckDirectionEnumeration | For CHECK CONSTRAINTs associated with PATH LINKs, the direction in which the check applies. Forwards = from/to, backwards = to/from. For Check constraints associated with an external ENTRANCE, forwards is into the SITE, backwards is out of the SITE. | We usually only use one direction. |
| + | CheckProcess | optional | 0..1 | CheckProcessTypeEnumeration | Type of process that may occur at CHECK CONSTRAINT. | Only a given subset is allowed |
| + | delays | expected | 0..1 | unknown | Delays for CHECK CONSTRAINT .process. |  |
| ++ | CheckConstraintDelay | expected | 1..1 | unknown | Time penalty associated with a CHECK CONSTRAINT. |  |
| +++ | AverageDelay | expected | 0..1 | xsd:duration | Average duration expected to pass through Check. |  |
| +++ | MaximumLikelyDelay | optional | 0..1 | xsd:duration | Maximum duration expected to pass through CHECK CONSTRAINT. |  |
