# テーブル設計

## usersテーブル

|    Column    |  Type   |     Option     |
|--------------|---------|----------------|
| nickname     | string  | null: false    |
| email        | string  | null: false    |
| password     | string  | null: false    |
| first_name   | string  | null: false    |
| last_name    | string  | null: false    |
| Day          | date    | null: false    |

### Association

- has_many :events
- has_many :comments

## eventsテーブル

|    Column      | Type   |   Option      |
|----------------|--------|---------------|
| name           | string | null: false   |
| info           | text   | null: false   |
| date-day       | date   | null: false   |


### Association

- has_many :comments
- belongs_to :user

## Commentsテーブル

|    Column     |  Type     |    Option    |
|---------------|-----------|--------------|
| text          | text      | null: false  |
| date-day      | date      | null: false  |

### Association

- belongs_to :user
- belongs_to :events