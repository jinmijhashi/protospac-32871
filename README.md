
## usersテーブル

| Column     | Type   | Options     |
| --------   | ------ | ----------- |
| name       | string | NOT NULL    |
| email      | string | NOT NULL    |    
| password   | string | NOT NULL    |
| profile    | text   | NOT NULL    |
| occupation | text   | NOT NULL    |
| position   | text   | NOT NULL    |
### Association

- has_many :prototype
- has_many :comments

## comments テーブル

| Column    | Type   | Options     |
| ------    | ------ | ----------- |
| text      | text       | NOT NULL    
| user      | references | 
| prototype | reference  |
### Association

- has_many :user
- has_many :prototype
- 

## prototype テーブル

| Column     | Type       | Options  |
| ------     | ---------- | ---------|
| title      | string     | NOT NULL |
| catch_copy | text       | NOT NULL |
| concept    | text       | NOT NULL |
| user       | reference  |
### Association

- belongs_to :user
- belongs_to :comments

