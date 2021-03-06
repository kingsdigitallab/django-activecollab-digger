ActiveCollab Digger
===================

Django application to integrate ActiveCollab issue reporting into Django based projects.

To use:

#. ``pip install django-activecollab-digger``
#. add ``activecollab_digger`` to ``INSTALLED_APPS``
#. add ``url(r'^digger/', include('activecollab_digger.urls'))`` to ``urls.py``
#. add the settings::

    # ActiveCollab API URL
    AC_BASE_URL = 'https://app.activecollab.com/COMPANY_ID'
    AC_API_URL = AC_BASE_URL + '/api/v1/'
    # ActiveCollab API token
    AC_TOKEN = ''
    # ActiveCollab project ID
    AC_PROJECT_ID = 1
    # ActiveCollab user ID to create the issues
    AC_USER = 1
#. in settings add the context processor ``activecollab_digger.context_processors.activecollab_digger`` to ``TEMPLATES['OPTIONS']['context_processors']``
   

Notes
-----

* The application needs to be behind authentication, having a ``LOGIN_URL`` setting should be enough in cases where the django admin is enabled
* In Python version lower than 2.7.9 ``pip install`` may not install all the dependencies, this is due to an issue with ``setuptools``. To work around it install/update the packages ``appdirs packaging setuptools six``.
