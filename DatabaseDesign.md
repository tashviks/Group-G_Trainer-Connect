### Tables:

PK - Primary Key
FK - Foreign Key

### 1.Users

| field        | type                           |
| ------------ | ------------------------------ |
| id           | UUID (PK)                      |
| display name | String                         |
| email        | String                         |
| password     | String                         |
| phone        | Number                         |
| userType     | String(Customer/Trainer/Admin) |
| isActive     | Boolean                        |

### 2. Services:

| field           | type                          |
| --------------- | ----------------------------- |
| id              | UUID (PK)                     |
| title           | String                        |
| description     | String                        |
| category/labels | String                        |
| price           | Number                        |
| trainerName     | String                        |
| slotsAvailable  | Number                        |
| slotsFilled     | Number                        |
| status          | String(Open/Closed/Cancelled) |
| createdAt       | DateTime                      |
| createdBy       | UserID (FK)                   |
| updatedAt       | DateTime                      |
| updatedBy       | UserID (FK)                   |

### 3. ServiceBookings:

| field     | type                                 |
| --------- | ------------------------------------ |
| id        | UUID (PK)                            |
| serviceID | UUID (FK)                            |
| userID    | UUID (FK)                            |
| zoomLink  | String                               |
| startTime | DateTimeTime                         |
| endTime   | DateTimeTime                         |
| status    | String(Booked/Rescheduled/Cancelled) |
| createdAt | DateTime                             |
| createdBy | UserID (FK)                          |
| updatedAt | DateTime                             |
| updatedBy | UserID (FK)                          |

### 4. Ratings:

| field     | type        |
| --------- | ----------- |
| id        | UUID (PK)   |
| serviceID | UUID (FK)   |
| userID    | UUID (FK)   |
| rating    | Number      |
| comment   | String      |
| createdAt | DateTime    |
| createdBy | UserID (FK) |
| updatedAt | DateTime    |
| updatedBy | UserID (FK) |

### 5. Complaints:

| field        | type                      |
| ------------ | ------------------------- |
| id           | UUID (PK)                 |
| userID       | UUID (FK)                 |
| serviceID    | UUID (FK)                 |
| complaint    | String                    |
| status       | Boolean(Pending/Resolved) |
| adminComment | String(if Resolved)       |
| createdAt    | DateTime                  |
| createdBy    | UserID (FK)               |
| updatedAt    | DateTime                  |
| updatedBy    | UserID (FK)               |
