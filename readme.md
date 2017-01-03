## Instructions

- Clone this repo and cd into it.

- Run the following command to create the homestead config file:
```
// Mac / Linux...
bash init.sh

// Windows...
init.bat
```

- Open the /Users/{{YOURUSERNAME}}/.homestead/Homestead.yaml file.

- Map the folders you want to share with guest and host systems.

        map -> path of the project on host (you must have it before booting your vm, otherwise vagrant will complain)
        to  -> path on vagrant box

- Map the public folder of your project to a custom local domain, making it easier to access your site.

        sites:
            - map: myapplication.app
              to: /home/vagrant/Code/Laravel/public

- Edit the /etc/hosts file and include "192.168.10.10  myapplication.app"

- Now you'll be able to access your project at http://myapplication.app

- Run "vagrant up" to start your virtual machine

- Generate a new Laravel project
```
composer create-project laravel/laravel myapplication
```

- Update the paths of the shared folder if necessary (in case it's different from what you specified in the steps above)

Note:

- If you're connecting to databases from the hosting machine, the username and password for both databases is homestead / secret.

**@anazard**
