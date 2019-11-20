<template>    
  <div id="header-nav">
    <div class="container-fluid header-shadow d-sm-none d-md-block d-lg-block d-xl-block">
      <div class="pos-f-t d-xl-none d-sm-block d-lg-none d-md-none">
      <b-navbar toggleable="md" type="dark" id="#nav-menu" class="c-nav ">
        <b-navbar-brand href="#">NavBar</b-navbar-brand>
        <!-- Put the toggle here after the brand -->
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
          <b-collapse is-nav id="nav_collapse">
          <b-navbar-nav>
            <b-nav-item><nuxt-link to="/">Главная</nuxt-link></b-nav-item>
            <b-nav-item><nuxt-link to="/about">О нас</nuxt-link></b-nav-item>
            <b-nav-item><nuxt-link to="/contacts">Контакты</nuxt-link></b-nav-item>          
          </b-navbar-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown text="Dropdown link" right>
              <b-dropdown-group id="dropdown" header="Group 1">
                <b-dropdown-item href="#">Action</b-dropdown-item>
                <b-dropdown-item href="#">Another action</b-dropdown-item>
                <b-dropdown-item href="#">Subdopdown link</b-dropdown-item>
              </b-dropdown-group>
              <b-dropdown-group id="sub-dropdown" header="Group 1">
                <b-dropdown-item href="#">Second level</b-dropdown-item>
                <b-dropdown-item href="#">Second level</b-dropdown-item>
                <b-dropdown-item href="#">Second level</b-dropdown-item>
              </b-dropdown-group>
              <!-- Using button-content slot -->
              </b-nav-item-dropdown>
          </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </div>
  <div class="container">
    <b-row class="navbar-row">
      <b-col md="2">
        <div id="acc-pic" class="column d-sm-none d-md-block d-lg-block d-xl-block"><img  alt="" srcset=""></div>
      </b-col>
      <b-col md="10">
      <b-row class="navbar-row">
        <div id="nav-menu" align-self="end">
          <div id="nav-title" class="container-fluid w-100 d-sm-none d-md-block d-lg-block d-xl-block">
            <h2 class="color-red">My account</h2>
          </div>
            <nav class="navbar navbar-expand-lg navbar-light bg-light container-fluid w-100  d-none d-lg-block d-xl-block">
              <div class="collapse navbar-collapse">
                <ul class="navbar-nav mr-auto">
                  <li class="nav-item">
                    <nuxt-link exact no-prefetch active-class="active" class="nav-link" to="/">Главная
                    </nuxt-link>
                  </li>
                  <li class="nav-item">
                    <nuxt-link active-class="active" class="nav-link" to="/about">О нас
                    </nuxt-link>
                  </li>
                  <li class="nav-item">
                    <nuxt-link active-class="active" class="nav-link" to="/contacts">Контакты
                    </nuxt-link>
                  </li>
                  <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink">
                      Dropdown link
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink" >
                      <li class="dropdown-item">Action</li>
                      <li class="dropdown-item">Another action </li>  
                      <li class="dropdown-item dropdown-submenu">
                        <a tabindex="-1" href="#">Subdopdown link</a>
                        <ul class="dropdown-menu">
                          <li class="subdropdown-item" ><a tabindex="-1" href="#">Second level</a></li>
                          <li class="subdropdown-item" ><a href="#">Second level</a></li>
                          <li class="subdropdown-item" ><a href="#">Second level</a></li>
                        </ul>
                      </li>
                    </div>
                  </li>
              </ul>
            </div>
          </nav>
        </div>
      </b-row>
      </b-col>
    </b-row>
  </div>
</div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
#header-nav{
  margin-bottom: 3rem;
}

