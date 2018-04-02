- ***Explain the purpose of the Test (what the original test exposed, and what your test exposes)***
To provide a product with the finest quality before we ARE required to test to make sure all the aspect of the product were concluded. Specifically this project gave us the understanding of what it feels like to work on someones else code which you just read and learnt for the first time. Doing so we now know the different approaches that in the future will increase the efficiency in our work when working on our own or someone else project.

	*The original test had issues with the approach. There were two tests one was for a single image test and the other one was to test all of the snapshots. The way the test for all snapshots was implemented leads to a problem of not knowing which snapshot was failed because when the test fails it does not indicate the exact image it just tells that the test failed.*

	*In the new test created we now see all of the separate passes and fails for each and every image, which will lead to easily finding the bugs.*

![New JUnit Test](https://github.com/Ekskursantas/JavaANPR/blob/master/JUNITTEST.png?raw=true)


----------


- ***Explain about Parameterized Tests in JUnit and how you have used it in this exercise***
	*As Parameterized Test repeatedly uses the same test with different parameters/values with loads of testing data this approach is the best as far as I can see to test all the images.*


----------


- ***Explain the topic Data Driven Testing, and why it often makes a lot of sense to read test data from a file***
There are many reasons what you would use Data Driven Testing. One of the them is that it makes the code more cleaning because you do not need to include hard coded values or randomizers to create inputs. You just read from a file which could contain a massive amount of data and that would not affect the readability of the code. Separating data and code improves efficiency as well.


----------


- ***Your answers to the question:***
	- *Whether what you implemented was a Unit Test or a JUnit Test?*
	*I believe it to be JUnit testing, I do not have any hard evidence, but when working with Java it is wiser to use JUnit.*


----------


- ***The steps you to include Hamcrest matchers in the project, and the difference they made for the test***
As it implies HamCrest is good to use for matching. Simple and easy to understand. 
![HC dependency](https://github.com/Ekskursantas/JavaANPR/blob/master/dependecies.png?raw=true)
```java
@Test
    public void recogniseIt() throws IOException{
        CarSnapshot carSnap = new CarSnapshot(new FileInputStream(file));
        String read = intel.recognize(carSnap);
        assertThat(carSnap, notNullValue());
        assertThat(read, notNullValue());
        assertThat(expectedResult, is(read));
    }

```

