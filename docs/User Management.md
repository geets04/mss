#User Management

##Via GUI:

System → Administration → Users and Groups

##Via Commandline:

    sudo su #Only mssadmin user is in sudoers group so log in as that user first

    useradd -m username #this adds user

    passwd username #creates password for user

    usermod -a -G epoptes username #adds user to epoptes group, needed only for teachers/admin accounts

Default server is shipped with the following user accounts
pre-configured i.e. if no customisation has been requested during order
placement -

**student accounts:** student1 to student100; **password:** 12345

**teacher accounts:** teacher1 to teacher10; **password:** imteacher