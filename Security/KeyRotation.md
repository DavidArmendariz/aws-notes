# Key Rotation

* For customer managed CMK (not AWS managed CMK)
* If enabled: automatic key rotation happens every 1 year
* Previous key is kept active so you can decrypt old data
* New key has the same CMK ID (only the backing key is changed)

## Manual Key Rotation

* When you want to rotate key every 90 days, 180 days, etc...
* New key has a different CMK ID
* Keep the previous key active so you can decrypt old data
* Better to use aliases in this case (to hide the change of key for the application)
* Good solution to rotate CMK that are not eligible for automatic rotation (like asymmetric CMK)

## KMS Alias Updating

* Better to use aliases in this case (to hide the change of key for the application)
