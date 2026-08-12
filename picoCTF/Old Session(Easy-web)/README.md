
<img width="876" height="819" alt="1" src="https://github.com/user-attachments/assets/cc483aaa-63dc-48c1-aefc-3ef2a965baf8" />
hello guys ,today i will explain how i analyzed Old session challenge ,first the challenge talk about session that being active indefinitely 
and that is vulnerability we can exploiting it.

<img width="1600" height="875" alt="2" src="https://github.com/user-attachments/assets/3ea580dd-c22d-43fd-abed-02b7ec8c3f49" />

moreover, when I open a website i saw login site and always in any challenge in web we should interact with a website like a normal user in first 

<img width="1600" height="865" alt="3" src="https://github.com/user-attachments/assets/f96bd9d7-d07a-4cd1-a1ea-30d18cadece3" />

so i register in a website with a random username and password 

<img width="1600" height="868" alt="4" src="https://github.com/user-attachments/assets/1c450a87-beec-4d59-a462-2374d3aba27f" />

after that i login with my new account 


<img width="1600" height="869" alt="5" src="https://github.com/user-attachments/assets/5d1da8a6-a49a-44a3-8d15-5b66fdc3d7fd" />

then a homepage is pooped and there is a four comment for some user but a one who marry_jones write is very interest 

<img width="1600" height="878" alt="6" src="https://github.com/user-attachments/assets/ea8cc622-18ef-4829-9634-1a392e996456" />

so I write a path and boom!! marry is right there is a strange page here ,but if we just focus a littel we will see ID session and key 
for admine site and a thing that is more important is a permanent value is true .

<img width="1600" height="861" alt="7" src="https://github.com/user-attachments/assets/a89a0842-db5c-4367-9f43-1982e06c4905" />

 in this point a normal user experince is end , I use curl command here to change a header and more specifically to change a cookie to make it
 send a specific session(and I select a session with a ID ) , so relationship between that three is : header have a cookie as a part of it and a cookie have a session data as a part of it.

and congrat!!! you have now i site with html markup language and in it there is a flag 


thank you for read my writeups!!!
