## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false|
### Association
- has_many :messages
- has_many :groups, through: :groups_users
- has_many :groups_users

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, forngin_key: true|
### Association
- has_many :users_id
- has_many :group, through: :groups_users
- has_many :groups_users

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :group
- belongs_to :user

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|text|
|image|string|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foregin_key: ture|
### Association
- belong_to :user
- belong_to :group
