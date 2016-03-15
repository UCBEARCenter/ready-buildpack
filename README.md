
This 'ready-buildpack' downloads a tar.bz2 file from an S3 URL and
unpacks it on top of /app.  That is all.

It is called 'ready-buildpack' because it is already ready -- no compilation
or other processing is needed -- all preparation should go into to the
tarball that is downloaded from S3.

Set variables:
    READY_BIN = s3://path/to/thing.tar.bz2

To download from S3 use S3_KEY and S3_SECRET variables.
Also, set READY_MD5 so that builder can verify if ball is in the cache.

Possible future extensions:
- Archives other than tar.gz.
- Resource locations other than s3.
