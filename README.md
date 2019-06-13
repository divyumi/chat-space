# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|stirng|null: false |

### Association
- has many : members 
- has many users , throgh : members
- has many messages


##usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|sring|null: false ,unique :true , add_index|
|email|string|null: false, unique: true|

### Association
- has many members 
- has many groups ,throgh:members
- has many messages


## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|string|null :false|
|image|string|null :false|
|user_id|integer|null :false,foreigh_key :true|
|group_id|integer|null :false,foreigh_key :ture|

### Association
- belongs to group
- belongs to user



