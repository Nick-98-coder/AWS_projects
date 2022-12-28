# AWS 3-Tier Architecture

![Screenshot_20221228_165551](https://user-images.githubusercontent.com/74515760/209805148-d6ff69c1-4053-4cff-b87a-f89e1d6c0bb1.png)

Creating VPC:

![Screenshot_20221228_104846](https://user-images.githubusercontent.com/74515760/209761543-c03cb5d3-a93e-4075-b668-7c243fa3c247.png)

Subnets:

![Screenshot_20221228_105407](https://user-images.githubusercontent.com/74515760/209762017-73109666-895e-42ae-9d87-8c878bb3d99d.png)

Route Table:

![Screenshot_20221228_105536](https://user-images.githubusercontent.com/74515760/209762160-9d1db34f-f6a0-4184-b7db-5f23217fffd5.png)

Internet Gateway

![Screenshot_20221228_105610](https://user-images.githubusercontent.com/74515760/209762231-31d97f99-5993-496c-8bb4-e3674e4011a6.png)

Security groups

![Screenshot_20221228_105652](https://user-images.githubusercontent.com/74515760/209762302-96dfe4ee-8927-4983-8298-1271dfe58fc1.png)

NAT Gateway

![Screenshot_20221228_153839](https://user-images.githubusercontent.com/74515760/209795545-93b155cf-ab1b-4d7b-a32e-7a0ad5f45fc7.png)

Configured in route table to access Internet for private networks

![Screenshot_20221228_153928](https://user-images.githubusercontent.com/74515760/209795654-ed2dffe2-8f05-493f-88df-8a201726f0cf.png)

### Creating front-end-server

![Screenshot_20221228_110113](https://user-images.githubusercontent.com/74515760/209762615-9a30edb8-fb08-4284-815b-40c5c233a000.png)

![Screenshot_20221228_111146](https://user-images.githubusercontent.com/74515760/209763600-57753bf4-2a4d-4e09-8834-a5a7347291ab.png)

![Screenshot_20221228_110951](https://user-images.githubusercontent.com/74515760/209763443-cbef5ec3-8062-4066-b5cd-0dd716d468a6.png)

## Creating Application-server

![Screenshot_20221228_111253](https://user-images.githubusercontent.com/74515760/209763700-c263f5bb-c17c-44cd-8e74-89006b34ceaf.png)

![Screenshot_20221228_111414](https://user-images.githubusercontent.com/74515760/209763838-3c23ce8b-30e1-40d4-8c85-ade8d15ed04e.png)

![Screenshot_20221228_113812](https://user-images.githubusercontent.com/74515760/209766222-72e8859b-502d-4b13-85bf-e6856b5cf225.png)

Instance status

![Screenshot_20221228_115731](https://user-images.githubusercontent.com/74515760/209768289-1db5bdd8-b65c-4183-9f6c-bac76c2eaed2.png)

Front-end server & Installed Tomcat apache server

![Screenshot_20221228_120933](https://user-images.githubusercontent.com/74515760/209769537-af3fbd0f-7836-447d-9348-04d308f619df.png)

Application server & installed Java and nginx server

![Screenshot_20221228_151625](https://user-image![Screenshot_20221228_153603](https://user-images.githubusercontent.com/74515760/209795294-7ebf10fd-06d3-483a-b247-a7db5c754fd6.png)
s.githubusercontent.com/74515760/209792547-7a3b5272-e1e1-40cd-bd7e-f7115b203e8e.png)

![Screenshot_20221228_153230](https://user-images.githubusercontent.com/74515760/209794868-ae7384f3-277e-455a-a934-62f8c9bedcd8.png)

DB server & Installed MariaDB

![Screenshot_20221228_153603](https://user-images.githubusercontent.com/74515760/209795399-722c4aa8-5c52-4e97-9fcd-9f67259a82fa.png)

# Done! My 3-Tier Environment is ready.
