<style lang="sass">
@mixin cf {
  &:after {
      content: " ";
      display: block;
      clear: both;
  }
}


.nav-wrap {
  @include container();
  position: relative;
  background: white;

  i{
      margin-top: 1.563rem;

      &:hover{
          cursor: pointer;
      }


  }

}

.navbar {

  border-top: 8px solid $maroon;

  @include cf;
  position: fixed;
  width: 100%;
  top: 0;
  background: white;
  z-index: 3;
  -webkit-box-shadow: 0 4px 4px -3px #000000;
  -moz-box-shadow: 0 4px 4px -3px #000000;
  box-shadow: 0 2px 5px 0 rgba(0,0,0,0.26);



  .logo {

      @include span(4);
      text-align: center;

      margin-top: 1%;



      @media(max-width:$md){

          margin-top: 1%;
          @include span(6);
      }
      @media(max-width:$sm){
          margin-top: 3%;
      }

  }

  .nav-links {
      @include span(last 5);
      @include cf;
      min-height: 100%;
      text-align: center;
      @media(max-width: 1512px) {
          @include span(8 last);
      }
      @media(max-width: $md) {
          display: none;
      }
      li {
          margin-left: (span(1 of 12) + gutter());
          letter-spacing: 0.125rem;
          .bold {
              font-weight: bold;
              color: $maroon;
          }
          a {
              font-family: 'Lato', serif;
              color: $maroon;
              font-weight: 300;
              line-height: 5.063rem;
              font-size: 1.2rem;


          }
      }
  }
}



//_______________MOBILE NAVIGATION STYLES________________//


.mobile-nav-btn {
  display: none;

  @media(max-width: $md) {
      display: inline-block;
      @include span(last 3);


      a {
          color: $maroon;
          line-height: 4.063rem;

          @media(max-width:$md){
              line-height: 5rem;
          }

          &:hover {
              cursor: pointer;
          }

      }
  }
}


.mobile-menu{
  width: 100%;
  height: inherit;
  background: white;
  transition: all 0.3s;

  li{
      display: block;
      width: 100%;

      &:hover{
          background: #E8E2DD;
      }
      text-align: center;

      a{
          color: $maroon;
          display: block;
          width: 100%;

      }
  }
}


.hidemenu {
  position: absolute;
  top: 0;
  z-index: -1;
  visibility: hidden;

}


.showmenu{
  position: absolute;
  top: 100%;

}





</style>
