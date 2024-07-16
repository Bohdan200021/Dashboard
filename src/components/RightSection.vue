<template>
    <div class="right">
        <div class="top">
            <button id="menu-btn">
                <span class="material-icons">menu</span>
            </button>
            <div class="theme-toggler">
                <span class="material-icons active">light_mode</span>
                <span class="material-icons">dark_mode</span>

            </div>
            <div class="profile">
                <div class="info">
                    <p>Hey, <b>Daniel</b></p>
                    <small class="text-muted">Admin</small>
                </div>
                <div class="profile-photo">
                    <img src="../images/profile-1.jpg" alt="">
                </div>
            </div>

        </div>
        <div class="recent-updates">
            <h2>Recent Updates</h2>
            <div class="updates">
                <div class="update">
                    <div class="profile-photo">
                        <img src="../images/profile-2.jpg" alt="">
                    </div>
                    <div class="message">
                        <p><b>Mike Tyson</b>received his order of Night lion tech GPS drone</p>
                        <small class="text-muted">2 Minutes Ago</small>
                    </div>
                </div>
                <div class="update">
                    <div class="profile-photo">
                        <img src="../images/profile-3.jpg" alt="">
                    </div>
                    <div class="message">
                        <p><b>Mike Tyson</b>received his order of Night lion tech GPS drone</p>
                        <small class="text-muted">2 Minutes Ago</small>
                    </div>
                </div>
                <div class="update">
                    <div class="profile-photo">
                        <img src="../images/profile-4.jpg" alt="">
                    </div>
                    <div class="message">
                        <p><b>Mike Tyson</b>received his order of Night lion tech GPS drone</p>
                        <small class="text-muted">2 Minutes Ago</small>
                    </div>
                </div>
            </div>
            
        </div>
        <div class="sales-analytics">
            <h2>Sales Analytics</h2>
            <div class="item online">
                <div class="icon">
                    <span class="material-icons">shopping_cart</span>
                </div>   
            
                <div class="right">
                    <div class="info">
                        <h3>ONLINE ORDERS</h3>
                        <small class="text-muted">Last 24 Hours</small>
                    </div>
                    <h5 class="success">+39%</h5>
                    <h3>3839</h3>
                </div>
            </div>
            <div class="item offline">
                <div class="icon">
                    <span class="material-icons">local_mall</span>
                </div>   
            
                <div class="right">
                    <div class="info">
                        <h3>OFFLINE ORDERS</h3>
                        <small class="text-muted">Last 24 Hours</small>
                    </div>
                    <h5 class="danger">-17%</h5>
                    <h3>1100</h3>
                </div>
            </div>
            <div class="item customers">
                <div class="icon">
                    <span class="material-icons">person</span>
                </div>   
            
                <div class="right">
                    <div class="info">
                        <h3>NEW CUSTOMERS</h3>
                        <small class="text-muted">Last 24 Hours</small>
                    </div>
                    <h5 class="success">+25%</h5>
                    <h3>849</h3>
                </div>
            </div>
            <div class="item add-product">
                <div>
                    <span class="material-icons">add</span>
                    <h3>Add Product</h3>
                </div>
            </div>
            
        </div>
    </div>
</template>
<script setup>
    
</script>
<style scoped>
.right {
    margin-top: 1.4rem;
}
.top {
    display: flex;
    justify-content: end;
    gap: 2rem;
}
.right .top button {
    display: none;
}
.right .theme-toggler {
    background: var(--color-light);
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 1.6rem;
    width: 4.2rem;
    cursor: pointer;
    border-radius: var(--border-radius-1);
}
.right .theme-toggler span {
    font-size: 1.2rem;
    width: 50%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;

}
.right .theme-toggler span.active {
    background: var(--color-primary);
    color: white;
    border-radius: var(--border-radius-1);
}
.right .top .profile {
    display: flex;
    gap: 2rem;
    text-align: right;
}
.recent-updates {
    margin-top: 1rem;
}
.recent-updates h2 {
    margin-bottom: 0.8rem;
}
.updates {
   background: var(--color-white);
   padding: var(--card-padding);
   border-radius: var(--card-border-radius);
   box-shadow: var(--box-shadow);
   transition: all 300ms ease;
}
.recent-updates:hover {
    box-shadow: none;
}
.update {
    display: grid;
    grid-template-columns: 2.6rem auto;
    gap: 1rem;
    margin-bottom: 1rem;

}

/* ======================================Analytics==================== */
.sales-analytics {
    margin-top: 2rem;
}
.sales-analytics h2 {
    margin-bottom: 0.8rem;
}
.sales-analytics .item {
    background: var(--color-white);
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 0.7rem;
    padding: 1.4rem var(--card-padding);
    border-radius: var(--border-radius-3);
    box-shadow: var(--box-shadow);
    transition: all 300ms ease;
}

.sales-analytics .item .right {
    display: flex;
    justify-content: space-between;
    align-items: start;
    margin: 0;
    width: 100%;
}
.icon {
    padding: 0.6rem;
    color: var(--color-white);
    border-radius: 50%;
    background: var(--color-primary);
    display: flex;
}
.right .sales-analytics .offline .icon {
    background: var(--color-danger);
}
.right .sales-analytics .customers .icon {
    background: var(--color-success);
}
.right .sales-analytics .add-product {
    background-color: transparent;
    border: 2px dashed var(--color-primary);
    color: var(--color-primary);
    display: flex;
    align-items: center;
    justify-content: center;
}
.right .sales-analytics .add-product:hover{
    background-color: var(--color-primary);
    color: white;
}
.right .sales-analytics .add-product div {
    display: flex;
    align-items: center;
    gap: 0.6rem;
}
.right .sales-analytics .add-product div h3 {
    font-weight: 600;
}
@media screen and (max-width: 768px){
  
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
    .right .profile .info {
      display: none;
    }
    .right .top button {
        display: inline-block;
        background: transparent;
        border: none;
        cursor: pointer;
        color: var(--color-dark);
        position: absolute;
        left: 1rem;
    }
    .right .top button span {
        font-size: 2rem;
    }
}
</style>