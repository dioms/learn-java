# learn-java
Learn how to create a website using java and spring.
[Using this guide](https://spring.io/guides/gs/rest-service/)
## Creating the Backend
- Install Git
- Install Java 8
- Install Maven 3
- Install Eclipse

### Getting Started
1. First, clone the repo
```git clone https://github.com/dioms/learn-java.git```
2. Open the project in Eclipse
3. Run maven install


### Learn about MVC
[Read this](http://www.tomdalling.com/blog/software-design/model-view-controller-explained/)

[Read this](http://code.tutsplus.com/tutorials/mvc-for-noobs--net-10488)

### Create Representation Class
Create a class to represent a blog post, this part is the "model" of MVC.
```
src/main/java/learn/java/Post.java
```
```java
package learn.java;

public class Post {

    private final String title;
    private final String content;

    public Greeting(String title, String content) {
        this.title = title;
        this.content = content;
    }

    public long getTitle() {
        return title;
    }

    public String getContent() {
        return content;
    }
}
```

### Create a Controller
This part is the "controller" of MVC.
```
src/main/java/learn/java/PostController.java
```
```java
package learn.java;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class PostController {

    @RequestMapping("value = /posts", method = RequestMethod.POST)
    public Post post(@RequestParam String title, @RequestParam String content) {
        return new Post(title, content);
    }
}
```

### Make the app executable
```
src/main/java/learn/java/Application.java
```
```java
package learn.java;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class Application {

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```
