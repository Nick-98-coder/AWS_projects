### AWS project1
# Hosting static website.
***
The below plan is my architechture.

&nbsp; &nbsp; &nbsp; &nbsp; <img width="630" alt="image" src="https://user-images.githubusercontent.com/74515760/209599126-e8b45f82-81bf-48e8-bc99-bdde923b9415.png">


Creating two new S3 bucket with a Unique names as `www.myelearning.nk` &  `myelearning.nk` in the same availability zone.

	*(reason for creating two buckets : to redirect the content with both the names)*
	
&nbsp; &nbsp; &nbsp; &nbsp; <img width="483" alt="Screenshot_20221227_063653" src="https://user-images.githubusercontent.com/74515760/209595843-06535b77-b526-45d3-8261-5800bc306a22.png">

&nbsp; &nbsp; &nbsp; &nbsp; <img width="426" alt="Screenshot_20221227_070731" src="https://user-images.githubusercontent.com/74515760/209597630-5f8877f3-a0e3-4052-ac40-cc9a0f88c40f.png">

Providing public access to the buckets, so that the content can be access to public

The bucket with public access `www.myelearning.nk` 

&nbsp; &nbsp; &nbsp; &nbsp; <img width="461" alt="Screenshot_20221227_063739" src="https://user-images.githubusercontent.com/74515760/209597040-296ff68d-4543-4fc5-bccd-a94a9b5448f6.png">

The bucket without public access `myelearning.nk`

&nbsp; &nbsp; &nbsp; &nbsp;  <img width="602" alt="image" src="https://user-images.githubusercontent.com/74515760/209598090-9fb07f52-2b86-4a93-ba08-910c5e6d1416.png">

Uploading all the files to the bucket `www.myelearning.nk`

&nbsp; &nbsp; &nbsp; &nbsp; <img width="629" alt="image" src="https://user-images.githubusercontent.com/74515760/209600550-895ddda6-7f08-4118-9a01-f5e82fcdea9c.png">

Adding bucket policy for `www.myelearning.nk` . 
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::www.electronium.ga/*"
        }
    ]
}
```
&nbsp; &nbsp; &nbsp; &nbsp; <img width="386" alt="image" src="https://user-images.githubusercontent.com/74515760/209601182-e146456e-a5c4-421f-af38-3ca08dc69941.png">

Set a permission to static host website for accessing single links for all content inside buckets.

&nbsp; &nbsp; &nbsp; &nbsp; Before permission

&nbsp; &nbsp; &nbsp; &nbsp; <img width="327" alt="image" src="https://user-images.githubusercontent.com/74515760/209601607-4b5b65a0-a0a6-44eb-a868-cba6781dd7ed.png">

&nbsp; &nbsp; &nbsp; &nbsp; After Permission

&nbsp; &nbsp; &nbsp; &nbsp; <img width="675" alt="image" src="https://user-images.githubusercontent.com/74515760/209601671-40e22494-3789-4a92-9304-9c12c42545ff.png">

This is for second bucket permission to static host website. 

&nbsp; &nbsp; &nbsp; &nbsp; <img width="635" alt="image" src="https://user-images.githubusercontent.com/74515760/209603369-f07a3c11-b7ed-4f48-9c88-32ffdf54ee27.png">

Now, all set from S3 side. PFB output from the Static website link was genarated using S3 bucket.

&nbsp; &nbsp; &nbsp; &nbsp; <img width="1248" alt="image" src="https://user-images.githubusercontent.com/74515760/209604293-f5977251-1bae-4c2d-b5aa-9c6b7dbb6977.png">

I got a free domain name from freenom.com

<img width="876" alt="Screenshot_20230107_110037" src="https://user-images.githubusercontent.com/74515760/211133785-1f29f05e-d546-4693-9b41-e3a8f8067400.png">

Created Host zone in Route53 service in the name of `electronium.ga`. (I have created new bucket with name of `www.electronium.ga`and it is redirected to the bucket name `www.myelearning.nk`)

<img width="1034" alt="Screenshot_20230107_110230" src="https://user-images.githubusercontent.com/74515760/211133899-067d3acb-ed46-4a9d-8ea8-536b1e46bde7.png">

Created a new record with S3 endpoint as a alias name with `www.electronium.ga` 

<img width="1062" alt="Screenshot_20230107_110442" src="https://user-images.githubusercontent.com/74515760/211133964-44a2d1dd-e211-4967-8ea6-10dc6281bf7e.png">

The result is below with `www.electronium.ga` domain name service.

<img width="1280" alt="Screenshot_20230107_112945" src="https://user-images.githubusercontent.com/74515760/211134003-1b9c18c0-98d9-468d-95d4-481d93c33928.png">

Now, setting up with CloudFont.
Created required cloudfront by linking with S3 link.

<img width="1233" alt="image" src="https://user-images.githubusercontent.com/74515760/211135512-738f8949-89eb-4366-be4b-a4985bef06d2.png">

PFB CloudFont result with it's genrated link.

<img width="1273" alt="image" src="https://user-images.githubusercontent.com/74515760/211135522-c4ac2032-c65a-43b1-a617-a5f46f0becf4.png">

Now we have to modify the pointing path of the website.
So, The below path we have to achieve  
Route53 --> CloudFont --> S3 Buckets

To do those, modifying the Route53's records 

Before

<img width="1079" alt="image" src="https://user-images.githubusercontent.com/74515760/211135161-28a6177d-a9c8-4980-812b-0430ff883a8f.png">

After

<img width="1086" alt="image" src="https://user-images.githubusercontent.com/74515760/211140997-c5e380a4-9509-4a7f-9569-1157c82a804f.png">

Before this we have to create SSL certificate and attach to the Route53 records.
After this we can configure the CloudFont Distribution and can get a access to `www.electronium.ga` name. (Since freenom is free domain service, I m not able to get Amazon cerification to host.)

I hope the conculsion result will be same as the Route53 --> S3 bucket link result.

## My static website is launched successfully!
