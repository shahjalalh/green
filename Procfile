web: gunicorn config.wsgi:application
worker: celery worker --app=green.taskapp --loglevel=info
