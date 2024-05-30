# Add-and-manage-users-with-Linux-commands-Activity (Edit Formmatting later)
Add and manage users with Linux commands (Activity)


In this activity, you’ll learn how to add users and manage user access in a system. These skills can be used when working with authentication technology. You’ll use Linux commands in the Bash shell to complete this activity.

You have multiple tasks in this Activity:
Add a new employee
Change ownership of a file
Add the new employee to a new group
Delete the employee from the system

1. Add a new user
A new employee has joined the Research department. In this task, you must add them to the system. The username assigned to them is researcher9.

Write a command to add a user called researcher9 to the system.
- sudo useradd researcher9
Next, you need to add the new user to the research_team group.
Use the usermod command and -g option to add researcher9 to the research_team group as their primary group.
- usermod -g research_team researcher9

Task 2. Assign file ownership
The new employee, researcher9, will take responsibility for project_r. In this task, you must make them the owner of the project_r.txt file.

The project_r.txt file is located in the /home/researcher2/projects directory, and owned by the researcher2 user.
Use the chown command to make researcher9 the owner of /home/researcher2/projects/project_r.txt.

navigate to where project_r.txt is located
- cd /home/researcher2/projects
type the command to change project_r.txt ownership to researcher9
- sudo chown researcher9 project_r.txt

Task 3. Add the user to a secondary group
A couple of months later, this employee's role at the organization has changed, and they are working in both the Research and the Sales departments.

In this task, you must add researcher9 to a secondary group (sales_team). Their primary group is still research_team.

Use the usermod command with the -a and -G options to add researcher9 to the sales_team group as a secondary group.
Note: Options for Linux commands are case-sensitive, so make sure you use a lowercase -a and an uppercase -G.

- sudo usermod -a -G sales_team reseacher9

Task 4. Delete a user
A year later, researcher9, decided to leave the company. In this task, you must remove them from the system.

Run a command to delete researcher9 from the system:
- sudo userdel researcher9
This command will output the following message:
- Userdel: Group researcher9 not removed because it is not the primary group of user researcher9.
This is expected.

Note: When you create a new user in Linux, a group with the same name as the user is automatically created and the user is the only member of that group. After removing users, it is good practice to clean up any such empty groups that may remain behind.
Run the following command to delete the researcher9 group that is no longer required:
- sudo groupdel researcher9

Conclusion
You now have practical experience in using basic Linux Bash shell commands to

add a new user,
add a user to a group,
change user permissions on files, and
delete a user.

