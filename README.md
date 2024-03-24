# CyberGuard-Automation-Suite
Project2 Network Research/ Me
Running the script:
sudo ./Project2

Also please execute these two commands before running the script:

-	sudo apt-get update
-	sudo apt-get upgrade

The script won’t run well if not.


The script itself has a bunch of notes, if you read it you will probably understand all of it. however I shall explain the basics if you don’t really want to read everything.

In the scripts there are 12 functions overall.

1. function rm_logs_if_exist(): this function’s use is for organization purposes. This function is used for running the script a second time or more.

2. check_and_install_program: this function’s use is for checking if the programs already exist, if they exist continue, if not then download them and save the logs manually in “logs” folder.

the function is using a for loop, for optimization purposes. if you want to add another program simply write its name at the start of the loop.

3. check_if_installed: This function’s use is for checking if all the installations were successful. If not, run them again. The program runs them a maximum of 5 times.

4. spoofed_ip_and_country:  The function checks the spoofed IP and country given by nipe.

5. am_I_anonymous: The function checks if you as the user are anonymous. If not, it will retry until you are. At first I wanted to make the program recursive, but i thought it might run indefinitely due to internet connectivity and other issues. so I stayed with a simple structure of loops.

6 . ready_for_remote_address: This function exist only for organization purposes. All of what’s inside this function can be written without needing a function to run it. I just wanted my script to be neat and nice to read.

7. sanitize_address: The function takes the given remote address and sanitizes it, making it easier to read without any special characters such as ./! etc..

8. scan_remote_address: The function scans the remote address, but before that, the function also checks if the remote address given is valid or not, meaning it won’t scan regularly if the address given is not real/exists.

9. After this program will come the SSH part. Due to instructions from my teacher, I wasn’t allowed to automate this part. However I did make it easier for you. All you need to add to this part is:
ssh_user_info="kali@192.168.253.130" # FOR TESTER: change user and IP to match your own
ssh_user_password="kali" # FOR TESTER: change password to match your own
Change the red parts to match your own.

10. remote_server_whois_check: The function connects to the remote server, checks and saves the Whois data of the given remote address.

11. remote_server_scan: The function connects to a remote server, and scans+saves the given remote address.

12. details_of_remote_server: The function connects to the remote server, and saves the private data of the server,
including it’s private and public IP, uptime and country.

13. move_logs_to_big_folder: The function moves all the different logs into one log folder, that was made in the start, For organization purposes.

14. Other than those functions, I did add some other variables outside of the functions like current_dir=$(pwd), and others of the same sort.

15. Throughout the scripts output you will see [+]/[*]/[#], They serve no purpose other than beauty and organization. You can ignore.



