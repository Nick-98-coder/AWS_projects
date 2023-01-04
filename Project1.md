### AWS project1 - WIP
# Hosting static website.
***
The below plan is my architechture.

&nbsp; &nbsp; &nbsp; &nbsp; <img width="630" alt="image" src="https://user-images.githubusercontent.com/74515760/209599126-e8b45f82-81bf-48e8-bc99-bdde923b9415.png">


* Step-1: Creating two new S3 bucket with a Unique names as `www.myelearning.nk` &  `myelearning.nk` in the same availability zone.

	*(reason for creating two buckets : to redirect the content with both the names)*
	
&nbsp; &nbsp; &nbsp; &nbsp; <img width="483" alt="Screenshot_20221227_063653" src="https://user-images.githubusercontent.com/74515760/209595843-06535b77-b526-45d3-8261-5800bc306a22.png">

&nbsp; &nbsp; &nbsp; &nbsp; <img width="426" alt="Screenshot_20221227_070731" src="https://user-images.githubusercontent.com/74515760/209597630-5f8877f3-a0e3-4052-ac40-cc9a0f88c40f.png">

* Step-2: Providing public access to the buckets, so that the content can be access to public

The bucket with public access `www.myelearning.nk` 

&nbsp; &nbsp; &nbsp; &nbsp; <img width="461" alt="Screenshot_20221227_063739" src="https://user-images.githubusercontent.com/74515760/209597040-296ff68d-4543-4fc5-bccd-a94a9b5448f6.png">

The bucket without public access `myelearning.nk`

&nbsp; &nbsp; &nbsp; &nbsp;  <img width="602" alt="image" src="https://user-images.githubusercontent.com/74515760/209598090-9fb07f52-2b86-4a93-ba08-910c5e6d1416.png">

* Step-3: Uploading all the files to the bucket `www.myelearning.nk`

&nbsp; &nbsp; &nbsp; &nbsp; <img width="629" alt="image" src="https://user-images.githubusercontent.com/74515760/209600550-895ddda6-7f08-4118-9a01-f5e82fcdea9c.png">

* Step-4: Adding bucket policy for `www.myelearning.nk` . 

&nbsp; &nbsp; &nbsp; &nbsp; <img width="386" alt="image" src="https://user-images.githubusercontent.com/74515760/209601182-e146456e-a5c4-421f-af38-3ca08dc69941.png">

* Step-5: Set a permission to static host website for accessing single links for all content inside buckets.

&nbsp; &nbsp; &nbsp; &nbsp; Before permission

&nbsp; &nbsp; &nbsp; &nbsp; <img width="327" alt="image" src="https://user-images.githubusercontent.com/74515760/209601607-4b5b65a0-a0a6-44eb-a868-cba6781dd7ed.png">

&nbsp; &nbsp; &nbsp; &nbsp; After Permission

&nbsp; &nbsp; &nbsp; &nbsp; <img width="675" alt="image" src="https://user-images.githubusercontent.com/74515760/209601671-40e22494-3789-4a92-9304-9c12c42545ff.png">

This is for second bucket permission to static host website. 

&nbsp; &nbsp; &nbsp; &nbsp; <img width="635" alt="image" src="https://user-images.githubusercontent.com/74515760/209603369-f07a3c11-b7ed-4f48-9c88-32ffdf54ee27.png">

Now, all set from S3 side. PFB output from the Static website link was genarated using S3 bucket.

&nbsp; &nbsp; &nbsp; &nbsp; <img width="1248" alt="image" src="https://user-images.githubusercontent.com/74515760/209604293-f5977251-1bae-4c2d-b5aa-9c6b7dbb6977.png">


