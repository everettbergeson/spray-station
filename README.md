# spray-station
Home Spray Wall Climbing App

Initial thoughts on database structure: 
Wall
- Id (int)
- Name (varchar)
Climb
- Id (int)
- WallId (int)
- PictureId (int)
- ClimberId (int)
- Description (varchar)
- SetDate (datetime)
- LastEditedDate (datetime)
Tag
- Id (int)
- Name (varchar)
ClimbTag
- ClimbId (int)
- TagId (int)
Climber
- Id (int)
- Name (varchar)
- PictureId (int)
Tick
- Id (int)
- ClimbId (int)
- ClimberId (int)
- Date (datetime)
- Note (varchar)
- Repeat (bool)
Grade (only allowed to vote once ticked)
- ClimbId (int)
- ClimberId (int)
- ProposedGrade (int)
Picture
- Id
- Url
Hold
- ClimbId (varchar)
- Coordinates (or something like that)
- Radius?

One to one:
- Climber to Picture
- Climber to Grade to Climb
One to many: 
- Wall to Climb
- Climb to Hold
- Climb to Grade
- Climb to Tick
- Climber to Tick
- Picture to Climb
Many to many: 
- Tag to Climb
