## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|string|null: false|
|password confirmation|string|null: false|
### Association
- has_many :messages
- has_many :groups, through: :groups_users
- has_many :groups_users

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_name|integer|null: false, unique: true|
### Association
- has_many :users_id
- has_many :groups, through: :groups_users
- has_many :groups_users
- has_many :massages

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|
|image|string|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foregin_key: ture|
### Association
- belongs_to :user
- belongs_to :group
