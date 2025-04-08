# Devops Fresher Labs
## Lab 1: Manage files and directories  
### Command "**mkdir**" && "**tree**": Using command **mkdir** to make a new folder and using **tree** to locate folder
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
### Using apt, apt-get, dpkg, … manage package update, install, remove software (nginx, apache2, sql, …):
  + Using "**apt list --installed**" or using "**dpkg --get-selections**" to get all the installed software :
    ![image](https://github.com/user-attachments/assets/ca8b1236-8063-453e-b5e5-dc889b699150)
    ![image](https://github.com/user-attachments/assets/453abf7a-9fc9-4264-8e81-d274af2a29a5)

  + Using "**sudo apt-get install [package_name]**" to install the software you needed:
    ![image](https://github.com/user-attachments/assets/39349f7b-d1e9-44af-a0aa-daf2f1824aec)

  + Using "**sudo apt-get update**" to update the lastest software versions of all your packages:
    ![image](https://github.com/user-attachments/assets/fc60a763-3f17-4975-a57b-001a815aec1e)

  + Using "**sudo apt-get install --only-upgrade <package-name>**" to update the lastest software based on your package's name:
    ![image](https://github.com/user-attachments/assets/7fa46abb-d291-4cd0-bf0f-208e9ec6dbd0)

  + Using "**sudo apt-get remove [packge_name]**" to remove the package you want:
    ![image](https://github.com/user-attachments/assets/5e52c450-d770-47c9-a7f9-28c02f112c8b)
  + You can clean up these packages using the "**sudo apt-get autoremove**":
    ![image](https://github.com/user-attachments/assets/d8c9e3cd-6920-4647-ab63-70d87706b964)

### Managing system (task, service, …) use tool: ps, top, htop, kill, grep process:
  + Using "**ps aux**" to list all the running services:
    ![image](https://github.com/user-attachments/assets/80338b66-14fe-4793-9abe-a4deec7674e1)

  + Using "**ps**" only show the processes running in the current shell (terminal session):
    
    ![image](https://github.com/user-attachments/assets/525d5d26-ae0b-4107-8073-600ee2809147)

  + Using "**top**" to show the running process in your shell:
    ![image](https://github.com/user-attachments/assets/0600bdd2-4a06-4086-8a56-e53e3cdb6ae4)

  + Using "**htop**" to easier to manage your process:
    ![image](https://github.com/user-attachments/assets/8e8b8dd8-3f9f-4646-8102-d7622b7bc1e9)

  + Using "**kill**" to kill a process or using "**kill -9 [process_PID]** to force kill a process by PID. And you can find your PID's process is running by using "**top | grep "your_process_name"**":
    
    + Before kill the firefox's process: 
    ![image](https://github.com/user-attachments/assets/d304e858-42f9-4775-9313-c043fcaab34e)
    
    + After kill the firefox's process:
    ![image](https://github.com/user-attachments/assets/6070617e-e8de-4a5f-8ee5-36303853832d)

  + Using "**netstat**" to display network connections, routing tables, interface statistics, ... :
    ![image](https://github.com/user-attachments/assets/f00e1326-83c9-45c3-a72e-5fd91840a9cb)

  + Using "**netstat -a**" to display all listening port for both TCP and UDP:
    ![image](https://github.com/user-attachments/assets/04d6c645-0ac0-4c3f-9843-cb97d5b574eb)

  + Using "**netstat -t**" to display all listening port for only TCP and using  "**netstat -au**" for UDP only:
    ![image](https://github.com/user-attachments/assets/52e08a08-c761-42d3-8f52-e63133995385)

## Lab 3: Shell Scripts / Bash scripting:
### Assignment 1: Comparing numbers:
<pre> bash #!/bin/bash
  # Read input
  read X 
  read Y 
  # Compare the numbers
  if [ "$X" -lt "$Y" ];
    then echo "X is less than Y"
  elif [ "$X" -gt "$Y" ];
    then echo "X is greater than Y" 
  else echo "X is equal to Y" fi 
</pre>
![image](https://github.com/user-attachments/assets/9a3bd39e-4ca8-4e53-8abd-b631ede8cfb7)

### Assignment 2: Calculate the math expression
<pre> 
  #!/bin/bash
  # Read the mathematical expression from user input
  echo "Enter a mathematical expression:"
  read expression
  # Remove any spaces from the input
  expression=$(echo "$expression" | tr -d ' ')
  # Calculate using bc with scale=3 for 3 decimal places
  result=$(echo "scale=3; $expression" | bc)
  echo "$result" 
</pre>
![image](https://github.com/user-attachments/assets/1dce4a7d-80d1-410d-adeb-ccc72a2519ff)
### Assignment 3: Unique number(s)
<pre> 
  #!/bin/bash
  # Read the number of integers
  read n
  # Read the array of space-separated integers
  read -a numbers
  # Initialize result as the first number
  result=${numbers[0]}
  # XOR all numbers to find the unique one
  for num in "${numbers[@]:1}"; do
    result=$((result ^ num))
  done
  # Display the result
  echo "$result"
</pre>
![image](https://github.com/user-attachments/assets/466b7f2e-5f7e-4ac5-b6e9-bf796cd3dc5e)






    




    





