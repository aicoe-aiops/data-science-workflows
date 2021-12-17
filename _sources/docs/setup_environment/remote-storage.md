# Remote Data Storage

One of the key elements for any successful data science project is the DATA! But how can we manage our data in a way that makes it easy to share, track and support reproducibility among teams and between experiments? Also, how can we do all this while avoiding using git as our data store?

We use the S3 compatible remote storage provided by the Operate First cluster. Its easy to request a bucket for your own or your team, just fill out and submit this [issue](https://github.com/operate-first/support/issues/new?assignees=first-operator&labels=kind%2Fonboarding%2Carea%2Fbucket&template=ceph_bucket_request.yaml&title=BUCKET%3A+%3Cname%3E) on the operate-first/support repo.

Once the issue is closed, the bucket is created and you have your bucket credentials, review [this notebook](/notebooks/EDA/interacting_with_ceph.ipynb) for an example of how to interact with your data stored in a remote storage bucket from a Jupyter Notebook.
