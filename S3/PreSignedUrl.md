# Pre-signed URL

* Can generate pre-signed URLs using SDK or CLI
* Valid for a default of 3600 seconds, can change timeout with `--expires-in [TIME_BY_SECONDS]` argument
* Users given a pre-signed URL inherit the permissions of the person who generate the URL for GET / PUT
