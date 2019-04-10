Things and Relationships Mapping
================================

# Things
- Theatres
- Festivals
- Projects
- Productions
- Company
- Co-Productions
- Performances
- Sponsors / Funders / Organisations
- Relationship Managers (us and them)

## Company
- has_many :productions
- has_many :theatres, through: productions
- has_many :festivals, through: productions
- has_many :sponsors, through: productions

- has_many :projects
- has_many :theatres, through: projects
- has_many :festivals, through: projects
- has_many :sponsors, through: projects

## Productions
- belongs_to :company

- has_many :coproductions
- has_many :theatres, through: coproductions
- has_many :festivals, through: coproductions

- has_many :performances
- has_many :theatres, through: performances
- has_many :festivals, through: performances

- ? Can we have more than one type of relationships to join table?

## Projects
- belongs_to :company
- belongs_to :theatres
- belongs_to :festivals

- ? Can it belong to more than one class, every time is different ?

## Sponsors
- has_many :productions
- has_many :projects

- belongs_to :production (A sponsor belongs to a production??!)
- belongs_to :project
- ? clarify relationship

#Relationship Managers
- belongs_to :company
- belongs_to :festival
- belongs_to :theatre

- ? Do we write belongs to the company ?
