---
config:
  layout: dagre
---
classDiagram
direction TB
    class Person {
	    - int id
	    - String firstName
	    - String lastName
	    - Date dateOfBirth
	    - String phone
	    - String mail
    }

    class PersonRole {
	    - int id
	    - Date startDate
	    - Date endDate
    }

    class Role {
	    - int id
	    - String nameRole
    }

    class Player {
    }

    class Coach {
    }

    class Guardianship {
	    - int id
	    - String relationType
	    - int contactPriority
	    - String contactNotes
    }

    Person "1" --> "0..*" PersonRole
    PersonRole "0..*" --> "1" Role
    PersonRole <|-- Player
    PersonRole <|-- Coach
    Person "1" --> "0..*" Guardianship : child
    Person "1" --> "0..*" Guardianship : guardian