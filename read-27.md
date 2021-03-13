## Using Models

This illustration of the structure of models feels like it's just all objects as shown below.
```
Snack:{ # Instance of Snack class aka a model
    title:Oreo
    manufacturer:Company[1] { # Instance of Company class aka a model
        name:Nibisco
        founder:User[1] { # Instance of User class aka a model
            name:Adolphus W. Green
            b-day:14JAN1844
        }
        head quarters:East Hanover, NJ
    flavor:mint
    store:Company[1] { # Instance of Company class aka a model
        name:HEB
        founder:Flourance Butt
        head quarters:San Antonio, TX
    }
}
```
Common field types:
- CharField - Short-Mid sized string with mandatory max_length.
- TextField - String of unspecified length and an optional max length.
- IntegerField - Whole number value only.
- Date/DateTimeField - Stores dates and datetime.
- EmailField - Validates and stores emails.
- File/ImageField - Uploads files/images respectively.
- AutoField - An incrementing integer field for order identification. One is automatically added if not specified.
- ForeaignKeyField - Store an item that has connections to several other databases. Like a username being stored in different purchaser sections.
- ManyToManyField - Stores an item that has connections to several items all of which have connections to several other items. Like an genre being connected to several books all of which have several genres.

## Admin Site

Admin models are used to change the apperance of models in the admin page of the django website. The following class (or admin model) adds columns of `last_name`, `first_name`, `date_of_birth`, and `date_of_death`.
```
class AuthorAdmin(admin.ModelAdmin):
    list_display = ('last_name', 'first_name', 'date_of_birth', 'date_of_death')
```
These classes are placed in the models.py directory with the rest of the models.
These can be made to alter any models appearance in admin by registering it in admin.py with the model to be altered by it as follows.
```
admin.site.register(Author, AuthorAdmin)
```