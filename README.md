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

### Create Representation Class
Create a class to represent a blog post
```src/main/java/learn/java/Post.java```
```
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
