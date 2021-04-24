<template>
 
    <div class="course-left">
        <div>
            <b-form-input size="sm" class="sm-2 search-box" placeholder="Search"></b-form-input>
        </div>
        <div class="introduction">
            <b-navbar-nav>
                <b-nav-item href="" >Getting started</b-nav-item>
                <b-nav-item href="" >Components</b-nav-item>
                <b-nav-item href="" >Icons</b-nav-item>
            </b-navbar-nav>
        </div>
    </div>
   
  
</template>

<script>
export default {
  
};
</script>

<style lang="scss">

    .course-left {
        padding: 15px;
        max-width: 16.666667%;
        height: 100%;
        .search-box {
            width: 80%;
        }
        .introduction {
            padding-top: 15px;
            a {
                color: rgba(0, 0, 0, 0.5);
            }
        }
    }
    

</style>
