# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| email              | string | null: false |
| encrypted_password | string | null: false |

### Association

- has_many :memos

## memos テーブル

| Column       | Type       | Options                        |
| ------------ | ---------- | ------------------------------ |
| title        | string     | null: false                    |
| content      | text       |                                |
| studied      | integer    | null: false                    |
| user         | references | null: false, foreign_key: true |

### Association

- belongs_to :user

