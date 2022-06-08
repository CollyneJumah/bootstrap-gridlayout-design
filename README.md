## NavBar
 Includes support for branding, navigation, and more, including support for our collapse plugin.

 ### How it works
 - Navbars require a wrapping .navbar with .navbar-expand{-sm|-md|-lg|-xl|-xxl} for responsive collapsing.
 - Navbars are responsive by default, but you can easily modify them to change that. Responsive behavior depends on our Collapse JavaScript plugin.
 - Ensure accessibility by using a `<nav>` element or, if using a more generic element such as a `<div>`, add a role="navigation" to every navbar to explicitly identify it as a landmark region for users of assistive technologies.
 - Indicate the current item by using `aria-current="page"` for the current page or aria-current="true" for the current item in a set.

 ### Setting Up
 #### 1. Create `nav` tage element. 
 ```
 <nav class="navbar navbar-expand-lg bg-light">
 </nav>
 
 ```

 We are adding classes `navbar, navbar-expand-lg` for responsiveness. `g-light` will be the background color.

#### 2. Wrap inside the `.container` class to center all its content on the page.

```
<div class="container-fluid">
      <a class="navbar-brand" href="#">Navbar</a>
      << add the toggle button for menu on smaller devices>>
</div>

```
 `.navbar-brand` class can be used for your company, product, or project name. Its usually a link.

#### 2.b Toggle button

```

<button class="navbar-toggler" type="button" data-bs-toggle="collapse"                   data-bs-target="#navbarDisplayNavigations" aria-controls="navbarDisplayNavigations" aria-expanded="false" aria-label="Toggle navigation">
<span class="navbar-toggler-icon"></span>
</button>

```
#### 2.c Add your navigation list items

```
<div class="collapse navbar-collapse" id="navbarDisplayNavigations">
      <div class="navbar-nav">
        <a class="nav-link active" aria-current="page" href="#">Home</a>
        <a class="nav-link" href="#">Features</a>
        <a class="nav-link" href="#">Pricing</a>
        <a class="nav-link disabled">Disabled</a>
      </div>
    </div>

```

NB: For the toggle to work, remember to target the `id` attribute of your `<div>`. 

### 3. Adding fixed navigation
We can make our `navigations` fixed at the top by applying the class `fixed-top` in the parent `nav`.
Add a `.shadow` class. 