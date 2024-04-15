It is a simple project to show how to use Allure report

1. Install Allure on your machine https://allurereport.org/docs/gettingstarted-installation/
2. Create JAVA project (Maven style)
3. In POM.xml add dependencies for TestNG, Allure
!!! To see code snippets please open readme.md in edit mode !!!

  <dependencies>
       <!-- allure with testng dependency -->
        <dependency>
            <groupId>io.qameta.allure</groupId>
            <artifactId>allure-testng</artifactId>
            <scope>test</scope>
        </dependency>

        <!-- Testng dependency -->
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>7.10.1</version>
            <scope>test</scope>
        </dependency>
    </dependencies>

    <!-- Add allure-bom to dependency management to ensure correct versions of all the dependencies are used -->
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>io.qameta.allure</groupId>
                <artifactId>allure-bom</artifactId>
                <version>2.24.0</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>

4. Run tests

5. Check if a folder named allure-results in generated

6. To visualize results you need to start local server for allure reports with the following command 
allure serve path_to_the_folder_allure-results


Example:

allure serve /Users/tsstrelkova/Downloads/TT/allure-results


!! You  need to stop server before visualization of the next report
   The server can be stopped with Ctr+C !!


Tutorials:

https://www.swtestacademy.com/allure-report-testng/

Some udemy course:
https://www.udemy.com/course/rest-assured-java-api-automation-for-beginners/learn/lecture/37977992#notes:~:text=70.-,How,-to%20generate%20Allure
