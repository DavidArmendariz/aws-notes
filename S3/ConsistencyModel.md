# Consistency Model

* Strong consistency as of December 2020
* After a:
  * successful write of a new object (new PUT)
  * or an overwrite or delete of an existing object (overwrite PUT or DELETE)
* ...any:
  * subsequent read request immediately receives the latest version of the object (read after write consistency)
  * subsequent list request immediately reflects changes
  