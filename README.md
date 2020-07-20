# UmaFoto_ae
A simple Django app for external image search

## Requirements
- Django Framework(should work with avery version)
- Requests
- API keys for [Pixabay](https://pixabay.com/api/docs/) and [Unsplash](https://unsplash.com/documentation)

## Instalation
1. First clone this repository to your Django project:
   
In the root of your project:

```
git clone https://github.com/joelschutz/umafoto_ae.git
```

2. Add app to your INSTALLED_APPS:

In the settings.py of your Django project, add the new app:

```
INSTALLED_APPS = [
    ...
    'umafoto_ae',
    ...
    ]
```

3. Add path to application:

In the urls.py of your project, add new paths:

```
urlpatterns = [
    ...
    path('umafoto-ae/', umafoto_ae.views.home, name='umafoto-ae'),
    path('umafoto-ae/result/', umafoto_ae.views.result, name='umafoto-ae-result'),
    path('umafoto-ae/info/', umafoto_ae.views.info, name='umafoto-ae-info'),
    ...
    ]
```

4. Define enviromental variables:

Go to your working terminal and define the keys that you acquired:

```
export PIXABAY_KEY="?key=your-Pixabay-API-key"
export UNSPLASH_KEY="?client_id=your-Unsplash-API-key
```

5. Test the server

```
python3 manage.py runserver
```

If everything goes well at this point, the app should be served at:

```
http://your.domain/umafoto-ae/
```

## Built With

* [Django](https://www.djangoproject.com/) - The web framework used
* [Requests](https://requests.readthedocs.io/en/master/) - Library used for interfacing with the APIs
* [Bootstrap](https://getbootstrap.com/) - To make the page prettier

## License

This project is licensed under the GNU General Public License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Much of the code is commented in english, but some prints and Docstrings are still in portuguese. This issue will be tackled in a future revision.
* Some improvement is needed in the managing of jsons. For now there is a cleaner for the JSONS folder, but a more elegant solution should be the objective.
