<?php
include('system/header.php');
$hosting = $connect->query("SELECT * FROM `Hostings` WHERE `status` IN(0,1) AND `username` = '".$getUser['username']."'")->num_rows;
$dichVu = $hosting;
echo Title('Trang Chủ - '.$system32['title']);
?>
    
<!--start main wrapper-->
<main class="main-wrapper">
  <div class="main-content">
    <!--breadcrumb-->
    <div class="page-breadcrumb d-none d-sm-flex align-items-center mb-3">
      <div class="breadcrumb-title pe-3">Thống Kê</div>
      <div class="ps-3">
        <nav aria-label="breadcrumb">
          <ol class="breadcrumb mb-0 p-0">
            <li class="breadcrumb-item"><a href="javascript:;"><i class="bx bx-home-alt"></i></a></li>
            <li class="breadcrumb-item active" aria-current="page">Trang Chủ</li>
          </ol>
        </nav>
      </div>
      <div class="ms-auto">
        <div class="btn-group">
          <button type="button" class="btn btn-outline-primary">Settings</button>
          <button type="button" class="btn btn-outline-primary split-bg-primary dropdown-toggle dropdown-toggle-split" data-bs-toggle="dropdown">
            <span class="visually-hidden">Toggle Dropdown</span>
          </button>
          <div class="dropdown-menu dropdown-menu-right dropdown-menu-lg-end">
            <a class="dropdown-item" href="//fb.com/HuyMasterDesign"> Facebook Admin</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="//zalo.me/0776550825">Zalo Admin</a>
          </div>
        </div>
      </div>
    </div>
    <!--end breadcrumb-->

    <div class="row">
      <div class="col-12 d-flex align-items-stretch">
        <div class="card w-100 overflow-hidden rounded-4">
          <div class="card-body position-relative p-4">
            <div class="row">
              <div class="col-12 col-sm-7">
                <div class="d-flex align-items-center gap-3 mb-5">
                    <?php if(isset($_SESSION['users'])){ ?>  
                  <img src="<?=AntiXss($system32['avataruser']);?>" class="rounded-circle bg-grd-info p-1" width="60" height="60" alt="Ảnh Avatar">
                  <div class="">
                    <p class="mb-0 fw-semibold">Chào Mừng</p>
                    <h4 class="fw-semibold mb-0 fs-4 mb-0"> <?=ReturnXss($getUser['name']);?>!</h4>
                  </div>
                </div>
                <div class="d-flex align-items-center gap-5">
                  <div class="">
                    <h4 class="mb-1 fw-semibold d-flex align-content-center"><?=Monney($hosting);?><i class="ti ti-arrow-up-right fs-5 lh-base text-success"></i></h4>
                    <p class="mb-3">Hosting Hoạt Động</p>
                    <div class="progress mb-0" style="height:5px;">
                      <div class="progress-bar bg-grd-success" role="progressbar" style="width: 100%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                  </div>
                  <div class="vr"></div>
                  <div class="">
                    <h4 class="mb-1 fw-semibold d-flex align-content-center"><?=level($getUser['level']);?><i class="ti ti-arrow-up-right fs-5 lh-base text-success"></i></h4>
                    <p class="mb-3">Cấp Bậc</p>
                    <div class="progress mb-0" style="height:5px;">
                      <div class="progress-bar bg-grd-danger" role="progressbar" style="width: 100%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-12 col-sm-5">
                <div class="welcome-back-img pt-4">
                  <img src="assets/images/gallery/welcome-back-3.png" height="180" alt="">
                </div>
              </div>
            </div><!--end row-->
          </div>
        </div>
      </div>
    </div><!-- end row -->
    
    
    <?php } else { ?>
    <img src="<?=AntiXss($system32['avataruser']);?>" class="rounded-circle bg-grd-info p-1" width="60" height="60" alt="Ảnh Avatar">
                  <div class="">
                    <p class="mb-0 fw-semibold">Khách Hàng</p>
                    <h4 class="fw-semibold mb-0 fs-4 mb-0"> Vui Lòng Đăng Nhập!</h4>
                  </div>
                </div>
                <div class="d-flex align-items-center gap-5">
                  <div class="">
                    <h4 class="mb-1 fw-semibold d-flex align-content-center"><?=Monney($hosting);?><i class="ti ti-arrow-up-right fs-5 lh-base text-success"></i></h4>
                    <p class="mb-3">Hosting Hoạt Động</p>
                    <div class="progress mb-0" style="height:5px;">
                      <div class="progress-bar bg-grd-success" role="progressbar" style="width: 100%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                  </div>
                  <div class="vr"></div>
                  <div class="">
                    <h4 class="mb-1 fw-semibold d-flex align-content-center">Chưa Load...<i class="ti ti-arrow-up-right fs-5 lh-base text-success"></i></h4>
                    <p class="mb-3">Cấp Bậc</p>
                    <div class="progress mb-0" style="height:5px;">
                      <div class="progress-bar bg-grd-danger" role="progressbar" style="width: 100%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-12 col-sm-5">
                <div class="welcome-back-img pt-4">
                  <img src="assets/images/gallery/welcome-back-3.png" height="180" alt="">
                </div>
              </div>
            </div><!--end row-->
          </div>
        </div>
      </div>
    </div><!-- end row -->
     <?php } ?>

    <div class="row">
      <div class="col-12 col-lg-3 col-xxl-2 d-flex">
        <div class="card rounded-4 w-100">
          <div class="card-body">
            <div class="mb-3 d-flex align-items-center justify-content-between">
              <div class="wh-42 d-flex align-items-center justify-content-center rounded-circle bg-primary bg-opacity-10 text-primary">
                <span class="material-icons-outlined fs-5">shopping_cart</span>
              </div>
            </div>
            <div>
              <h4 class="mb-0"><?=Monney($hosting);?></h4>
              <p class="mb-3">Hosting</p>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-3 col-xxl-2 d-flex">
        <div class="card rounded-4 w-100">
          <div class="card-body">
            <div class="mb-3 d-flex align-items-center justify-content-between">
              <div class="wh-42 d-flex align-items-center justify-content-center rounded-circle bg-success bg-opacity-10 text-success">
                <span class="material-icons-outlined fs-5">attach_money</span>
              </div>
            </div>
            <div>
              <h4 class="mb-0"><?=Monney($getUser['monney']);?> <sup>đ</sup></h4>
              <p class="mb-3">Số Dư </p>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-3 col-xxl-2 d-flex">
        <div class="card rounded-4 w-100">
          <div class="card-body">
            <div class="mb-3 d-flex align-items-center justify-content-between">
              <div class="wh-42 d-flex align-items-center justify-content-center rounded-circle bg-info bg-opacity-10 text-info">
                <span class="material-icons-outlined fs-5">visibility</span>
              </div>
            </div>
            <div>
              <h4 class="mb-0"><?=Monney($getUser['monneydatieu']);?> <sup>đ</sup></h4>
              <p class="mb-3">Tiền Đã Sử Dụng</p>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-3 col-xxl-2 d-flex">
        <div class="card rounded-4 w-100">
          <div class="card-body">
            <div class="mb-3 d-flex align-items-center justify-content-between">
              <div class="wh-42 d-flex align-items-center justify-content-center rounded-circle bg-warning bg-opacity-10 text-warning">
                <span class="material-icons-outlined fs-5">leaderboard</span>
              </div>
            </div>
            <div>
              <h4 class="mb-0"><?=Monney($getUser['monneydanap']);?> <sup>đ</sup></h4>
              <p class="mb-3">Tiền Đã Nạp</p>
            </div>
          </div>
        </div>
      </div>
    </div><!--end row-->

  </div><!--end main-content-->
</main><!--end main wrapper-->

<!--start overlay-->
<div class="overlay btn-toggle"></div>
<!--end overlay-->

<?php
include('system/footer.php');
?>
