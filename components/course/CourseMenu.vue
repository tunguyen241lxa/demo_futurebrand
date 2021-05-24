<template>
  <div class="course-left">
    <div>
      <b-form-input
        size="sm"
        placeholder="Tìm"
        type="text"
        title="Type in a name"
      ></b-form-input>
    </div>
    <div class="introduction">
      <ul class="left-menu">
        <!-- An element that will wrap our component -->
        <li class="dropDownMenuWrapper">
          <!-- <ul class="dropDownMenuWrapper menu-lv1"> -->
          <!-- A button that will actually open & close our menu -->
          <a><button
            class="dropDownMenuButton text-color"
            ref="menu"
            @click="openClose"
          >
            {{ menuDropDrown }}
             <div class="iconWrapper">
              <svg
              data-v-cca980e4
                class="bar1"
                :class="{ 'bar1--open': isOpen }"
                xmlns="http://www.w3.org/2000/svg"
                width="40"
                height="40"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"  
              >
                <polyline data-v-cca980e4="" points="9 18 15 12 9 6"></polyline>
              </svg>
          </div>
          </button></a>
          <!-- Pure CSS icon that indicates if the menu is open or closed -->
         
          <!-- An element that will wrap the actual menu content —links and such. -->
          <ul
            class="dropdownMenu text-color"
            menu-title="Start"
            v-if="isOpen"
          >
            <!-- Just a for pointing purposes  -->
            <!-- <div class="menuArrow" /> -->

            <li
              class="option menu-lv2"
              v-for="(data, key) in itemList"
              :key="key"
              :class="{ 'active' : isActive == data.product}" 
              @click="openCourse(data.product)"
              prefetchPayloads
            >
              <NuxtLink :to="data.link">{{ data.product }}</NuxtLink>
            </li>

          </ul>
        </li>
        <!-- <div class="list" :class="{ 'list--open': isOpen }"></div> -->
        <li class="menu-lv1" 
            :class="{ 'active' : isActive == 'concepts'}" 
            @click="openCourse('concepts')">
          <NuxtLink to="/course/concepts">{{menuSingle1}}</NuxtLink>
        </li>

        <li class="menu-lv1"
            :class="{ 'active' : isActive == 'features'}" 
            @click="openCourse('features')"
          >
          <NuxtLink to="/course/features">{{menuSingle2}}</NuxtLink>
        </li>
      </ul>
    </div>

    <!-- <div class="course-right"></div> -->
  </div>
</template>

<script>
export default {
 
  // props: [ "menuTitle" ], // Menu title from the parent
  data() {
    return {
      isOpen: false, // Variable if the menu is open or closed,

      search: "",
      menuDropDrown: "Bắt đầu",
      menuSingle1: "Chủ đề",
      menuSingle2: "Nổi Bật",
      itemList: [],
      isActive: ''
    };
  },
  mounted() {
    // Tips: data form server
    // Simulate the server response using a timer
    setTimeout(() => {
      const data = {
        "0": {
          ID: "Bắt đầu",
          product: "Hello1",
          link: "/course"
        },
        "1": {
          ID: "Bắt đầu",
          product: "Hello2",
          link: "/course"
        },
        "2": {
          ID: "Bắt đầu",
          product: "Hello3",
          link: "/course"
        }
      };

      // it's works
      // By 'mv' modules
      this.itemList = data;
    }, 1000);
  },
  computed: {
    filteredList() {
      return this.postList.filter(post => {
        return post.title.toLowerCase().includes(this.search.toLowerCase());
      });
    }
  },
  methods: {
    openClose() {
      // Toggle between open or closed ( true || false )
      this.isOpen = !this.isOpen;
    },
    openCourse(item) {
      this.isActive = item;
    }
    //@keyup="myFunction()
    // myFunction() {
    //   var input, filter, ul, li, a, i, txtValue;
    //   input = document.getElementById("myInput");
    //   filter = input.value.toUpperCase();

    //   menuLv1 = document.getElementByClassName("menu-lv1");
    //   for (let i = 0; i < menuLv1.length; i++) {
    //     if (menuLv1[i].textContent != filter) {
    //       let childs = menuLv1.childNodes.length;
    //       if (childs == 0) {
    //         menuLv1[i].style.display = "none";
    //       }
    //     } else {
    //       menuLv1[i].style.display = "block";
    //     }
    //   }
    // }
  }
};
</script>

