[<<Back](../README.md)

| #                          | case                            | example                                |
|----------------------------|---------------------------------|----------------------------------------|
| Controller                 | Singular                        | ArticleController                      |
| Route                      | Plural                          | articles/1                             |
| Named route                | Snake_case                      | users.show_active                      |
| Model                      | Singular                        | User                                   |
| hasOne or belongsTo rel.   | Singular                        | articleComment                         |
| All other relationships    | Plural                          | articleComments                        |
| Table                      | Plural                          | article_comments                       |
| Pivot table                | Singular                        | article_user                           |
| Table column               | Snake_case                      | meta_title                             |
| Foreign key                | Singular w/ _id                 | article_id                             |
| Primary key                | -                               | id                                     |
| Migration                  | -                               | 2017_01_01_000000_create_articles_table|
| Method                     | CamelCase                       | getAll                                 |
| Function                   | CamelCase                       | getUsersList                               |
| Method in resource ctrl    | More infos: table               | store                                  |
| Method in test class       | CamelCase                       | testGuestCannotSeeArticle              |
| Model property             | Snake_case                      | $model->model_property                 |
| Variable                   | CamelCase                       | $anyOtherVariable                      |
| Collection                 | Descriptive, Plural             | $activeUsers = User::active()->get()   |
| Object                     | Descriptive, Singular           | $activeUser = User::active()->first()  |
| Config and language files index | Snake_case                 | articles_enabled                       |
| View                       | snake_case                      | show_filtered.blade.php                |
| Config                     | snake_case                      | google_calendar.php                    |
| Contract (interface)       | Adjective or noun               | Authenticatable                        |
| Trait                      | Adjective                       | Notifiable                             |
