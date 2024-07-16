

<template>
    <aside id="aside-block">
        <div class="top">
            <div class="logo">
            <img src=".././images/logo.png" alt="">
            <h2>EGA<span class="danger">TOP</span></h2> 
            </div>
            <div class="close" id="close-btn">
            <span class="material-icons">
                close
            </span>
            </div>
        </div>
        <div class="sidebar">
            <a href="">
            <span class="material-icons">grid_view</span>
            <h3>Dashboard</h3>
            </a>
            <a href="" class="active">
            <span class="material-icons">person</span>
            <h3>Customers</h3>
            </a>
            <a href="">
            <span class="material-icons">receipt_long</span>
            <h3>Orders</h3>
            </a>
            <a href="">
            <span class="material-icons">insights</span>
            <h3>Analytics</h3>
            </a>
            <a href="">
            <span class="material-icons">mail_outline</span>
            <h3>Massages</h3>
            <span class="message-count">26</span>
            </a>
            <a href="">
            <span class="material-icons">inventory</span>
            <h3>Products</h3>
            </a>
            <a href="">
            <span class="material-icons">report_gmailerrorred</span>
            <h3>Reports</h3>
            </a>
            <a href="">
            <span class="material-icons">settings</span>
            <h3>Settings</h3>
            </a>
            <a href="">
            <span class="material-icons">add</span>
            <h3>Add Products</h3>
            </a>
            <a href="">
            <span class="material-icons">logout</span>
            <h3>Logout</h3>
            </a>
        </div>
    </aside>

</template>

<style scoped>
aside {
  height: 100vh;

}
.top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 1.4rem;
}
.logo {
  display: flex;
  gap: 0.8rem;
}


.logo img {
  width: 2rem;
  height: 2rem;
}

.close {
  display: none;
}
/* =======================================Sidebar============================ */
.sidebar {
  display: flex;
  flex-direction: column;
  height: 86vh;
  position: relative;
  top: 3rem;
}
aside h3 {
  font-weight: 500;
}
.sidebar a {
  display: flex;
  color: var(--color-info-dark);
  margin-left: 2rem;
  gap: 1rem;
  align-items: center;
  position: relative;
  height: 3.7rem;
  transition: all 300ms ease;
}

.sidebar a span {
  font-size: 1.6rem;
  transition: all 300ms ease;
}
.sidebar a:last-child{
  position: absolute;
  bottom: 2rem;
  width: 100%;
}
.sidebar a.active {
  background: var(--color-light);
  color: var(--color-primary);
  margin-left: 0;
}
.sidebar a.active:before {
  content: '';
  width: 6px;
  height: 100%;
  background: var(--color-primary);
}
.sidebar a.active span {
  color: var(--color-primary);
  margin-left: calc(1rem - 3px);
}
.sidebar a:hover {
  color: var(--color-primary);
  
}
.sidebar a:hover span {
  margin-left: 1rem;
}
.sidebar .message-count {
  background: var(--color-danger);
  color: var(--color-white);
  padding: 2px 10px;
  font-size: 11px;
  border-radius: var(--border-radius-1);
}
@media screen and (max-width: 1200px){
    .logo h2{
        display: none;
    }
    .sidebar h3 {
      display: none;

    }
    .sidebar a {
      width: 5.6rem;

    }
    .sidebar a:last-child {
      position: relative;
      margin-top: 1.8rem;
    }
    
}
@media screen and (max-width: 768px){
    aside {
        position: fixed;
        left: -100%;
        background: var(--color-white);
        width: 18rem;
        z-index: 3;
        box-shadow: 1rem 3rem 4rem var(--color-light);
        height: 100vh;
        padding-right: var(--card-padding);
        display: none;
        animation: showMenu 400ms ease forwards;
    }
    @keyframes showMenu {
      to {
        left: 0;
      }
    }
    aside .logo {
      margin-left: 1rem;
    }
    aside .logo h2 {
      display: inline;
    }
    aside .sidebar h3 {
      display: inline;
    }
    aside .sidebar a {
      width: 100%;
      height: 3.4rem;
    }
    aside .sidebar a:last-child {
      position: absolute;
      bottom: 5rem;
    }
    .close {
      display: inline-block;
      cursor: pointer;
    }
    main {
      margin-top: 8rem;
      padding: 0 1rem;
    }
    main .recent-orders {
      position: relative;
      margin: 3rem 0 0 0 ;
      width: 100%;
    }
    main .recent-orders table {
      width: 100%;
      margin: 0;
    }
    .right {
      width: 94%;
      margin: 0 auto 4rem;
    }
    .right .top {
      position: fixed;
      top: 0;
      left: 0;
      align-items: center;
      padding: 0 0.8rem;
      height: 4.6rem;
      background: var(--color-white);
      width: 100%;
      margin: 0;
      z-index: 2;
      box-shadow: 0 1rem var(--color-light);
    }
    .right .top .theme-toggler {
      width: 4.4rem;
      position: absolute;
      left: 66%;
    }
    .info {
      display: none;
    }
}
</style>
<script setup>



</script>