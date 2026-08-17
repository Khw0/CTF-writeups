
<img width="1600" height="873" alt="1 " src="https://github.com/user-attachments/assets/4eb75a08-7ae8-44eb-9511-a2ffbef6c723" />

hello guys today I'll explain how I analyzed that challenge 

so a challenge give me three things: source code with python language , list of username-password pair , and website

<img width="1600" height="879" alt="2" src="https://github.com/user-attachments/assets/4566529d-ee20-48f7-ba44-41232ab5637c" />

firstly, i open a website and interact with it to know how it work and I didn't notice anything strange


<img width="1600" height="933" alt="3" src="https://github.com/user-attachments/assets/2fda2c6e-52e4-443f-a135-9623dd485f2f" />

secondly , I print a source code and read it to understand how this website works under the hood , so one of things i saw is: there is a homepage if I login correctly it will give me a flag , I made sure there is a system that locked a user out if he use a brute force and a limit of requests is 10 in 30 seconds and a user lock out is end after 120 second.
but if we focus a little we will see in APP ROUTE section there is an important TODO(to do) author write :check rate limit 
and because this point we can conclude a condition he write not present in app route 


<img width="1600" height="956" alt="4" src="https://github.com/user-attachments/assets/c0fbfe2a-0e62-477e-a1ad-aa7c942734ea" />

moreover, only a list of paswsword and username left , so I print it to check it and there nothing strange here, and now we need a way to send many POST requests that use our list so I use a burpsuit



first I open a burpsuite and made a new project ,after that I have a two options : link my browser with proxy or just use a burpsuit browser so I do second option 

after I open a website in a burpsuit browser i send a random username and password from login page

<img width="1280" height="774" alt="5" src="https://github.com/user-attachments/assets/6a8d866c-415d-48ad-8ac0-bad2412ca45b" />

 after that a went to HTTP history and I saw my POST request so I just right click on it and choose  (send to intruder) 
 
  
  <img width="1600" height="967" alt="6" src="https://github.com/user-attachments/assets/140bc578-f7ab-4fa9-b931-329ca6b8844b" />

<img width="1600" height="960" alt="7" src="https://github.com/user-attachments/assets/f13750fb-3ddf-476c-9b1e-dd1c76956f46" />


 first of all I change a kind of attack to (pitchfork) because i have a pair of username-password and a main difference in this attack can a make two payload that send together and each one of it have its list
 
 after that  click option clear& and select a place I want an ampersand on it
 
 after I select a two payload I divided a list to two section (with cut command in terminal) and I added a each of them in a payload that fits it
 
 <img width="1600" height="930" alt="8" src="https://github.com/user-attachments/assets/09682d71-3c31-4aa3-b702-ef6fcb17e801" />
 
now a attack is start!! in this stage all my focus was in length of response

<img width="1600" height="949" alt="9" src="https://github.com/user-attachments/assets/17070dd9-0a76-4102-a7a2-b679c8b3ff36" />

that request is an only request that have a different length so I click right on it and send it to repeater 


<img width="1600" height="968" alt="10" src="https://github.com/user-attachments/assets/e96927a1-c1c4-4225-b799-5dd4e93da496" />
 it's a 302 status!! 
 
 
 <img width="1600" height="878" alt="12" src="https://github.com/user-attachments/assets/53e41dc0-6454-47f5-b9be-9ca595bc9324" />

 so i took a password and username and login with them 
 
 
 <img width="1600" height="970" alt="11" src="https://github.com/user-attachments/assets/415699a5-f98d-4e7f-98ee-7a3c1367af24" /> 

 congrat!!! we found a flag


 thank you for read my writups

 

 

 
 


 




