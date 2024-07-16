<template>
    <main>
        <h1>Dashboard</h1>
        <div class="date">
            <input type="date">
        </div>
        <div class="insights">
            <div class="sales">
                <span class="material-icons">analytics</span>
                <div class="middle">
                    <div class="left">
                        <h3>Total Sales</h3>
                        <h1>$25,024</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx='38' cy='38' r='36'></circle>
                        </svg>
                        <div class="number">
                            <p>81%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
            <div class="expenses">
                <span class="material-icons">bar_chart</span>
                <div class="middle">
                    <div class="left">
                        <h3>Total Expenses</h3>
                        <h1>$14,160</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx='38' cy='38' r='36'></circle>
                        </svg>
                        <div class="number">
                            <p>62%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
            <div class="income">
                <span class="material-icons">stacked_line_chart</span>
                <div class="middle">
                    <div class="left">
                        <h3>Total Income</h3>
                        <h1>$10,864</h1>
                    </div>
                    <div class="progress">
                        <svg>
                            <circle cx='38' cy='38' r='36'></circle>
                        </svg>
                        <div class="number">
                            <p>44%</p>
                        </div>
                    </div>
                </div>
                <small class="text-muted">Last 24 Hours</small>
            </div>
        </div>
        <div class="recent-orders">
            <h2>Resent Orders</h2>
            <table>
                <thead>
                    <tr>
                        <th>Product Name</th>
                        <th>Product Number</th>
                        <th>Payment</th>
                        <th>Status</th>
                        <th></th>

                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>
                    <tr>
                        <td>Foldabel Mini Drone</td>
                        <td>85631</td>
                        <td>Due</td>
                        <td class="warning">Pending</td>
                        <td class="primary">Details</td>
                    </tr>

                </tbody>
            </table>
            <a href="#">Show All</a>
        </div>
    </main>
</template>
<script>

</script>
<style scoped>
main {
    margin-top: 1.4rem;
}
main .date {
    display: inline-block;
    background: var(--color-light);
    border-radius: var(--border-radius-1);
    margin-top: 1rem;
    padding: 0.5rem 1.6rem;
}
main .date > input[type='date'] {
    background: transparent;
    color: var(--color-dark);
}
main .insights {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.6rem;
}
main .insights > div {
    background: var(--color-white);
    padding: var(--card-padding);
    border-radius: var(--card-border-radius);
    margin-top: 1rem;
    box-shadow: var(--bax-shadow);
    transition: all 300ms ease;
}
.insights > div:hover {
    box-shadow: none;
}
.insights > div span {
    background: var(--color-primary);
    padding: 0.5rem;
    border-radius: 50%;
    color: var(--color-white);
    font-size: 2rem;
}
.insights > div.expenses span{
    background: var(--color-danger);
}
.insights > div.income span{
    background: var(--color-success);   
}
.insights > div .middle {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.insights h3 {
    margin: 1rem 0 0.6rem;
    font-size: 1rem;
}
main .insights .progress {
    position: relative;
    width: 92px;
    height: 92px;
    border-radius: 50%;
}
main .insights svg {
    width: 7rem;
    height: 7rem;
}
main .insights svg circle {
    fill: none;
    stroke: var(--color-primary);
    stroke-width: 14;
    stroke-linecap: round;
    transform: translate(5px, 5px);
    stroke-dasharray: 110;
    stroke-dashoffset: 92;

}
main .insights .sales svg circle {
    stroke-dashoffset: -30;
    stroke-dasharray: 200;
}
main .insights .expenses svg circle {
    stroke-dashoffset: 20;
    stroke-dasharray: 80;
}
main .insights .income svg circle {
    stroke-dashoffset: 35;
    stroke-dasharray: 110;
}
main .insights .progress .number {
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
main.insights small {
    margin-top: 1.3rem;
    display: block;
}
/* ==================================RECENT ORDERS========================== */
.recent-orders {
    margin-top: 2rem;
}
.recent-orders h2 {
    margin-bottom: 0.8rem;
}
.recent-orders table {
    background: var(--color-white);
    width: 100%;
    border-radius: var(--card-border-radius);
    padding: var(--card-padding);
    text-align: center;
    box-shadow: var(--bax-shadow);
    transition: all 300ms ease;
}
.recent-orders table:hover {
    box-shadow: none;
}
tbody td {
    height: 2.8rem;
    border-bottom: 1px solid var(--color-light);
    color: var(--color-dark-variant);
}
tbody tr:last-child td{
    border: none;
}
.recent-orders a {
    text-align: center;
    display: block;
    margin: 1rem auto;
    color: var(--color-primary);

}
@media screen and (max-width: 1200px){
    main .insights {
      grid-template-columns: 1fr;
      gap: 0;
    }
    main .recent-orders {
       width: 94%; 
       position: absolute;
       left: 50%;
       transform: translateX(-50%);
       margin: 2rem 0 0 8.8rem;
    }
    .main .recent-orders table {
        width: 83vw;
    }
    main table tbody tr td:last-child,  
    main table tbody tr td:first-child   {
        display: none;
    }
    
}
@media screen and (max-width: 768px){

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
}

</style>