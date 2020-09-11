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

### Association

##  messages
|Column|Type|Options|
|------|----|-------|

### Association

##  users_groups
|Column|Type|Options|
|------|----|-------|

### Association