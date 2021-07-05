<template>
    <div>
        <b-navbar toggleable="sm" type="dark" style="background-color: #563d7c;">
            <b-navbar-toggle target="nav-collapse" class="mr-auto"></b-navbar-toggle>
            <b-navbar-brand href="/">
                
                Home
            </b-navbar-brand>
            
            
            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item href="/findshop">お店を探す</b-nav-item>
                    <!-- <b-nav-item-dropdown text="お店を探す" right>
                        <b-dropdown-item href="#">EN</b-dropdown-item>
                        <b-dropdown-item href="#">ES</b-dropdown-item>
                        <b-dropdown-item href="#">RU</b-dropdown-item>
                        <b-dropdown-item href="#">FA</b-dropdown-item> -->
                    <!-- </b-nav-item-dropdown> -->
                    <b-nav-item href="/comunity">コミュニティ</b-nav-item>
                </b-navbar-nav>
                <!-- <b-navbar-nav class="ml-auto mr-auto">
                    <b-nav-form >
                        <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
                        <b-button size="sm" variant="outline-primary" class="my-2 my-sm-0" type="submit">Search</b-button>
                    </b-nav-form>
                </b-navbar-nav> -->
            </b-collapse>
            <b-navbar-brand href="/" class="ml-auto">
                <img src="https://placekitten.com/g/30/30" class="d-inline-block align-top " style="border-radius: 50% ">
            </b-navbar-brand>
        </b-navbar>
    </div>
</template>