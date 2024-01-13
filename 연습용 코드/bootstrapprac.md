    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand" href="#">Navbar</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Link</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  Dropdown
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" href="#">Action</a></li>
                  <li><a class="dropdown-item" href="#">Another action</a></li>
                  <li><hr class="dropdown-divider"></li>
                  <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link disabled" aria-disabled="true">Disabled</a>
              </li>
            </ul>
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
          </div>
        </div>
    </nav>

    <h1>Hello, world!</h1>
    <button type="button" class="btn btn-info">Info</button>


    <div class="card shadow bg-body-tertiary rounded" style="width: 18rem;">
        <img src="IMG_3546.JPG" class="card-img-top" alt="...">
        <div class="card-body">
            <span class="badge rounded-pill text-bg-primary">News</span>
            <h5 class="card-title">Rainy Day</h5>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <div class="d-flex">
                <div class="flex-shrink-0">
                    <img src="IMG_3551.jpeg" alt="..." width="50px" style="border-radius: 50%;">
                </div>
                <div class="flex-grow-1 ms-3">
                    <span>Chloe Choi</span>
                    <p>September 13. 2023</p>
                </div>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="row">
            <div class="col-md-6 col-lg-3">
                <div class="card" style="width: 18rem;">
                    <img src="IMG_3546.JPG" class="card-img-top" alt="...">
                    <div class="card-body">
                        <span class="badge rounded-pill text-bg-primary">News</span>
                        <h5 class="card-title">Rainy Day</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="card" style="width: 18rem;">
                    <img src="IMG_3546.JPG" class="card-img-top" alt="...">
                    <div class="card-body">
                        <span class="badge rounded-pill text-bg-primary">News</span>
                        <h5 class="card-title">Rainy Day</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="card" style="width: 18rem;">
                    <img src="IMG_3546.JPG" class="card-img-top" alt="...">
                    <div class="card-body">
                        <span class="badge rounded-pill text-bg-primary">News</span>
                        <h5 class="card-title">Rainy Day</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="card" style="width: 18rem;">
                    <img src="IMG_3546.JPG" class="card-img-top" alt="...">
                    <div class="card-body">
                        <span class="badge rounded-pill text-bg-primary">News</span>
                        <h5 class="card-title">Rainy Day</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="row">
            <div class="col-2 col-md-2 order-md-2">
                <img src="IMG_3551.jpeg" alt="..." width="100%" style="border-radius: 50%;">
            </div>
            <div class="col-10 col-md-5 order-md-1 text-md-end">
                fubao so cute. <br> lg twins might win this year. <br> i love iced tea espresso added
            </div>
            <div class="col-md-5 order-md-3"></div>
        </div>
        <div class="row">
            <div class="col-2 col-md-2 order-md-2">
                <img src="IMG_3551.jpeg" alt="..." width="100%" style="border-radius: 50%;">
            </div>
            <div class="col-10 col-md-5 order-md-3">
                fubao so cute. <br> lg twins might win this year. <br> i love iced tea espresso added
            </div>
            <div class="col-md-5 order-md-1"></div>
        </div>
        <div class="row">
            <div class="col-2 col-md-2 order-md-2">
                <img src="IMG_3551.jpeg" alt="..." width="100%" style="border-radius: 50%;">
            </div>
            <div class="col-10 col-md-5 order-md-1 text-md-end">
                fubao so cute. <br> lg twins might win this year. <br> i love iced tea espresso added
            </div>
            <div class="col-md-5 order-md-3"></div>
        </div>
    </div>
    


<!-- div row는 내부를 12칸으로 쪼개주는 class, "col-3"이라고 하면 3칸을 차지하겠다는 뜻 -->
<!-- grid 시스템, col-md-6이건 조건식! xl-1200px, lg-992px, md-768px, sm-576px(모바일) -->
<!-- if pc size row3 & mb size row1 => col-lg-4 -->
<!-- order class는 순서 재배치를 하게 해줌.  -->
