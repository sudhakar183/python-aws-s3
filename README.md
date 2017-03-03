# python-aws-s3

Open [AWS Console](https://aws.amazon.com/console/) and log in.

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/1.png?token=AGNQQB4Q7sizjmFqsAVZq3V_sN8TMRFLks5YwerPwA%3D%3D "Logo Title Text 1")

Click the `Services` dropdown and select the `S3` service.

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/2.png?token=AGNQQNz_t6F17wj-SFdtfMyDoIajZS_0ks5YweyxwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/3.png?token=AGNQQJstPfN74ZaU0DAGs48onSsPTqsjks5YwezAwA%3D%3D "Logo Title Text 1")

Click `Create Bucket`. Give it a name, region then hit next through each step.

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/4.png?token=AGNQQLW_rjSbf4dhVQzVyf9K82ftwDGXks5YwezYwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/5.png?token=AGNQQD4kg2EX_ZXz6jNEQOl03rXmi4g6ks5YwezIwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/6.png?token=AGNQQBiuGeGun0prBmDnWfCGS7txhGqCks5YweztwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/7.png?token=AGNQQKrDpZNUvJ_1BSsAxBTL4z-F-9yzks5Ywez6wA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/8.png?token=AGNQQLY2H-I-DXKgioN3a_sSZa0RvA9vks5Ywe0RwA%3D%3D "Logo Title Text 1")

Now click your new bucket

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/9.png?token=AGNQQIF3ijNHUArFfOIKmDqQLesD-0xDks5Ywe06wA%3D%3D "Logo Title Text 1")

Upload a test image to your bucket

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/10.png?token=AGNQQNvBtD2xdq2lEv-0nPOSd4lr_HcUks5Ywe1IwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/11.png?token=AGNQQJ7uOOASpUpWvH17LFx1hUf2gn-Nks5Ywe1UwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/12.png?token=AGNQQJ5neNpGcIPRJruFgoLHluLHjfzSks5Ywe1pwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/13.png?token=AGNQQPvo-Kz8gzLdfDzuJFTDqHOw7zZ9ks5Ywe12wA%3D%3D "Logo Title Text 1")

You can find your new file. If you click it, you should see a link. Open the link in a new tab.

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/14.png?token=AGNQQPBk3nKWXD5dLMty1mbSz_wq4Towks5Ywe2MwA%3D%3D "Logo Title Text 1")

As you can see, you'll get "Access Denied".

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/15.png?token=AGNQQBPsYqTSH6PhLfvI_JcpDzkuZE3pks5Ywe2bwA%3D%3D "Logo Title Text 1")

Click the file, and under "more" press make public. Refresh the link.

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/16.png?token=AGNQQNKjd5GvP2Wnh8f5JGTYV1AfVIhfks5Ywe2mwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/17.png?token=AGNQQB9N71ROMur-mOpgYYbJnD8_tGiHks5Ywe2zwA%3D%3D "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/keithweaver/python-aws-s3/master/images-for-setup/18.png?token=AGNQQDZfL40P0kDRLMraNNS1gNjT15ARks5Ywe27wA%3D%3D "Logo Title Text 1")

```


arn:aws:iam::281979644754:user/sample-user
```

```
{
    "Version": "2012-10-17",
    "Id": "Policy1488494182833",
    "Statement": [
        {
            "Sid": "Stmt1488493308547",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::281979644754:user/sample-user"
            },
            "Action": [
                "s3:ListBucket",
                "s3:ListBucketVersions",
                "s3:GetBucketLocation",
                "s3:Get*",
                "s3:Put*"
            ],
            "Resource": "arn:aws:s3:::img-bucket-00123"
        }
    ]
}
```

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListAllMyBuckets",
                "s3:PutObject",
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::*"
            ]
        }
    ]
}
```

```
<?xml version="1.0" encoding="UTF-8"?>
<CORSConfiguration xmlns="http://s3.amazonaws.com/doc/2006-03-01/">
  <CORSRule>
    <AllowedOrigin>*</AllowedOrigin>
    <AllowedMethod>GET</AllowedMethod>
    <AllowedMethod>POST</AllowedMethod>
    <AllowedMethod>PUT</AllowedMethod>
    <MaxAgeSeconds>3000</MaxAgeSeconds>
    <AllowedHeader>Authorization</AllowedHeader>
  </CORSRule>
</CORSConfiguration>
```

https://aws.amazon.com/cli/

```
pip
aws configure
```

It access for access id and secret key.
Then region
then default output
