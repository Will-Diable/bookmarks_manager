### To set up the database

 Connect to `psql` and create a `bookmark_manager` and a `bookmark_manager_test` database:

 ```
 CREATE DATABASE bookmark_manager;
  CREATE DATABASE bookmark_manager_test;
 ```

 To set up the appropriate tables, connect to both databases respectively in `psql` and run the SQL scripts in the `db/migrations` folder in the given order.


### planning

User Stories:

1. 
```
As a user,
So that I can see which bookmarks I've saved,
I would like to show a list of bookmarks
```

| Verb | Method | Object |
| :--: | :----: | :----: |
| show | list | bookmarks |
 
2. 
```
As a user,
So that I can save links,
I would like to add new bookmarks
```

| Verb | Method | Object |
| :--: | :----: | :----: |
| add | add | bookmark |

3. 
```
As a user,
So that I can remove links no longer needed,
I would like to delete bookmarks
```

| Verb | Method | Object |
| :--: | :----: | :----: |
| delete | delete | bookmark |

4. 
```
As a user,
So that I can amend my links,
I would like to update bookmarks
```

 Verb | Method | Object |
| :--: | :----: | :----: |
| update | update | bookmark |

5. 
```
As a user,
So that I can annotate,
I would like to comment on bookmarks
```

 Verb | Method | Object |
| :--: | :----: | :----: |
| comment | comment | bookmark |

6. 

```
As a user,
So that I can organise my links,
I would like to tag bookmarks into categories
```

 Verb | Method | Object |
| :--: | :----: | :----: |
| tag | tag | bookmark |

7. 
```
As a user,
To make searching easier,
I would like to filter bookmarks by tag
```

 Verb | Method | Object |
| :--: | :----: | :----: |
| filter | search_by_tag | bookmark |

8. 
```
As an administrator, 
To preserve client data,
Users are restricted to manage only their own bookmarks
```

 Verb | Method | Object |
| :--: | :----: | :----: |
| restricted | lock | bookmark |

### BELOW IMAGE FROM MAKERS

![dm_image](https://github.com/makersacademy/course/raw/main/apprenticeships_bookmark_manager/images/bookmark_manager_1.png)


| Component   | Responsibility                                | Refactor                                |
| :-----------: | :--------------------------------------------:  | :----------------------------------------: |
| Model       | Encapsulate logic with relevant data          | Encapsulate bookmark data in a class    |
| View        | Display the result to a user                  | Show the bookmark data in a list        |
| Controller  | Get data from the model and put in the view   | Render bookmark data into to the view   |