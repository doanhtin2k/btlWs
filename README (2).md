create project
    taskservice: 
    
        create project: curl -s "https://laravel.build/taskservice" | bash
        
            add jetstream : composer require laravel/jetstream
            
            add inertia : sail php artisan jetstream:install inertia
            npm: npm install
            
                npm install -D tailwindcss
                
                npm install vue-loading-overlay@^5.0 
        
        service 1
            create project: curl -s "https://laravel.build/service1" | bash
        service 2
        create project: curl -s "https://laravel.build/service2" | bash
Config Port:

    taskservice: 
                APP_PORT=80
                mysql 3306
                adminer 8080
    service 1
                APP_PORT=3001
                mysql 33061
                adminer 8081


    service 2
                APP_PORT=3002
                mysql 33062
                adminer 8082
     
                
                
