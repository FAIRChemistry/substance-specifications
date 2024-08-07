# Substance research data model

Python object model specifications based on the [software-driven-rdm](https://github.com/JR-1991/software-driven-rdm) Python library.

## Core objects

### Substance

Specification of a chemical substance.

- label
  - Type: string
  - Description: Any name or identifier of the substance.
- properties
  - Type: [Property](#property)
  - Description: Properties of the substance.
  - Multiple: True
- preparation_procedure
  - Type: [PreparationProcedure](#preparationprocedure)
  - Description: Procedure used to prepare the substance.
- analytical_data
  - Type: [AnalyticalData](#analyticaldata)
  - Description: Analytical data of the substance.
  - Multiple: True
- applications
  - Type: [Application](#application)
  - Description: Applications the substance was usd in
  - Multiple: True

### PreparationProcedure

Specification of a preparation procedure.

- preparation_description
  - Type: string
  - Description: Description of the preparation procedure.
- preparation_steps
  - Type: [PreparationStep](#preparationstep)
  - Description: Steps of the preparation procedure.

### PreparationStep

Specification of a preparation step.

- label
  - Type: string
  - Description: Label of the step.
- preparation_id
  - Type: Identifier
  - Description: Identifier of the preparation step.

### AnalyticalData

Specification of analytical data.

- label
  - Type: string
  - Description: Label of the analytical data.
- analytical_method
  - Type: string
  - Description: Method used to obtain the analytical data.
- analytics_id
  - Type: Identifier
  - Description: Identifier of the analytical data.

### Application

Specification of an application.

- label
  - Type: string
  - Description: Label of the application.
- application_description
  - Type: string
  - Description: Description of the application.
- application_id
  - Type: Identifier
  - Description: Identifier of the application.
