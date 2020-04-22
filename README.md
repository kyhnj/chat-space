<<<<<<< Updated upstream
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Assciation
- has_many :massage

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, forngin_key: true|
### Assciation
- has_many :user_id

=======
>>>>>>> Stashed changes
## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user

## massageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foregin_key: ture|
### Assciation
- belong_to :user
- belong_to :group
