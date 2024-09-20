To use an `ImageField` in Django with SQLite3 and manage images using the Pillow library, follow this guide:

### Prerequisites:
- Django installed (`pip install django`)
- Pillow installed (`pip install pillow`)

### Steps:

#### 1. **Set Up Your Django Project:**
If you haven’t set up a Django project yet, you can do so by running:

```bash
django-admin startproject myproject
cd myproject
python manage.py startapp myapp
```

Add your app to `INSTALLED_APPS` in `settings.py`:

```python
INSTALLED_APPS = [
    # other apps
    'myapp',
]
```

#### 2. **Configure Media Settings:**
In your `settings.py`, add configurations for media files (where uploaded images will be saved).

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

#### 3. **Create a Model with an ImageField:**
In your `myapp/models.py`, define a model that includes an `ImageField`:

```python
from django.db import models

class Profile(models.Model):
    name = models.CharField(max_length=100)
    avatar = models.ImageField(upload_to='avatars/')  # ImageField with Pillow support

    def __str__(self):
        return self.name
```

- `upload_to='avatars/'` specifies the directory where uploaded images will be stored.

#### 4. **Apply Migrations:**
Run the following commands to create and apply migrations for your new model:

```bash
python manage.py makemigrations
python manage.py migrate
```

#### 5. **Install Pillow Library:**
Ensure Pillow (Python Imaging Library) is installed. It’s needed to handle image uploads.

```bash
pip install pillow
```

#### 6. **Set Up File Upload Handling in Views:**
Create a form to upload images. In `myapp/forms.py`, define the form using Django’s `ModelForm`:

```python
from django import forms
from .models import Profile

class ProfileForm(forms.ModelForm):
    class Meta:
        model = Profile
        fields = ['name', 'avatar']
```

In `myapp/views.py`, write the view to handle the image upload:

```python
from django.shortcuts import render, redirect
from .forms import ProfileForm

def profile_upload(request):
    if request.method == 'POST':
        form = ProfileForm(request.POST, request.FILES)
        if form.is_valid():
            form.save()
            return redirect('profile_list')  # Redirect to another page after success
    else:
        form = ProfileForm()
    
    return render(request, 'profile_upload.html', {'form': form})
```

#### 7. **Create Templates:**
In your templates folder, create `profile_upload.html`:

```html
<form method="POST" enctype="multipart/form-data">
    {% csrf_token %}
    {{ form.as_p }}
    <button type="submit">Upload</button>
</form>
```

#### 8. **Serve Media Files During Development:**
Add the following in your `urls.py` to serve media files during development:

```python
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    # your URL patterns
] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

#### 9. **Display Uploaded Images:**
In your `views.py`, you can display uploaded images. Add this in `profile_list.html`:

```html
{% for profile in profiles %}
    <p>{{ profile.name }}</p>
    <img src="{{ profile.avatar.url }}" alt="Avatar for {{ profile.name }}">
{% endfor %}
```

Make sure your view returns the profiles:

 ```python
def profile_list(request):
    profiles = Profile.objects.all()
    return render(request, 'profile_list.html', {'profiles': profiles})
```

#### 10. **Run Your Project:**
Run the development server to test the setup:

```bash
python manage.py runserver
```

### Summary:
- **`ImageField`** stores images in Django.
- **Pillow** handles image files and is required for Django's `ImageField`.
- Configure media settings to store and serve uploaded files.
