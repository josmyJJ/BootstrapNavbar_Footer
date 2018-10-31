# BootstrapNavbar_Footer
## Learning Objectives
* Using bootstrap navbar

## The Walkthrough

1. Create a Spring Boot Application
	* Name it BootsrapButtons
	* Add the dependencies for the web and for thymeleaf
	* Hit next until you finish the wizard, and then wait until it's done.

2. Create a Controller
	* Right click on com.example.demo and click New -> Class
	* Name it HomeController.java
	* Edit it to look like this:
```java
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
public class HomeController {

    @RequestMapping("/")
    public String index(){
        return "index";
    }
}
```

3. Create a Template
  * Right click on templates and click New -> Html
	* Name it index.html
	* Edit it to look like this:
```html
<!DOCTYPE html>
<html lang="en" xmlns:th="www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>Bootstrap 101 template</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Navbar</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse"
              data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
              aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ml-auto">

              <li class="nav-item active">
                  <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
              </li>
              <li class="nav-item dropdown">
                  <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown"
                     role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Dropdown
                  </a>
                  <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <a class="dropdown-item" href="#">Action</a>
                      <a class="dropdown-item" href="#">Another action</a>
                      <div class="dropdown-divider"></div>
                      <a class="dropdown-item" href="#">Something else here</a>
                  </div>
              </li>
              <li class="nav-item ">
                  <a class="nav-link" href="#">Item</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#">Link</a>
              </li>
          </ul>
      </div>
  </nav>


<footer>
  <nav class="navbar fixed-bottom navbar-expand-lg navbar-dark bg-dark">
      <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
              <li class="nav-item active">
                  <a class="nav-link" href="#">Home</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#">Features</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#">Pricing</a>
              </li>
          </ul>
      </div>
  </nav>
</footer>
</body>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
</html>
```

4. Run your application and open a browser, if you type in the URL http://localhost:8080 

## What is Going On
Navbar is placed at the top of the page. It provides an easy access to information.
navbar class goes on to the main container. All navigation elements will go on top of one other, and we have to add navbar-expand to specify when you want them to go horizontal.
Next we need to specify a color for the navbar. Here we have bg-light, which make the background light.
navbar-light class and bg-light class work together.    
Inside this main navbar class we need another container for navbar-nav. This is where your
main navigation will go.
Footer usually goes at the very bottom of a web page.
fixed-bottom class make sure that the navigation will stay at the bottom of the web page.
### The Controller
Here, the default route maps to index.html.

### The View