#acc-pic{
  border: 1px solid gray;
  background-color: red;
  width: 90%;
  height: 150px;
  margin: 0px auto;
  background-image: url(~assets/img/photo.jpg);
  box-shadow:0 1px 5px 0 rgba(0, 0, 0, 0.2)
}
#nav-title{
  padding: 1.5rem 0 1rem;
}
#nav-menu{
  width: 100%;
  float:right;
}
#nav-menu nav {
    border-radius: 10px;
    background: linear-gradient(0deg, rgba(221,221,221,1) 0%, rgba(217,217,217,1) 0%, rgba(233,233,233,1) 69%, rgba(255,255,255,1) 100%, rgba(235,235,235,1) 100%, rgba(219,219,219,1) 100%);
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.2);
    padding: 0;
}
#nav-menu .c-nav {
    border-radius: 10px;
    background: linear-gradient(0deg, rgba(221,221,221,1) 0%, rgba(217,217,217,1) 0%, rgba(233,233,233,1) 69%, rgba(255,255,255,1) 100%, rgba(235,235,235,1) 100%, rgba(219,219,219,1) 100%);
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.2);
    padding: 0;
}
a.nav-link{
  font-size: 1.2rem;
  margin: 0.5em 0!important;
  box-shadow:inset -3px 0px 2px -2px rgba(0,0,0,.2);
  padding-left: 1.5em!important;
  padding-right: 1.5em!important;
  white-space: nowrap;
}
li.nav-item{
  padding: 0;
}
.dropdown>.dropdown-menu {
  top: 200%;
  transition: 0.3s all ease-in-out;
  min-width: 250px;
}
.dropdown:hover>.dropdown-menu {
  display: block;
  background-color: #f2f2f2;
  top: 97%;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
  border-top: 2px inset rgba(0, 0, 0, 0.05);
      z-index: 99995;
}
.dropdown>.dropdown-toggle:active {
  /*Without this, clicking will make it sticky*/
    pointer-events: none;
}
button.navbar-toggler {
    border-radius: 5px;
    background: #999;
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.2);
    padding: 6px;
}
li.dropdown-item, li.dropdown-item a {
 color:#4e4e4e;
}
li.subdropdown-item, li.subdropdown-item a {
 color:#4e4e4e;
}
li.subdropdown-item a:hover {
 color:#c20016;
 text-decoration: none;
 visibility: visible;
}
li.dropdown-item:hover, li.dropdown-item:hover a {
 color:#c20016;
 text-decoration: none;
 visibility: visible;
}
li.dropdown-item.active, li.dropdown-item:hover:active {
    color: #c20016;
    text-decoration: none;
    background-color: #fff;
     visibility: visible;
}
.dropdown-submenu {
    position: relative;
}

.dropdown-submenu>.dropdown-menu {
    top: 0;
    left: 95%;
    margin-top: -3.6%;
    -webkit-border-radius: 0 6px 6px 6px;
    -moz-border-radius: 0 6px 6px;
    border-radius: 0 6px 6px 6px;
    background-color: #f2f2f2;
    min-width: 200px;
}

.dropdown-submenu:hover>.dropdown-menu {
    display: block;
}
li.subdropdown-item:hover{
    background-color: #fff;
}
.dropdown-submenu>a:after {
    display: block;
    content: " ";
    float: right;
    width: 0;
    height: 0;
    border-color: transparent;
    border-style: solid;
    border-width: 5px 0 5px 5px;
    border-left-color: #ccc;
    margin-top: 10px;
    margin-right: -10px;
}

.dropdown-submenu:hover>a:after {
    border-left-color: #fff;
}

.dropdown-submenu.pull-left {
    float: none;
}

.dropdown-submenu.pull-left>.dropdown-menu {
    left: -100%;
    margin-left: 10px;
    -webkit-border-radius: 6px 0 6px 6px;
    -moz-border-radius: 6px 0 6px 6px;
    border-radius: 6px 0 6px 6px;
}
.subdropdown-item a{
  color:#4e4e4e!important;
}

.subdropdown-item:hover a{
  color:#c20016!important;
}

.subdropdown-item {
    display: block;
    width: 100%;
    padding: 0.25rem 1.5rem;
    clear: both;
    font-weight: 400;
    color: #212529;
    text-align: inherit;
    white-space: nowrap;
    background-color: transparent;
    border: 0;
}
@media ( max-width:768px) {
  .d-sm-none{
    display: none;
    }
.pos-f-t.d-xl-none.d-sm-block.d-lg-none.d-md-none {
    background: #444;
}
ul.dropdown-menu.dropdown-menu-right.show {
    background: #aaa;
}
header#_bv_sub-dropdown_group_dd_header {
    color: #fff;
    font-size: 1.1rem;
}
header#_bv_dropdown_group_dd_header {
    color: #fff;
    font-size: 1.1rem;
}

}
</style>
