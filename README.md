# Devops Fresher Labs
## Lab 1: Manage files and directories  
- Command "**mkdir**" && "**tree**": Using command **mkdir** to make a new folder and using **tree** to locate folder
  ![image](https://github.com/user-attachments/assets/d9625256-962f-473a-a61e-b49b41f75e2c)


- Command "**cp**" (copy files and folders) "**mv**" (move files or folders):
  ![image](https://github.com/user-attachments/assets/e86dfea0-8533-483b-947c-f27db6f23ed8)

  
- Show the full path of the directories using "**pwd**":
  ![image](https://github.com/user-attachments/assets/342a9cfb-aef7-4945-aa8f-85abe1ff8928)


- Compress, extracts files using "**zip**":
  ![image](https://github.com/user-attachments/assets/19b184ec-83c2-4037-8c2f-291dd4e7b387)

- Edit files using "**nano**":
  ![image](https://github.com/user-attachments/assets/fc977951-113d-45c1-8075-33f5e61697d1)

- Transfer files using "**WinSCP**":
  + First we will need to check if the sshd service is active or not. By using the command **systemctl status sshd**:
    ![image](https://github.com/user-attachments/assets/0601cfc3-7d57-4e13-bb6c-713fb6312476)

  + Second we will check the **IP Adress** by using the command **ifconfig**:
  ![image](https://github.com/user-attachments/assets/6e01fd5a-622b-4460-b764-ffbbf74fa7b0)

  + After having the informations that we need. We using the WinSCP application to transfer the files via **SCP**:
   ![image](https://github.com/user-attachments/assets/aee43232-8239-4286-98bb-59e94f3bb1c9)

   ![image](https://github.com/user-attachments/assets/e3dbc60a-0d88-42fd-9eca-846cf9bc0a0a)

## Lab 2: Managing software, system and network  
- Using apt, apt-get, dpkg, … manage package update, install, remove software (nginx, apache2, sql, …):
  + Using "**apt list --installed**" or using "**dpkg --get-selections**" to get all the installed software :
    ![image](https://github.com/user-attachments/assets/ca8b1236-8063-453e-b5e5-dc889b699150)
    ![image](https://github.com/user-attachments/assets/453abf7a-9fc9-4264-8e81-d274af2a29a5)

  + Using "**sudo apt-get install [package_name]**" to install the software you needed:
    ![image](https://github.com/user-attachments/assets/39349f7b-d1e9-44af-a0aa-daf2f1824aec)

  + Using "**sudo apt-get update**" to update the lastest software versions of all your packages:
    ![image](https://github.com/user-attachments/assets/fc60a763-3f17-4975-a57b-001a815aec1e)

  + Using "**sudo apt-get install --only-upgrade <package-name>**" to update the lastest software based on your package's name:
    ![image](https://github.com/user-attachments/assets/7fa46abb-d291-4cd0-bf0f-208e9ec6dbd0)

    





