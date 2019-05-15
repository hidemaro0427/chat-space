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


comments テーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign,key true|
|image|text|
|text|text|
Association
belongs_to :user
belongs_to :group

usersテーブル
|Column|Type|Options|
|------|----|-----|
|id|integer|null: fales, unique: true|
|E-maill|string|null: fales, unique: true|
|name|string|null: fales|
Association
has_many :comments
has_many :groups

groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|comment_id|integer|null: false, foreign_key: true|
Association
has_many :users
has_many :comments