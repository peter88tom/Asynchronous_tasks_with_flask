# Asynchronous_tasks_with_flask
The goal of this project is to develop a Flask application that works in conjuctions with Celery to handle long-running process outside  the normal request/response cycle.

1. The end user kicks off a new task via POST request to the server-side.
2. Within the router handler, a task is added to the quest and the ID is send back to client-side.
3. Using Ajax, the client continues to poll the server to check the status of the task while the task itself is running on the background.

# Objective
1. Integrate Celery into [Flask](https://flask.palletsprojects.com/en/2.2.x/) App and create tasks.
2. Containerize Flask, [Celery](https://docs.celeryq.dev/en/stable/getting-started/introduction.html) and [Redis](https://redis.io/) with [Docker](https://docs.docker.com/).
3. Run process in the background with different worker process.
4. Save Celery logs to a file
5. Setup [Flower](https://flower.readthedocs.io/en/latest/) to monitor Celery jobs and workers
6. Test Celery with both unit and integration test
