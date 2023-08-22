# Github Actions:
## V1: Java Console(Github Checkout, Install Java)
In this task I have to create a CI pipeleine.For this I need to install java and do Github checkout.<br>

--> Clone a Repositories(https://github.com/codingsenpai27/Repo1.git) <br>
--> Install Java. <br>
--> Compile the program <br>
--> Exceute the program <br>
--> Create a new branch. Ex-V1 <br>
--> Add all the changes. <br>

``` 
git add .

 ```

--> Commit all the changes. <br>

``` 
git commit -m "V1"

 ```

-->Push the changes to the branch. <br>

``` 
git push origin V1

```

```

name: Perform CICD Operations on Console Based Java Application
  on: push
  jobs:
    CICD:
      runs-on: ubuntu-latest
      steps:
        - name: 1. Clone Project
          uses: actions/checkout@v3     

        - name: 2. Set up JDK 17 From My Friend Temurin
          uses: actions/setup-java@v3
          with:
            java-version: '17'
            distribution: 'temurin'

        - name: 3. Compile Java Console App Project
          run: javac WelcomeWorld.java

        - name: 4. Check Class Generated
          run: ls -ltra

        - name: 5. Run Java Console App Project
          run: java WelcomeWorld

```
--> on: is for the command on which you want the file to be executed <br>
--> name: In this any text can be given. <br>
--> run: In run the command which needs to be executed <br>

![image](https://github.com/NubeEra-Projects/MedicalSystem/assets/103624779/75a84d39-f8c3-46df-837b-1b08c72546b4)




