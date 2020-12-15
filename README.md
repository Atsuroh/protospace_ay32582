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

# テーブル設計

## users テーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | NOT NULL    |
| password   | string | NOT NULL    |
| name       | string | NOT NULL    |
| profile    | text   | NOT NULL    |
| occupation | text   | NOT NULL    |
| position   | text   | NOT NULL    |

## comments テーブル

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       |  NOT NULL   |
| user      | references |             |
| prototype | references |             |

## prototypes テーブル

| Column     | Type               | Options |
| ---------- | ------------------ | ------- |
| title      | string             | NOT NUL |
| catch_copy | text               | NOT NUL |
| concept    | text               | NOT NUL |
| image      | ActiveStorageで実装 |         |
| user       | references         |         |
