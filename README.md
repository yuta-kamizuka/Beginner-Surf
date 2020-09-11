# README

# Beginner-Surf DB設計

##  usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|emil|string|null: false|
|password|string|null: false|
### Association
- has_many :messages
- has_many :groups_users
- has_many :groups,  through:  :groups_users

##  groups
|Column|Type|Options|
|------|----|-------|
|name|string|null :false|
### Association
has_many :groups_users
has_many  :users,  :through:  :groups_users
has_many :messages

##  messages
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|user_id|integer|null :false|
|group_id|integer|null :false|
### Association
belongs_to :user
belongs_to :group

##  users_groups
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null :false, foreign_kye: true|
|group_id|integer|null: false, foreign_kye: true|
### Association
belongs_to :user
belongs_to :group