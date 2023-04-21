 /
    - src /
        index.js // server
        models/
        controllers/
        middlewares/
        services/
        utils/
        config/
        repository/
    
    - tests / [later]

    # Project setup
       - clone the project on your local
       - execute `npm install` on the same path as of your root directory of the 
         download project
       - Create a `.env` file in the root directory and add the golling environment
         variables
            - `PORT = 3000`
       -Inside the `src/config` folder create a new file `config.json` and then ass 
        following piece of json

    ```  

          {
                "development": {
                "username": "<your bd name>",
                "password": "<your db password>",
                "database": "Flights_Search_DB_DEV",
                "host": "127.0.0.1",
                "dialect": "mysql"

             }
        }

        Onces you addes your db config as listed above, go to the src folder your 
        terminal and execute `npx sequlize db:create`
        and then execute 

        `npx sequelize db:migrate`


    ``` 

  ## DB Design
     - Airplane Table
     - Flight
     - AirPort
     - CIty

     - A flight belongs to the airport but one airplane can be used in multiple flights
     - A city has many airports but one airport belongs to a city
     - One airport can have many Flights , but a flight belongs to one airport 

 ## Table
     ### City -> id , name , created_at , updated_at
     ### Airport -> id , name, address , city_id , created_at , updated_at
          Relationship -> City has many airports and airports belongs to the city (one to many) 
  
