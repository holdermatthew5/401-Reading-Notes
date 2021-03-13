## Working with forms

Based on the image of the form handeling process it looks like django and node do pretty much the same stuff. The only real difference I see is that node gives me the actual function to do do things with whenever the requests are made while in django the only way i can think to control that is by learning the full django process and modifying that process directly. For this reason, so far, I prefer Node.js. It may require more work from me to get a decent looking website, but it also gives me more control up front.
Types of input values for forms in django:
- BooleanField
- ChoiceField
- TypedChoiceField
- DateField
- DateTimeField
- DecimalField
- DurationField
- EmailField
- FileField
- FilePathField
- FloatField
- ImageField
- IntegerField
- GenericIPAddressField
- MultipleChoiceField
- TypedMultipleChoiceField
- NullBooleanField
- RegexField
- SlugField
- TimeField
- URLField
- UUIDField
- ComboField
- MultiValueField
- SplitDateTimeField
- ModelMultipleChoiceField
- ModelChoiceField.
Supposedly you can create forms as views, but that seems a little weird to me and i'm not sure how to explain why. An example of this use is pasted below.
```
import datetime

from django import forms
from django.core.exceptions import ValidationError
from django.utils.translation import ugettext_lazy as _

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

    def clean_renewal_date(self):
        data = self.cleaned_data['renewal_date']

        # Check if a date is not in the past.
        if data < datetime.date.today():
            raise ValidationError(_('Invalid date - renewal in past'))

        # Check if a date is in the allowed range (+4 weeks from today).
        if data > datetime.date.today() + datetime.timedelta(weeks=4):
            raise ValidationError(_('Invalid date - renewal more than 4 weeks ahead'))

        # Remember to always return the cleaned data.
        return data
```
URL configuration has a += assigning the paths to urlpatterns which confuses me. I definitely thought that was supposed to be an = and i definitely thought

## Creating a home page

Important steps in crating a viewable page are as follows.
- Write view in apps views.py
- Write url in apps urls.py
If a model is necessary for this website the following steps are also important.
- Write model in apps models.py
- Register model in projects admin.py
From here it's only a matter of writing the templating in the html templates to get the objects to show up where they need to be, adding get_absolute_url methods to models as well as fields and success urls to views to redirect to the proper pages and present the necessary input lines when a form is used.