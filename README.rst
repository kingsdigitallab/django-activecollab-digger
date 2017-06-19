# ActiveCollab Digger
A Django application for ActiveCollab tasks overview and creation.

To use: 
1. install the requirements in `requirements.txt`
1. add `activecollab_digger` to `INSTALLED_APPS`
1. add url to `urls.py`:
    `url(r'^digger/', include('activecollab_digger.urls'))`
1. add the settings:
    ```
    AC_BASE_URL = 'https://app.activecollab.com/COMPANY_ID/api/v1/'
    AC_TOKEN = ''
    AC_PROJECT_ID = 1
    AC_USER = 1
    ```
