
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WBMDTCL e-Challan: DashBoard</title>
    <link rel="stylesheet" href="dashboard_style.css">
    <link href='https://unpkg.com/boxicons@2.1.1/css/boxicons.min.css' rel='stylesheet'>
</head>
<body>

    <!DOCTYPE html>
<html lang="en">
<head>

<style>

.Panel_View{
    width: 100%;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
}
.MenuData{
    margin-top: 3em;
}

.Panel_View .top_bar{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 50px;
    padding: 8px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #283747;
    -webkit-box-shadow: 0 8px 6px -6px rgba(0,0,0,0.06);
	-moz-box-shadow: 0 8px 6px -6px rgba(0,0,0,0.06);
	box-shadow: 0 8px 6px -6px rgba(0,0,0,0.06);

}

.Panel_View .top_bar h2#logo{
    font-weight: 2em;
    font-size: 18px;
    color: rgba(255,255,255,0.9);
    display: flex;
    align-items: center;
    justify-content: center;
}

.Panel_View .top_bar h2#logo i{
    margin-right: 5px;
}

.Panel_View .menu_control_box{
    display: flex;
    align-items: center;
}
.Panel_View .top_bar .total_challans_tv,.Panel_View .menu_control_box #menu_btn{
    padding: 8px 13px;
    border-radius: 5px;
    border: none;
    outline: none;
    display: flex;
    align-items: center;
    justify-content: center;
}
.Panel_View .top_bar .total_challans_tv{
    color: rgba(255,255,255,0.8);
    background: #76448A;
    font-size: 14px;
}

.Panel_View .top_bar .total_challans_tv i{
    font-size: 1.2em;
    margin-right: 10px;
}

.Panel_View .menu_control_box #menu_btn{
    height: 40px;
    width: 40px;
    border-radius: 50%;
    font-size: 1.3em;
    background: none;
    cursor: pointer;
    color: #fff;
    margin-right: 10px;
}
.Panel_View .menu_control_box #menu_btn:hover{
    background: rgba(255,255,255,0.2);
}

.SideBar{
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 250px;
    padding: 10px;
    background: #283747;
    z-index: 1000;
    transition: 0.5s;
    transform: translateX(-300px);
    box-shadow: 0.1px 4px 8px 2px rgba(0,0,0,0.1);
}

.SideBar .user_account_box{
    padding: 10px;
    display: flex;
    margin-top: 10px;
    border-radius: 5px;
    color: rgba(255,255,255,0.8);
    background: #76448A;
}
.SideBar .user_account_box .account_details{
    margin-left: 10px;
}
.SideBar .user_account_box p:last-child{
    color: rgba(255,255,255,0.6);
    font-size: 12px;
    margin-top: 5px;
}

.SideBar .contol_sidebar_box{
    padding: 10px;
    display: flex;
    justify-content: right;
}

.SideBar #contol_sidebar_btn{
    padding: 5px;
    border: none;
    outline: none;
    font-size: 1.3em;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(255,255,255,0.2);
    color: #fff;
    cursor: pointer;
}

.SideBar #plan_type{
    font-size: 12px;
    color: rgba(255,255,255,0.8);
}

.SideBar ul{
    margin-top: 1em;
}

#line{
    width: 100%;
    height: 1.2px;
    background: rgba(255,255,255,0.1);
}

.SideBar .logo_box{
    width: 100%;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
}

.SideBar .logo_box h2{
    font-weight: 2em;
    color: aliceblue;
}

.SideBar ul li{
    width: 100%;
    list-style: none;
    margin-top: 10px;
}

.SideBar ul li .ActiveMenu{
    background: rgba(255,255,255,0.1);
}

.SideBar ul li a{
    padding: 12px 15px;
    color: rgba(255,255,255,0.8);
    display: inline-block;
    width: 100%;
    height: 100%;
    cursor: pointer;
    text-decoration: none;
    border-radius: 5px;
}

.SideBar ul li:nth-child(1) i{
    color: #3498DB;
}

.SideBar ul li:nth-child(2) i{
    color: #2ECC71;
}

.SideBar ul li:nth-child(3) i{
    color: #3498DB;
}

.SideBar ul li:nth-child(4) i{
    color: #F4D03F;
}

.SideBar ul li:nth-child(5) i{
    color: #3498DB;
}

.SideBar ul li a:hover{
    background: rgba(255,255,255,0.1);
}

.SideBar ul li a i{
    margin-right: 10px;
    font-size: 1.1em;
}
.Panel_View .top_bar .hide_view{
    display: none;
}

</style>

</head>
<body>

<div class="Panel_View">

    <div class="SideBar">

      <div class="contol_sidebar_box">
        <button id="contol_sidebar_btn" onclick="HandleMenu()"><i class='bx bx-chevron-left'></i></button>
      </div>

      <div class="user_account_box">
        <i class='bx bx-user'></i>
        <div class="account_details">
            <p>+91 2580362580</p>
            <p>admin</p>
        </div>
      </div>

      <br>
      <ul id="ul_menu_bar">
        <li><a onclick="ShowSelectedOption('Dashboard')" id="DashboardMenu"><i class='bx bx-grid-alt'></i>Dashboard</a></li>
        <li><a onclick="ShowSelectedOption('Challans')" id="ChallanMenu"><i class='bx bx-receipt'></i>Create Challan</a></li>
        <li><a onclick="ShowSelectedOption('MyChallans')" id="MyChallansMenu"><i class='bx bxs-user'></i>My Challans</a></li>
        <li><a href="../api/delete_all_challan.php"><i class='bx bx-trash-alt'></i>Clear All Challans</a></li>
                <li><a onclick="LogoutAccount()" id="MyChallansMenu"><i class='bx bxs-cog'></i>Logout</a></li>
    </ul>

    </div>

    <div class="top_bar">
      <div class="menu_control_box">
       <button id="menu_btn" onclick="HandleMenu()"><i class='bx bx-menu' ></i></button>  
       <h2 id="logo">Dashboard</h2>
      </div>
      <button class="total_challans_tv hide_view"></button>
    </div>

    <div class="MenuData"><!DOCTYPE html>
