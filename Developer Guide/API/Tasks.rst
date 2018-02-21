Tasks
=====

The API supports tasks execution via the HTTP API. Cron is the only supported task as the moment.

Execute Cron Job
----------------

Cron job can be executed, remotely, by making a post to :code:`POST /api/tasks/cron`. See :code:`scripts/rcron.php`
