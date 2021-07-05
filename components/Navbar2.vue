<template>



        <!--============= Navbar =============-->
        <nav class="navbar">
            <div class="container">

                <!-- Navbar Header [collects both toggle button and navbar brand] -->
                <div class="navbar-header">
                    <!-- Toggle Button [handles opening navbar menu on mobile screens]-->
                    <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#exampleNavComponents" aria-expanded="false">
                        <i class="glyphicon glyphicon-align-center"></i>
                    </button>

                    <!-- Navbar Brand -->
                    <a href="#" class="navbar-brand">
                        Bootstrap Navbar
                    </a>
                </div>


                <!-- Navbar Collapse [collect navbar components such as navbar links and forms ] -->
                <div class="collapse navbar-collapse" id="exampleNavComponents">

                    <!-- Navbar Links -->
                    <ul class="nav navbar-nav navbar-right">
                        <li><a href="#">Page 1</a></li>
                        <li><a href="#">Page 2</a></li>
                        <li><a href="#">Page 3</a></li>
                    </ul>

                    <!-- Navbar Form -->
                    <form action="#" class="navbar-form navbar-right">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Search">
                        </div>
                        <button type="submit" class="btn">Submit</button>
                    </form>

                    <!-- Navbar Button -->
                    <button type="button" class="btn navbar-btn navbar-right">Sign in</button>

                </div>
            </div>

        </nav><!-- /.============= Navbar =============-->



        

</template>
<script>
$(document).ready(function() {
  // Calculating the distance from the top of the page to the initial position of the navbar, and store it in a variable
  var navbarOffest = $(".navbar").offset().top;

  $(window).on("scroll", function() {
    var navbarHeight = $(".navbar").outerHeight();

    if ($(window).scrollTop() >= navbarOffest) {
      $(".navbar").addClass("navbar-fixed-top");
      $("body").css("padding-top", navbarHeight + "px");
    } else {
      $(".navbar").removeClass("navbar-fixed-top");
      $("body").css("padding-top", "0");
    }
  });
});
</script>
<style>
   nav.navbar {
    background: #6d7fcc;
    color: #fff;
    border-bottom: none;
    border-radius: 0;
    box-shadow: 2px 2px 7px rgba(0, 0, 0, 0.2);
    padding: 15px 0;
    -webkit-transition: all 0.5s;
    -o-transition: all 0.5s;
    transition: all 0.5s;
}

/* Navbar Brand */
nav.navbar a.navbar-brand {
    color: #fff;
    font-weight: 600;
}
    nav.navbar a.navbar-brand:hover,
    nav.navbar a.navbar-brand:focus {
        color: inherit;
    }


/* Toggle Button */
nav.navbar .navbar-toggle {
    background: #fff;
    color: #333;
    border: none;
    border-radius: 0;
}
    nav.navbar .navbar-toggle:hover,
    nav.navbar .navbar-toggle:focus {
        background: #fff;
        color: #333;
    }

/* Navbar Components Holder */
nav.navbar .navbar-collapse {
    border: none;
}

/* Navbar links */
nav.navbar ul.navbar-nav {
    border: none;
}

nav.navbar ul.navbar-nav a {
    color: #fff;
}
    nav.navbar ul.navbar-nav a:hover,
    nav.navbar ul.navbar-nav a:focus {
        color: #333;
        background: #fff;
    }



/* Navbar Form */
nav.navbar form.navbar-form input {
    border-radius: 0 ;
    border-color: #6172b9;
    background: none;
    color: #fff;
    font-weight: 300;
}

nav.navbar form.navbar-form button {
    background: #6172b9;
    color: #fff;
    border-color: #6172b9;
    border-radius: 0;
    box-shadow: none !important;
    outline: none;
}
    nav.navbar form.navbar-form button:hover {
        background: #fff;
        color: #6172b9;
    }

/* Navbar Button */
nav.navbar button.navbar-btn {
    border-radius: 0;
    border-color: #6172b9;
    background: #6172b9;
    color: #fff;
}
    nav.navbar button.navbar-btn:hover {
        background: #fff;
        color: #6172b9;
    }
</style>
