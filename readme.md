Welcome ,, if you have any confusion with the vpc configuration in aws , youre in a right place buddy . lets start !!
1️⃣ Create a VPC → Acts like a private land with boundaries.

2️⃣ Create a Subnet (Private by Default) → A smaller area inside the VPC with an AZ , and provide the CIDR which must be within the range of the vpc . For example: if the vpc CIDR range is 10.0.0.1/16 (65536 ip's) , then the subnet CIDR may be 10.0.0.1/24 ( smaller that vpc cidr )

3️⃣ Create an Internet Gateway (IGW) & Attach it to the VPC → This is the main door to connect the VPC to the internet.

4️⃣ Create a Route Table → Acts like a roadmap that tells traffic where to go. so here choose the roadmap for which vpc or , choose the route table for the vpc you want.

5️⃣ Edit the Route Table → set one target as the IGW and destinatin to 0.0.0.0/0,, means one end of the road would connect to IGW and one end of the road to subnet.

0.0.0.0/0 → Internet Gateway (IGW) (Meaning all internet traffic should go through IGW) 6️⃣ Associate the Route Table with the Subnet → Now, the subnet has a road leading to the IGW. now associate means we are connecting both end of the roads .

7️⃣ Subnet Becomes Public → Because now it has a pathway (route table) to the IGW.