<html lang="en">
<head>

<style>
.transactions_items_layout{
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 10px;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.transactions_items_layout::-webkit-scrollbar{
    display: none;
}

#data{
    border-collapse: collapse;
    width: 100%;
    margin-top: 1em;
    border-radius: 10px;
    background-color: #fff;
    overflow-x: scroll;
}
/* #data thead tr th:first-child{
    border-top-left-radius: 10px;
}

#data thead tr th:last-child{
    border-top-right-radius: 10px;
}

#data tbody tr:last-child td:first-child{
    border-bottom-left-radius: 10px;
}
#data tbody tr:last-child td:last-child{
    border-bottom-right-radius: 10px;
} */

#data td, #data th{
  padding: 10px;
  max-width: 200px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

#data thead tr{
    background-color: rgba(0,0,0,0.08);
}

#data tbody tr:nth-child(odd){
    background-color: rgba(0,0,0,0.02);
}

#data td{
    font-size: 14px;
}

#data .no_data_found_box{
    padding: 15px;
}

#data th{
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    font-size: 15px;
    color: rgba(0,0,0,0.7);
}

#data tr p#status_box{
    padding: 5px 0;
    width: 80px;
    background: #E8DAEF;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
}
#data tr p#copy_btn{
    padding: 5px 0;
    width: 70px;
    background: #28B463;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
    color: #fff;
    cursor: pointer;
}
#data .sort_issue_date{
    cursor: pointer;
}
#data .sort_issue_date:hover{
    background: #D2B4DE;
}
#order_id{
    cursor: pointer;
    color: #AF7AC5;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
}
#order_id:hover{
    text-decoration: underline;
}

.pagination_box{
    display: flex;
    align-items: center;
}

.pagination_box .nxt_pre_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    margin-left: 10px;
    background:  #283747;
    cursor: pointer;
}
.pagination_box .pages_btn{
    margin-left: 10px;
}
.pagination_box .pages_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    cursor: pointer;
    background:  rgba(0,0,0,0.1);
}
.pagination_box .pages_btn a:active{
    background:  #283747;
}
.pagination_box .pages_btn a.active_page_btn{
    background:  #283747;
}


.floating_action_btns{
    position: fixed;
    right: 30px;
    bottom: 30px;
    display: flex;
    align-items: center;
}

.floating_action_btns button{
    border: none;
    outline: none;
    height: 40px;
    width: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background: #2E4053;
    color: #fff;
    margin-right: 10px;
    font-size: 1.2em;
    cursor: pointer;
}

.transactions_items_layout .hide_view{
    display: none;
}

</style>

</head>
<body>

<div class="transactions_items_layout">

   <table id="data">
       <thead>
		 <tr>
			<th>Challan No</th>
			<th class="sort_issue_date" onclick="SortIssueDate('all_challans')">Issue Date&nbsp;<i class='bx bx-sort'></i></th>
			<th>Valid Date</th>
			<th>Vehicle No</th>
			<th>Sand Quantity</th>	
		 </tr>
       </thead>
       <tbody id="tbody_data_box"></tbody>
	</table><br>

    <div class="pagination_box hide_view">
     </div>

    <div class="floating_action_btns">
      <button onclick="ShowSelectedOption('Challans')"><i class='bx bx-plus'></i></button>
      <button onclick="ShowFilterChallans()"><i class='bx bx-search'></i></button>
    </div>

</div>

</body>
</html></div>
           
</div>

<script>
let IsMenuOpen = false,OrderType='asc';
let dashboard_loading_holder = null;
let DashboardMenu = document.querySelector("#DashboardMenu");
let ChallanMenu = document.querySelector("#ChallanMenu");
let MyChallansMenu = document.querySelector("#MyChallansMenu");
let ul_menu_bar = document.querySelector("#ul_menu_bar");
let SideBar = document.querySelector(".SideBar");
let Panel_View = document.querySelector(".Panel_View");
let total_challans_tv = document.querySelector(".top_bar .total_challans_tv");

function HandleMenu(){
    if(IsMenuOpen==true){
        IsMenuOpen=false;
        SideBar.style.transform = "translateX(-300px)";
    }else{
        IsMenuOpen=true;
        SideBar.style.transform = "translateX(0px)";
    }
}

