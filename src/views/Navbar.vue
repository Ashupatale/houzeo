<template>
    <div class="Navbar">
  <div >
    <nav class="navbar navbar-expand-lg row mb-2 container mx-auto">
      <div class="container-fluid first-nav">
        <a class="navbar-brand" href="#">
          <img src="@/assets/Logo.svg"/>
        </a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item dropdown nav-class">
              <a
                class="nav-link active dropdown-toggle"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
                aria-current="page"
              >
                Product
              </a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action......</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><hr class="dropdown-divider" /></li>
                <li>
                  <a class="dropdown-item" href="#">Something else here</a>
                </li>
              </ul>
            </li>
            <li class="nav-item nav-class">
              <a class="nav-link active" href="#">How Houzeo Works</a>
            </li>
            <li class="nav-item nav-class">
              <a class="nav-link active" href="#">Reviews</a>
            </li>
            <li class="nav-item nav-class dropdown">
              <a
                class="nav-link dropdown-toggle active"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
                aria-current="page"
              >
                Buy
              </a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action......</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
              </ul>
            </li>
            <li class="nav-item nav-class dropdown">
              <a
                class="nav-link dropdown-toggle active"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
                aria-current="page"
              >
                Sell
              </a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action......</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
              </ul>
            </li>
            <li class="nav-item nav-class">
              <a class="nav-link active" href="#">Pricing</a>
            </li>
            <li class="nav-item nav-class dropdown">
              <a
                class="nav-link dropdown-toggle active"
                href="#"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
                aria-current="page"
              >
                Resources
              </a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Action......</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
              </ul>
            </li>
            <li class="nav-item nav-class">
              <a class="nav-link active" href="#">Sign In</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" href="#" style="">
                <span>(844) 448-0110 </span>
                <br />
                <span>(9am to 6pm CST, Mon-Sat)</span></a
              >
            </li>
          </ul>
          <button class="form-btn" type="submit">Start Free Listing</button>
        </div>
      </div>
    </nav>

  
  </div>

  <div class="second-nav container">
      <div class="row">
        <span class="fw-bold">2856 Meadow Park Ave,</span>
        <p>Henderson, NV 89052</p>
      </div>
      <div class="row">
        <span class="fw-bold">$500,000</span>
        <p class="d-flex">
          <span style="margin-right: 8px">Est. $4,284/mo</span>
          <span style="color: #0b5aa5" class="fw-bold">$Get Pre-Approved</span>
        </p>
      </div>
      <div class="d-flex justify-content-between">
        <div>
          <span style="margin-right: 8px">4</span>
          <p>Beds</p>
        </div>
        <div>
          <span style="margin-right: 8px">3</span>
          <p>Bath</p>
        </div>
        <div>
          <span style="margin-right: 8px">998</span>
          <p>sqft</p>
        </div>
      </div>
      <div class="offerBtn-div">
        <button class="offer-btn" type="submit">Make an offer</button>
      </div>
    </div>
</div>
</template>

<script>
export default {
  name: "navbar-page",
};
</script>

<style>
.nav-class {
  margin-top: 10px;
}
.Navbar {
  box-shadow: 0px 3px 5px #4e4e4e26;
}
.navbar-brand img{
  width:100px;
  height:34px;
}
.form-btn {
  background: transparent linear-gradient(270deg, #0e5293 0%, #2876c1 100%) 0%
    0% no-repeat padding-box;
  border-radius: 8px;
  font-size: 14px;
  opacity: 1;
  outline: none;
  border: none;
  padding: 5px 10px;
  color: white;
  width: 146px;
  height: 38px;
}
.navbar-brand {
  margin-right: 50px;
}
.nav-link {
  font-size: 14px;
  font-weight: regular;
}
.offer-btn {
  background-color: #f05d29;
  border-radius: 8px;
  opacity: 1;
  outline: none;
  border: none;
  padding: 5px 10px;
  color: white;
  width: 162px;
  height: 50px;
}

.offerBtn-div {
  text-align: right;
}
.second-nav {
  display: grid;
  grid-template-columns: 2fr 2fr 1fr 1fr;
}
@media (min-width: 360px) and (max-width: 992px) {
  .form-btn {
    width: 176px;
    height: 50px;
  }
  .second-nav {
    display: none;
  }
}
@media (max-width: 991px) {
  .nav-link {
    text-align: center;
  }
  .form-btn {
    text-align: center;
    justify-content: center;
  }
}
@media (min-width: 992px) and (max-width: 1219px) {
  .nav-link {
    font-size: 10px;
  }
  .form-btn {
    font-size: 12px;
  }
}

@media (min-width: 1000px) {
  .nav-link {
    text-align: left;
  }
}
</style>
