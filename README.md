# Getting-Started-Unit-Testing-with-JUnit-5

WRITING A J-Unit 5 TEST
 -The order of a Test is....                                                                                                                               
    -SetUp - Setup code                                                                                                                                     
    -Execute - Code that calls the system to test                                                                                                           
    -Verify -Assertions to verify results
    
   
    
Writing More Complex Test

![image](https://user-images.githubusercontent.com/107411441/196058893-bdefb042-0587-41ff-900b-54ff3719c353.png)


    -Apply Data Assertion
        -There are many different Types of asserts such as assertSame, assertTrue, assertFalse, etc.
        
    -Setting up and tearing down tests
        -@BeforeAll will run once before all test methods in the class
        -@BeforeEach will run once before each method
        -@AfterAll will run once after all test methods in the class
        -@AfterEach will run once before each method
        -A repeating method such as Dog dog = new Dog; can be turned into a setup method to run before each method without having to repeat that line over and over.
        
    -Testing exceptions
        -Unit tests act as a safety net when refractoring and cleaning up code.
        -There are multiple ways and varations to run test exceptions in order to verify your test it testing properly.
    
    -Controlling Test Method Execusion
        -@Disable under @Test will disable that test and when ran it will show it was ignored.
        -commenting tests out would work also but the disadvantage to that is they would not be present on test report output and you would forget about it.
        -The very first AssertEquals failure will end the test method. basically short circuting.
        -assertAll(adding all the asserts in here with () -> behind each assert call) in order to test all the asserts without short circuting when one fails.
        
![image](https://user-images.githubusercontent.com/107411441/196209757-e3aefb48-7ae7-4ddb-8bc4-c90308d8b47c.png)

   -Running Group of Tests
        -@Tag("null") creating a tag in order to tests every test that has the keyword between the qoutations. If put above the class it will run all methods that contain the keyword. If put above the method it will only run that method.
        