function ShowSelectedOption(option){
    dashboard_loading_holder = document.querySelector(".dashboard_loading_holder");
    let MenuData = document.querySelector(".Panel_View .MenuData");
    DashboardMenu.classList.remove("ActiveMenu");
    ChallanMenu.classList.remove("ActiveMenu");
    MyChallansMenu.classList.remove("ActiveMenu");
    total_challans_tv.classList.add("hide_view");
    OrderType='asc';

    if(option == 'Dashboard' || option == 'DeDashboard'){             
        MenuData.innerHTML = "";
        dashboard_loading_holder.classList.remove("hide_view");
        MenuData.innerHTML = `<!DOCTYPE html>
<html lang="en">
<head>

<style>
.transactions_items_layout{
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 10px;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.transactions_items_layout::-webkit-scrollbar{
    display: none;
}

#data{
    border-collapse: collapse;
    width: 100%;
    margin-top: 1em;
    border-radius: 10px;
    background-color: #fff;
    overflow-x: scroll;
}
/* #data thead tr th:first-child{
    border-top-left-radius: 10px;
}

#data thead tr th:last-child{
    border-top-right-radius: 10px;
}

#data tbody tr:last-child td:first-child{
    border-bottom-left-radius: 10px;
}
#data tbody tr:last-child td:last-child{
    border-bottom-right-radius: 10px;
} */

#data td, #data th{
  padding: 10px;
  max-width: 200px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

#data thead tr{
    background-color: rgba(0,0,0,0.08);
}

#data tbody tr:nth-child(odd){
    background-color: rgba(0,0,0,0.02);
}

#data td{
    font-size: 14px;
}

#data .no_data_found_box{
    padding: 15px;
}

#data th{
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    font-size: 15px;
    color: rgba(0,0,0,0.7);
}

#data tr p#status_box{
    padding: 5px 0;
    width: 80px;
    background: #E8DAEF;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
}
#data tr p#copy_btn{
    padding: 5px 0;
    width: 70px;
    background: #28B463;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
    color: #fff;
    cursor: pointer;
}
#data .sort_issue_date{
    cursor: pointer;
}
#data .sort_issue_date:hover{
    background: #D2B4DE;
}
#order_id{
    cursor: pointer;
    color: #AF7AC5;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
}
#order_id:hover{
    text-decoration: underline;
}

.pagination_box{
    display: flex;
    align-items: center;
}

.pagination_box .nxt_pre_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    margin-left: 10px;
    background:  #283747;
    cursor: pointer;
}
.pagination_box .pages_btn{
    margin-left: 10px;
}
.pagination_box .pages_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    cursor: pointer;
    background:  rgba(0,0,0,0.1);
}
.pagination_box .pages_btn a:active{
    background:  #283747;
}
.pagination_box .pages_btn a.active_page_btn{
    background:  #283747;
}


.floating_action_btns{
    position: fixed;
    right: 30px;
    bottom: 30px;
    display: flex;
    align-items: center;
}

.floating_action_btns button{
    border: none;
    outline: none;
    height: 40px;
    width: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background: #2E4053;
    color: #fff;
    margin-right: 10px;
    font-size: 1.2em;
    cursor: pointer;
}

.transactions_items_layout .hide_view{
    display: none;
}

</style>

</head>
<body>

<div class="transactions_items_layout">

   <table id="data">
       <thead>
		 <tr>
			<th>Challan No</th>
			<th class="sort_issue_date" onclick="SortIssueDate('all_challans')">Issue Date&nbsp;<i class='bx bx-sort'></i></th>
			<th>Valid Date</th>
			<th>Vehicle No</th>
			<th>Sand Quantity</th>	
		 </tr>
       </thead>
       <tbody id="tbody_data_box"></tbody>
	</table><br>

    <div class="pagination_box hide_view">
     </div>

    <div class="floating_action_btns">
      <button onclick="ShowSelectedOption('Challans')"><i class='bx bx-plus'></i></button>
      <button onclick="ShowFilterChallans()"><i class='bx bx-search'></i></button>
    </div>

</div>

</body>
</html>`;
        DashboardMenu.classList.add("ActiveMenu");
        LoadAllChallans(1);
    }else if(option == 'Challans' || option == 'DeChallan'){
        MenuData.innerHTML = "";
        MenuData.innerHTML = `
<!DOCTYPE html>
<html>
<style>
 *{
     box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}

.form_box{
  width: 100%;
  display: flex;
  justify-content: center;
}

.form_box .form{
  width: 500px;
  display: flex;
	flex-direction: column;
	padding: 10px;
  margin: 2em 0;
  box-shadow: 0.1px 4px 8px 2px rgba(0,0,0,0.05);
}

.input_box{
	display: flex;
  flex-direction: column;
  margin-top: 15px;
}
.input_box p{
	color: #EC407A;
}
.input_box input{
   width: 100%;
   height: 50px;
   font-size: 18px;
   padding: 0 10px;
   margin-top: 10px;
}
.form_box #action_btn{
   width: 100%;
   height: 50px;
   margin-top: 30px;
   cursor: pointer;
   font-size: 18px;
   color: #fff;
   outline: none;
   border: none;
   background: #283747;
}
.input_box #desc{
	width: 100%;
	height: 80px;
	resize: none;
  margin-top: 10px;
  font-size: 18px;
  padding: 5px 10px;
}

select{
    padding: 10px;
}


@media (max-width: 500px) {
        .input_box{
        flex-direction: column;
    }
    .input_box .small_box{
	   width: 100%;
    }
}

</style>
<body>
  
<div class="form_box">
    
  <div class="form">

   <h2>Create new challan</h2><br>

   <div class="input_box">
        <p>Challan No</p>
        <input type="text" name="product_id" id="challan_no" placeholder="Challan Number" autocomplete="off" id="post">
    </div>

    <div class="input_box">
        <p>Issue Date</p>
        <input type="text" name="product_id" id="issue_date" placeholder="Select Date" value="" autocomplete="off" id="post">
    </div>

    <div class="input_box">
        <p>Issue Time</p>
        <input type="text" name="product_id" id="issue_time" placeholder="Select Time" value="" autocomplete="off" id="post">
    </div>

    <div class="input_box">
        <p>Valid Date</p>
        <input type="text" name="product_id" id="valid_date" placeholder="Select Date" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>Valid Time</p>
        <input type="text" name="product_id" placeholder="Select Time" id="valid_time" value="" autocomplete="off" id="post">
    </div>

    <div class="input_box">
        <p>Quantity of sand</p>
        <input type="text" name="product_id" placeholder="Quantity of sand" id="quantity_of_sand" value="" autocomplete="off" id="post">
    </div>
        
    <div class="input_box">
        <p>Vehicle No</p>
        <input type="text" name="product_id" placeholder="Vehicle Number" id="vehicle_number" value="" autocomplete="off" id="post">
    </div>
  
    <div class="input_box">
        <p>Block Id</p>
        <input type="text" name="product_id" placeholder="Block Id" id="block_id" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>River Name</p>
        <input type="text" name="product_id" placeholder="River Name" id="river_name" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>Block District</p>
        <input type="text" name="product_id" placeholder="Block District" id="block_district" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>Lessee</p>
        <input type="text" name="product_id" placeholder="Lessee" id="lessee" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>Destination District</p>
        <input type="text" name="product_id" placeholder="Destination Distric" id="destination_district" value="" autocomplete="off" id="post">
    </div>
    
    <div class="input_box">
        <p>Purchaser Name</p>
        <input type="text" name="product_id" placeholder="Purchaser Name" id="purchaser_name" value="" autocomplete="off" id="post">
    </div>
     
    <button id="action_btn" onclick="CreateNewChallan()">Create New Challan</button>

  </div>

</div>

  
</body>
</html>

`;
        ChallanMenu.classList.add("ActiveMenu");
    }else if(option == 'MyChallans' || option == 'DeMyChallan'){
        MenuData.innerHTML = "";
        dashboard_loading_holder.classList.remove("hide_view");
        MenuData.innerHTML = `<!DOCTYPE html>
<html lang="en">
<head>

<style>
.transactions_items_layout{
    width: 100%;
    display: flex;
    flex-direction: column;
    padding: 10px;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.transactions_items_layout::-webkit-scrollbar{
    display: none;
}

#data{
    border-collapse: collapse;
    width: 100%;
    margin-top: 1em;
    border-radius: 10px;
    background-color: #fff;
    overflow-x: scroll;
}
/* #data thead tr th:first-child{
    border-top-left-radius: 10px;
}

#data thead tr th:last-child{
    border-top-right-radius: 10px;
}

#data tbody tr:last-child td:first-child{
    border-bottom-left-radius: 10px;
}
#data tbody tr:last-child td:last-child{
    border-bottom-right-radius: 10px;
} */

#data td, #data th{
  padding: 10px;
  max-width: 200px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

#data thead tr{
    background-color: rgba(0,0,0,0.08);
}

#data tbody tr:nth-child(odd){
    background-color: rgba(0,0,0,0.02);
}

#data td{
    font-size: 14px;
}

#data .no_data_found_box{
    padding: 15px;
}

#data th{
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    font-size: 15px;
    color: rgba(0,0,0,0.7);
}

#data tr p#status_box{
    padding: 5px 0;
    width: 80px;
    background: #E8DAEF;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
}
#data tr p#copy_btn{
    padding: 5px 0;
    width: 70px;
    background: #28B463;
    font-size: 12px;
    text-align: center;
    border-radius: 6px;
    color: #fff;
    cursor: pointer;
}
#data .sort_issue_date{
    cursor: pointer;
}
#data .sort_issue_date:hover{
    background: #D2B4DE;
}
#order_id{
    cursor: pointer;
    color: #AF7AC5;
    -webkit-touch-callout: none;
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
}
#order_id:hover{
    text-decoration: underline;
}

.pagination_box{
    display: flex;
    align-items: center;
}

.pagination_box .nxt_pre_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    margin-left: 10px;
    background:  #283747;
    cursor: pointer;
}
.pagination_box .pages_btn{
    margin-left: 10px;
}
.pagination_box .pages_btn a{
    text-decoration: none;
    padding: 5px 10px;
    color: #fff;
    display: inline-block;
    border-radius: 5px;
    cursor: pointer;
    background:  rgba(0,0,0,0.1);
}
.pagination_box .pages_btn a:active{
    background:  #283747;
}
.pagination_box .pages_btn a.active_page_btn{
    background:  #283747;
}


.floating_action_btns{
    position: fixed;
    right: 30px;
    bottom: 30px;
    display: flex;
    align-items: center;
}

.floating_action_btns button{
    border: none;
    outline: none;
    height: 40px;
    width: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background: #2E4053;
    color: #fff;
    margin-right: 10px;
    font-size: 1.2em;
    cursor: pointer;
}

.transactions_items_layout .hide_view{
    display: none;
}

</style>

</head>
<body>

<div class="transactions_items_layout">

   <table id="data">
       <thead>
		 <tr>
			<th>Challan No</th>
            <th class="sort_issue_date" onclick="SortIssueDate('my_challans')">Issue Date&nbsp;<i class='bx bx-sort'></i></th>
			<th>Valid Date</th>
			<th>Vehicle No</th>
			<th>Sand Quantity</th>	
		 </tr>
       </thead>
       <tbody id="tbody_data_box"></tbody>
	</table><br>

    <div class="pagination_box hide_view">
     </div>

    <div class="floating_action_btns">
      <button onclick="ShowSelectedOption('Challans')"><i class='bx bx-plus'></i></button>
      <button onclick="ShowFilterChallans()"><i class='bx bx-search'></i></button>
    </div>

</div>

</body>
</html>`;
        MyChallansMenu.classList.add("ActiveMenu");
        LoadMyChallans(1);
    }

    if(IsMenuOpen==true){
      HandleMenu();
    }
}