<style lang="scss">
.course-left {
  padding: 15px;
    padding-left: 55px;
    padding-top: 2rem;
    max-width: 25%;
    width: 30%;
    height: 100%;
 
.form-control-sm {
  width: 80%;
}
  .search-box {
    width: 80%;
  }

  .introduction {
    padding-top: 15px;
    .left-menu {
      list-style: none;
      padding: 3px;
    }
    a {
      color: rgba(0, 0, 0, 0.5);
    }

    .list {
      height: 0px;
    }

    .list--open {
      height: 120px;
    }
    .active a {
      color: #71e271;
    }
    .menu-lv1 {
      height: 40px;
      display: flex;
      align-items: center;
      text-decoration: none;
      a {
        text-decoration: none;
        &:hover {
          color: #71e271;
        }
      }
    }
    
    // dropmenu demo
    .dropDownMenuWrapper {
     
      button:hover {
        color: #71e271;
        .iconWrapper svg {
          // color: #71e271;
          filter: #71e271;
          // filter: invert(27%) sepia(51%) saturate(2878%) hue-rotate(346deg) brightness(104%) contrast(97%);
        }
      }
      .active {
        color: #71e271;
      }
      .menu-lv2 {
        display: flex;
        padding: auto;
        align-items: center;
        a {
          text-decoration: none;
          &:hover {
            color: #71e271;
          }
        }
      }
      position: relative;
      // width: 500px;
      height: auto;
      border-radius: 8px;
      background: white;
      // border: 1px solid #eee;
      // box-shadow: 10px 10px 0 0 rgba(black,.03);
      -webkit-tap-highlight-color: rgba(0, 0, 0, 0);

      * {
        box-sizing: border-box;
        text-align: left;
      }

      .text-color {
        color: rgba(0, 0, 0, 0.5);
        list-style: none;
        padding: 0px;
      }

      .dropDownMenuButton {
        padding: 0px;
        border: none;
        font-size: inherit;
        background: none;
        outline: none;
        border-radius: 4px;
        // position: absolute;
        top: 0;
        left: 0;
        display: flex;
        align-items: center;
        // padding: 0 70px 0 20px;
        margin: 0;
        line-height: 1;
        width: 100%;
        height: 40px;
        z-index: 2;
        cursor: pointer;
      }

      .dropDownMenuButton--dark {
        color: #eee;
      }

      .iconWrapper {
        width: 25px;
        height: 25px;
        position: absolute;
        right: 30px;
        top: 35px;
        transform: translate(0, -50%);
        z-index: 1;

        .bar1 {
          width: 100%;
          left: 50%;
          border-radius: 9999px;
          transform: translate(-50%, calc(-50% - 0px));
          transition: all 0.2s ease;
        }

        .bar1--dark {
          background: #eee;
        }

        .bar1--open {
          transform: translate(-50%, -50%) rotate(90deg);
          margin-top: 0;
          
        }
      }

      .iconWrapper--noTitle {
        left: 0;
        top: 0;
        bottom: 0;
        right: 0;
        width: auto;
        height: auto;
        transform: none;
      }

      .dropdownMenu {
        // height:100px;
        // position: absolute;
        top: 60%;
        width: 100%;
        // min-width: 300px;
        min-height: 10px;
        border-radius: 8px;
        // border: 1px solid #eee;
        // box-shadow: 10px 10px 0 0 rgba(black,.03);
        background: white;
        // padding: 10px 30px;
        // animation: menu 0.3s ease forwards;
        
        .menuArrow {
          width: 20px;
          height: 20px;
          position: absolute;
          top: -10px;
          left: 20px;
          border-left: 1px solid #eee;
          border-top: 1px solid #eee;
          background: white;
          transform: rotate(45deg);
          border-radius: 4px 0 0 0;
        }

        .menuArrow--dark {
          background: #333;
          border: none;
        }

        .option {
          width: 100%;
          height: 40px;
          // border-bottom: 1px solid #eee;
          // padding: 20px 0;
          cursor: pointer;
          position: relative;
          z-index: 2;

          &:last-child {
            border-bottom: 0;
          }

          * {
            color: inherit;
            text-decoration: none;
            background: none;
            border: 0;
            padding: 0;
            outline: none;
            cursor: pointer;
          }
        }

        .desc {
          opacity: 0.5;
          display: block;
          width: 100%;
          font-size: 14px;
          margin: 3px 0 0 0;
          cursor: default;
        }
      }

      .dropdownMenu--dark {
        background: #333;
        border: none;

        .option {
          border-bottom: 1px solid #888;
        }

        * {
          color: #eee;
        }
      }

      @keyframes menu {
        from {
          transform: translate3d(0, 30px, 0);
        }

        to {
          transform: translate3d(0, 20px, 0);
        }
      }
    }

    .dropDownMenuWrapper--noTitle {
      padding: 0;
      width: 60px;
      height: 60px;
    }

    .dropDownMenuWrapper--dark {
      background: #333;
      border: none;
    }
  }
}
</style>