function LoadAllChallans(page_no){
   let tbody_data_box = document.querySelector("#tbody_data_box");
   let pagination_box = document.querySelector(".pagination_box");

   let content = 15;
   let offset = (page_no-1)*content;

   var formData = {
     'offset': offset,
     'content': content,
     'requestedby': 2580362580,
   }

   let jsondata = JSON.stringify(formData);

   fetch('../api/load_all_challans.php',{
    method : 'POST',
    body: jsondata,
    headers:{
      'Content-type': 'application/json',
    }
   })
    .then((response)=> response.json())
    .then((data) =>{
        if(data['success']=='failed'){
            dashboard_loading_holder.classList.add("hide_view");
            tbody_data_box.innerHTML = "<div class='no_data_found_box'><i class='bx bx-search'></i>&nbsp;No data found</div>";
        }else{
            let total_content = data['total_content'];
            let total_pages = data['total_page'];
            let DynamicHtml = '';
            for(var i in data['data']){
                DynamicHtml += 
                `<tr>
			      <td><p id="order_id" onclick="ShowTransacInfoDialog('${data['data'][i]['challan_no']}')">${data['data'][i]['challan_no']}</p></td>
			      <td>${data['data'][i]['challan_date']}</td>
		          <td>${data['data'][i]['valid_date']}</td>
		          <td>${data['data'][i]['vehicle_no']}</td>
		          <td>${data['data'][i]['sand_quantity']}</td>
	            </tr>`
            }
            tbody_data_box.innerHTML = DynamicHtml;

            if(total_pages > 1){
                let DynamicHtml = '';

                if(page_no > 1){
                    DynamicHtml += 
                    `<div class="nxt_pre_btn">
                      <a onclick="LoadAllChallans(${page_no-1})">Previous</a>
                     </div>`;
                }

                if(total_pages==2){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadAllChallans(1)" class="active_page_btn">1</a>
                     <a onclick="LoadAllChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages == 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadAllChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadAllChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadAllChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages > 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadAllChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadAllChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadAllChallans(${total_pages-1})">${total_pages-1}</a>
                     <a onclick="LoadAllChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }

                if(page_no != total_pages){
                   DynamicHtml +=
                   `<div class="nxt_pre_btn">
                      <a onclick="LoadAllChallans(${page_no+1})">Next</a>
                   </div>`;
                }

                   pagination_box.innerHTML = DynamicHtml;
                   pagination_box.classList.remove('hide_view');
            }

            total_challans_tv.classList.remove('hide_view');
            total_challans_tv.innerHTML = `<i class='bx bx-receipt'></i>`+total_content;
            dashboard_loading_holder.classList.add("hide_view");
        }
    }).catch((error)=>{
        console.log(error);
        dashboard_loading_holder.classList.add("hide_view");
    });
}

function LoadMyChallans(page_no,type){
   let tbody_data_box = document.querySelector("#tbody_data_box");
   let pagination_box = document.querySelector(".pagination_box");

   let content = 15;
   let offset = (page_no-1)*content;

   var formData = {
     'offset': offset,
     'content': content,
   }

   let jsondata = JSON.stringify(formData);

   fetch('../api/load_my_challans.php',{
    method : 'POST',
    body: jsondata,
    headers:{
      'Content-type': 'application/json',
    }
   })
    .then((response)=> response.json())
    .then((data) =>{
        if(data['success']=='failed'){
            dashboard_loading_holder.classList.add("hide_view");
            tbody_data_box.innerHTML = "<div class='no_data_found_box'><i class='bx bx-search'></i>&nbsp;No data found</div>";
        }else{
            let total_content = data['total_content'];
            let total_pages = data['total_page'];
            let DynamicHtml = '';
            for(var i in data['data']){
                DynamicHtml += 
                `<tr>
			      <td><p id="order_id" onclick="ShowTransacInfoDialog('${data['data'][i]['challan_no']}')">${data['data'][i]['challan_no']}</p></td>
			      <td>${data['data'][i]['challan_date']}</td>
		          <td>${data['data'][i]['valid_date']}</td>
		          <td>${data['data'][i]['vehicle_no']}</td>
		          <td>${data['data'][i]['sand_quantity']}</td>
	            </tr>`
            }
            tbody_data_box.innerHTML = DynamicHtml;

            if(total_pages > 1){
                let DynamicHtml = '';

                if(page_no > 1){
                    DynamicHtml += 
                    `<div class="nxt_pre_btn">
                      <a onclick="LoadMyChallans(${page_no-1})">Previous</a>
                     </div>`;
                }

                if(total_pages==2){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(1)" class="active_page_btn">1</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages == 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadMyChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages > 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadMyChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadMyChallans(${total_pages-1})">${total_pages-1}</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }

                if(page_no != total_pages){
                   DynamicHtml +=
                   `<div class="nxt_pre_btn">
                      <a onclick="LoadMyChallans(${page_no+1})">Next</a>
                   </div>`;
                }

                   pagination_box.innerHTML = DynamicHtml;
                   pagination_box.classList.remove('hide_view');
            }

            total_challans_tv.classList.remove('hide_view');
            total_challans_tv.innerHTML = `<i class='bx bx-receipt'></i>`+total_content;
            dashboard_loading_holder.classList.add("hide_view");
        }
    }).catch((error)=>{
        console.log(error);
        dashboard_loading_holder.classList.add("hide_view");
    });
}

function LoadFilterChallans(type){
   let tbody_data_box = document.querySelector("#tbody_data_box");
   let pagination_box = document.querySelector(".pagination_box");

   let content = 15,page_no=1;
   let offset = (page_no-1)*content;

   var formData = {
     'offset': offset,
     'content': content,
     'type': type,
     'order': OrderType,
   }

   let jsondata = JSON.stringify(formData);

   fetch('../api/load_filter_challans.php',{
    method : 'POST',
    body: jsondata,
    headers:{
      'Content-type': 'application/json',
    }
   })
    .then((response)=> response.json())
    .then((data) =>{
        if(data['success']=='failed'){
            dashboard_loading_holder.classList.add("hide_view");
            tbody_data_box.innerHTML = "<div class='no_data_found_box'><i class='bx bx-search'></i>&nbsp;No data found</div>";
        }else{
            let total_content = data['total_content'];
            let total_pages = data['total_page'];
            let DynamicHtml = '';
            for(var i in data['data']){
                DynamicHtml += 
                `<tr>
			      <td><p id="order_id" onclick="ShowTransacInfoDialog('${data['data'][i]['challan_no']}')">${data['data'][i]['challan_no']}</p></td>
			      <td>${data['data'][i]['challan_date']}</td>
		          <td>${data['data'][i]['valid_date']}</td>
		          <td>${data['data'][i]['vehicle_no']}</td>
		          <td>${data['data'][i]['sand_quantity']}</td>
	            </tr>`
            }
            tbody_data_box.innerHTML = DynamicHtml;

            if(total_pages > 1){
                let DynamicHtml = '';

                if(page_no > 1){
                    DynamicHtml += 
                    `<div class="nxt_pre_btn">
                      <a onclick="LoadMyChallans(${page_no-1})">Previous</a>
                     </div>`;
                }

                if(total_pages==2){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(1)" class="active_page_btn">1</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages == 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadMyChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }else if(total_pages > 3){
                    DynamicHtml +=
                    `<div class="pages_btn">
                     <a onclick="LoadMyChallans(${total_pages-total_pages+1})" class="active_page_btn">${total_pages-total_pages+1}</a>
                     <a onclick="LoadMyChallans(${total_pages-total_pages+2})">${total_pages-total_pages+2}</a>
                     <a onclick="LoadMyChallans(${total_pages-1})">${total_pages-1}</a>
                     <a onclick="LoadMyChallans(${total_pages})">${total_pages}</a>
                   </div>`;
                }

                if(page_no != total_pages){
                   DynamicHtml +=
                   `<div class="nxt_pre_btn">
                      <a onclick="LoadMyChallans(${page_no+1})">Next</a>
                   </div>`;
                }

                   pagination_box.innerHTML = DynamicHtml;
                   pagination_box.classList.remove('hide_view');
            }

            if(OrderType=='asc'){
                OrderType='desc';
            }else{
                OrderType='asc';
            }
            
            total_challans_tv.classList.remove('hide_view');
            total_challans_tv.innerHTML = `<i class='bx bx-receipt'></i>`+total_content;
            dashboard_loading_holder.classList.add("hide_view");
        }
    }).catch((error)=>{
        console.log(error);
        dashboard_loading_holder.classList.add("hide_view");
    });
}

</script>

</body>
</html>
    <div class="dialog_view_holder"></div>

    <div class="crudentials hide_view">
        <p id="user_id_tv">2580362580</p>
    </div>

    <div class="dashboard_loading_holder hide_view">
        <div class="dashboard_loader"></div>
    </div>
    
 <script src="qrcode.min.js"></script>
    
 <script>
let dialog_view_holder = document.querySelector(".dialog_view_holder");

  function OpenAURL(url){
    window.open(url);
  }

  function ShowFilterChallans(){
    dialog_view_holder.innerHTML = "";
    dialog_view_holder.innerHTML = `<!DOCTYPE html>
<html lang="en">
<head>
<style>
    .dialog_view_layout{
      position: absolute;
      left: 0;
      top: 0;
      height: 100vh;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(0,0,0,0.5);
      z-index: 1000000;
    }
    .dialog_view_layout .dialog_view{
        position: relative;
        height: auto;
        width: 330px;
        background: #fff;
        border-radius: 5px;
        padding: 15px;
    }
    .dialog_view_layout .dialog_view p{
        color: rgba(0,0,0,0.6);
    }
    .dialog_view_layout .dialog_top_part{
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 10px;
    }
    .dialog_view_layout .dialog_top_part p{
        font-weight: bold;
    }
    .dialog_view_layout .close_dialog_btn{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 30px;
        width: 30px;
        font-size: 1em;
        cursor: pointer;
        border-radius: 50%;
        background: rgba(0,0,0,0.05);
    }
    .dialog_view_layout #info_txt{
        font-size: 13px;
    }
    .dialog_view_layout .input_data_box{
        margin-top: 15px;
    }
    .dialog_view_layout .input_data_box input::placeholder{
        color: rgba(0,0,0,0.5);
    }
    .dialog_view_layout .input_data_box p{
        font-size: 13px;
        font-weight: bold;
    }
    .dialog_view_layout .input_data_box input{
        height: 40px;
        padding: 0 7px;
        width: 100%;
        font-size: 0.92em;
        margin-top: 6px;
        outline: none;
        border-radius: 5px;
        color: rgba(0,0,0,0.8);
        border: 1px solid rgba(0,0,0,0.08);
    }

    .dialog_view_layout .action_btn{
      border: none;
      outline: none;
      color: #fff;
      cursor: pointer;
      padding: 12px 18px;
      font-size: 1em;
      border-radius: 5px;
      background: #6C3483;
    }

    .dialog_view_layout a{
        display: inline-block;
        font-size: 12px;
        margin-top: 10px;
    }

    .select_op_box{
    margin-top: 1em;
  }

  .select_op_box select{
    display: inline-block;
    padding: 10px;
    font-size: 16px;
    width: 100%;
    border: 1px solid rgba(0, 0, 0, 0.1);
}

  .select_op_box p{
      margin-bottom: 10px;
  }

  .dialog_view_layout .dialog_view_loader {
	  display: block;
	  border: 2px solid rgba(0,0,0,0.1);
	  border-radius: 50%;
	  border-top: 2px solid #283747;
	  width: 30px;
	  height: 30px;
	  -webkit-animation: spin 0.5s linear infinite; /* Safari */
	  animation: spin 0.5s linear infinite;
    }
  
  /* Safari */
  @-webkit-keyframes spin {
	0% { -webkit-transform: rotate(0deg); }
	100% { -webkit-transform: rotate(360deg); }
  }
  
  @keyframes spin {
	0% { transform: rotate(0deg); }
	100% { transform: rotate(360deg); }
  }

.dialog_view_layout .hide_view{
    display: none;
}

</style>
</head>
<body>

<div class="dialog_view_layout">
    <div class="dialog_view">
      <div class="dialog_top_part">
        <p>Search / Filter</p>
        <div class="close_dialog_btn" onclick="CloseDialogMsg()"><i class='bx bx-x' ></i></div>
      </div>

      <div class="input_data_box">
          <input type="text" id="search_input" placeholder="Search challan no,vehicle no & more">
      </div>

      <br><br>
      <button class="action_btn" onclick="SearchRecord()">Search Record&nbsp;&nbsp;<i class='bx bx-search'></i></button>
      <div class="dialog_view_loader hide_view"></div>
    </div>
</div>
    
</body>
</html>`;
  }

function ShowTransacInfoDialog(challan_no){
  dashboard_loading_holder.classList.remove("hide_view");

  var formData = {
    'challan_no': challan_no,
  }

  let jsondata = JSON.stringify(formData);

  fetch('../api/load_challan_info.php',{
    method : 'POST',
    body: jsondata,
    headers:{
     'Content-type': 'application/json',
    }
  })
  .then((response)=> response.json())
  .then((data) =>{
    if(data['empty']){
        dialog_view_holder.innerHTML = "";
        dashboard_loading_holder.classList.add("hide_view");
        alert("Oops!, failed to fetch data!");
    }else{
      dialog_view_holder.innerHTML = "";
      dialog_view_holder.innerHTML = `<!DOCTYPE html>
<html lang="en">
<head>
<style>
    .dialog_view_layout{
      position: absolute;
      left: 0;
      top: 0;
      min-height: 100vh;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(0,0,0,0.5);
      z-index: 1000000;
    }
    .dialog_view_layout .dialog_view{
        position: relative;
        height: auto;
        width: 340px;
        background: #fff;
        border-radius: 5px;
        padding: 15px;
    }
    .dialog_view_layout .dialog_view p{
        color: rgba(0,0,0,0.6);
    }
    .dialog_view_layout .dialog_top_part{
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 10px;
    }
    .dialog_view_layout .dialog_top_part p{
        font-weight: bold;
    }
    .dialog_view_layout .close_dialog_btn{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 30px;
        width: 30px;
        font-size: 1em;
        cursor: pointer;
        border-radius: 50%;
        background: rgba(0,0,0,0.05);
    }
    .dialog_view_layout #info_txt{
        font-size: 13px;
    }
    .dialog_view_layout .input_data_box{
        margin-top: 15px;
    }
    .dialog_view_layout .input_data_box p{
        font-size: 13px;
        font-weight: bold;
    }
    .dialog_view_layout .input_data_box input{
        height: 35px;
        padding: 0 7px;
        width: 100%;
        font-size: 1em;
        margin-top: 6px;
        outline: none;
        border-radius: 5px;
        color: rgba(0,0,0,0.5);
        border: 1px solid rgba(0,0,0,0.08);
    }

    .dialog_view_layout .action_btn{
      border: none;
      outline: none;
      color: #fff;
      cursor: pointer;
      padding: 12px 18px;
      border-radius: 5px;
      background: #6C3483;
    }

    .dialog_view_layout .edit_btn{
        background: #2E4053;
    }

    .dialog_view_layout .red_back{
        background: #EC7063;
    }

    .dialog_view_layout .info_in_table_box{
        display: grid;
        margin-top: 15px;
        grid-template-columns: 1fr 1fr;
    }

    .dialog_view_layout .info_in_table_box p{
        font-size: 14px;
        font-weight: bold;
        color: rgba(0,0,0,0.5);
    }

    .dialog_view_layout .info_in_table_box p:first-child{
        color: rgba(0,0,0,0.4);
    }

    .dialog_view_layout #info_url_tv{
        font-size: 13px;
        font-weight: bold;
        margin-top: 5px;
        color: rgba(0,0,0,0.5);
    }

    .qr_box img{
        height: 70px;
    }
</style>
</head>
<body>

<div class="dialog_view_layout">
    <div class="dialog_view">
      <div class="dialog_top_part">
        <p><i class='bx bx-info-circle' ></i>&nbsp;Details</p>
        <div class="close_dialog_btn" onclick="CloseDialogMsg()"><i class='bx bx-x' ></i></div>
      </div>

      <div class="qr_box" id="qr_box">
      </div>

      <div class="info_in_table_box">
          <p>Challan No: </p>
          <p id="challan_no_tv"></p>
      </div>

      <div class="info_in_table_box">
          <p>Valid Date </p>
          <p id="valid_date_tv"></p>
      </div>

      <div class="info_in_table_box">
          <p>Vehicle No: </p>
          <p id="vehicle_no_tv"></p>
      </div>

      <div class="info_in_table_box">
          <p>Sand Quantity: </p>
          <p id="sand_quantity"></p>
      </div>
      
      <div class="info_in_table_box">
          <p id="tran_date_title">Created By: </p>
          <p id="challan_created_by"></p>
       </div>

       <div class="info_in_table_box">
          <p id="tran_date_title">Created At: </p>
          <p id="challan_date"></p>
       </div>

       <div class="info_in_table_box tran_link_box">
          <p>Link: </p>
       </div>

       <p id="info_url_tv"></p>

       <br>
       <div>
         <button class="action_btn delete_btn red_back">Delete Challan</button>
         <button class="action_btn edit_btn green_back"><i class='bx bxs-edit-alt'></i>&nbsp;Edit</button>
       </div>
    </div>
</div>
    
</body>
</html>`;
      
      let challan_details = `https://mdtcll.wbgev.com/challan-details/${data[0]['challan_no']}`;
      
      const qrcode=new QRCode('qr_box',{
          text: challan_details,
          width: 250,
	      height: 250,
          correctLevel : QRCode.CorrectLevel.H
        });
        
      document.querySelector(".dialog_view_layout .info_in_table_box #challan_no_tv").innerHTML = data[0]['challan_no'];
      document.querySelector(".dialog_view_layout #challan_date").innerHTML = data[0]['challan_date']+' '+data[0]['challan_time'];
      document.querySelector(".dialog_view_layout #valid_date_tv").innerHTML = data[0]['valid_date'];
      document.querySelector(".dialog_view_layout #vehicle_no_tv").innerHTML = data[0]['vehicle_no'];
      document.querySelector(".dialog_view_layout #sand_quantity").innerHTML = data[0]['sand_quantity'];
      document.querySelector(".dialog_view_layout #info_url_tv").innerHTML = `https://mdtcll.wbgev.com/challan-details/`+data[0]['challan_no'];
      document.querySelector(".dialog_view_layout #challan_created_by").innerHTML = data[0]['created_by'];
      document.querySelector(".dialog_view_layout .dialog_view .edit_btn").addEventListener('click',()=>{
        OpenAURL('https://mdtcll.wbgev.com/edit-challan/edit.php'+'?challan_no='+data[0]['challan_no']);
        CloseDialogMsg();
      });

      document.querySelector(".dialog_view_layout .dialog_view .delete_btn").addEventListener('click',()=>{
        if (confirm('Are you sure you want to delete?') == true) {
          OpenAURL('https://mdtcll.wbgev.com/api/delete_challan.php'+'?challan_no='+data[0]['challan_no']);
          CloseDialogMsg();
        }
      });

      dashboard_loading_holder.classList.add("hide_view");
    }
  }).catch((error)=>{
    alert("Sorry, failed to load data!");
    dashboard_loading_holder.classList.add("hide_view");
  });

}

  function CloseDialogMsg(){
    dialog_view_holder.innerHTML = "";
  }

  function SearchRecord(){

   let content = 15,page_no=1;
   let offset = (page_no-1)*content;

    let tbody_data_box = document.querySelector("#tbody_data_box");
    let action_btn = document.querySelector(".dialog_view_layout .action_btn");
    let dialog_view_loader = document.querySelector(".dialog_view_layout .dialog_view_loader");
    let search_input = document.querySelector("#search_input");

    if(search_input.value == ""){
      alert("Oops! Invalid search term.");
      return;
    }else{
      dialog_view_loader.classList.remove("hide_view");
      action_btn.classList.add("hide_view");
    }

    var formData = {
      'search': search_input.value,
      'offset': offset,
      'content': content,
    }
  
    let jsondata = JSON.stringify(formData);

    fetch('../api/search_record.php',{
      method : 'POST',
      body: jsondata,
      headers:{
        'Content-type': 'application/json',
      }
    })
    .then((response)=> response.json())
    .then((data) =>{
        if(data['empty']){
            tbody_data_box.innerHTML = "<div class='no_data_found_box'><i class='bx bx-search'></i>&nbsp;No data found</div>";
        }else{
            let DynamicHtml = '';
            for(var i in data){
                DynamicHtml += 
                `<tr>
			      <td><p id="order_id" onclick="ShowTransacInfoDialog('${data[i]['challan_no']}','transactions')">${data[i]['challan_no']}</p></td>
			      <td>${data[i]['challan_date']}</td>
		          <td>₹${data[i]['valid_date']}</td>
		          <td>${data[i]['vehicle_no']}</td>
		          <td><p id="status_box">pending</p></td>
	            </tr>`
            }
            tbody_data_box.innerHTML = DynamicHtml;
        }
        dialog_view_loader.classList.add("hide_view");
        action_btn.classList.remove("hide_view");

     }).catch((error)=>{
        console.log(error);
        CloseDialogMsg();
        alert("Oops! something went wrong!");
        dialog_view_loader.classList.add("hide_view");
        action_btn.classList.remove("hide_view");
     });
  }
  

  function CreateNewChallan(){
    let action_btn = document.querySelector(".form_box .action_btn");
    let challan_no = document.querySelector("#challan_no");
    let issue_date = document.querySelector("#issue_date");
    let issue_time = document.querySelector("#issue_time");
    let valid_date = document.querySelector("#valid_date");
    let valid_time = document.querySelector("#valid_time");
    let quantity_of_sand = document.querySelector("#quantity_of_sand");
    let vehicle_number = document.querySelector("#vehicle_number");
    
    let block_id = document.querySelector("#block_id");
    let river_name = document.querySelector("#river_name");
    let block_district = document.querySelector("#block_district");
    let lessee = document.querySelector("#lessee");
    let destination_district = document.querySelector("#destination_district");
    let purchaser_name = document.querySelector("#purchaser_name");

    if(valid_date.value == ""){
      alert("Please fill valid date!");
      return;
    }else if(valid_time.value == ""){
      alert("Please fill valid time!");
      return;
    }else if(quantity_of_sand.value == ""){
      alert("Please fill quantity of sand!");
      return;
    }else if(vehicle_number.value == ""){
      alert("Please fill vehicle number!");
      return;
    }else if(block_id.value == "" || river_name.value == "" || block_district.value == "" || lessee.value == "" || destination_district.value == "" || purchaser_name.value == ""){
      alert("Please fill other details!");
      return;
    }else{
      dashboard_loading_holder.classList.remove("hide_view");
    }
    
    // dateSplit = valid_date.value.split("-");

    // new_day = dateSplit[2];
    // new_month = dateSplit[1];
    // new_year = dateSplit[0];

    // valid_date = new_day+"-"+new_month+"-"+new_year;
    
    // var timeSplit = valid_time.value.split(':'),hours,minutes,meridian;
    // hours = timeSplit[0];
    // minutes = timeSplit[1];
    // if (hours > 12) {
    //   meridian = 'PM';
    //   hours -= 12;
    // } else if (hours < 12) {
    //   meridian = 'AM';
    //   if (hours == 0) {
    //   hours = 12;
    //   }
    // } else {
    //   meridian = 'PM';
    // }
    // valid_time = hours + ':' + minutes + ' ' + meridian;

    var formData = {
      'challan_no': challan_no.value,
      'issue_date': issue_date.value,
      'issue_time': issue_time.value,
      'valid_date': valid_date.value,
      'valid_time': valid_time.value,
      'sand_quantity': quantity_of_sand.value,
      'vehicle_number': vehicle_number.value,
      'ch_block_id': block_id.value,
      'ch_river': river_name.value,
      'ch_block_district': block_district.value,
      'ch_lessee': lessee.value,
      'ch_destination_district': destination_district.value,
      'ch_purchaser_name': purchaser_name.value,
    }
  
    let jsondata = JSON.stringify(formData);

    fetch('../api/create_challan.php',{
      method : 'POST',
      body: jsondata,
      headers:{
        'Content-type': 'application/json',
      }
    })
    .then((response)=> response.json())
    .then((data) =>{
        if(data['failed']){
          dashboard_loading_holder.classList.add("hide_view");
          alert("Failed to create challan!");
          location.reload();
        }else if(data['exist']){
          dashboard_loading_holder.classList.add("hide_view");
          alert("Oops! something went wrong");
          location.reload();
        }else{
          dashboard_loading_holder.classList.add("hide_view");
          alert("Challan created successfully!");
          ShowSelectedOption("DeMyChallan");
        }

     }).catch((error)=>{
        dashboard_loading_holder.classList.add("hide_view");
        alert("Oops! something went wrong!");
        location.reload();
     });
  }

  function LogoutAccount(){
    const body = document.querySelector('body');
    const anchortag = document.createElement("a");
    anchortag.href=`https://mdtcll.wbgev.com/api/logout_account.php`;
    body.appendChild(anchortag);
    anchortag.click();
    body.removeChild(anchortag);
  }

  function SortIssueDate(type){
    LoadFilterChallans(type);
  }

   ShowSelectedOption("DeDashboard");

   </script>    
</body>
</html>ACCT.ALAMTRADERS@GMAIL.COM
