# banksite
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Bank of America – Login</title>
<style>
body{font-family:"Helvetica Neue",Helvetica,Arial,sans-serif;margin:0;background:#f5f5f5;color:#333}
.login{max-width:360px;margin:100px auto;padding:20px;background:#fff;border:1px solid #ddd;border-radius:4px}
.header{display:flex;align-items:center;margin-bottom:20px}
.header img{height:40px;margin-right:10px}
.header h2{margin:0;font-size:18px}
input{width:100%;padding:8px;margin:5px 0;border:1px solid #ccc;border-radius:3px}
button{width:100%;padding:10px;background:#004b87;color:#fff;border:none;border-radius:3px;cursor:pointer}
button:hover{background:#003a66}
.error{color:red;font-size:14px;margin-top:10px}
.statement{margin:20px;padding:20px;background:#fff;border:1px solid #ddd;border-radius:4px}
table{width:100%;border-collapse:collapse}
th,td{border:1px solid #ddd;padding:8px;text-align:left}
th{background:#f5f5f5}
.balance{font-weight:bold;font-size:18px;color:#004b87}
</style>
</head>
<body>

<div id="app">
<div v-if="!loggedIn" class="login">
<div class="header">
<img src="https:
<h2>Bank of America</h2>
</div>
<input v-model="username" placeholder="Username">
<input v-model="password" type="password" placeholder="Password">
<button @click="login">Log In</button>
<p v-if="error" class="error">{{ error }}</p>
</div>

<div v-else class="statement">
<div class="header">
<img src="https://www.bankofamerica.com/etc/designs/bofa/clientlib/img/bofa-logo.svg" alt="BofA logo">
<div>
<h2>Bank of America</h2>
<p>Account Statement</p>
</div>
</div>
<table>
<tr><th>Account Name</th><td>ASHLEY HOWARD</td></tr>
<tr><th>Account Number</th><td>****‑****‑****‑1234</td></tr>
<tr><th>Statement Period</th><td>2012‑01‑01 to 2013‑12‑31</td></tr>
<tr><th>Current Balance</th><td class="balance">$72,680.00</td></tr>
</table>

<h3>Transactions</h3>
<table>
<thead>
<tr><th>Date</th><th>Description</th><th>Amount</th></tr>
</thead>
<tbody>
<tr><td>2012‑03‑15</td><td>Online Transfer</td><td>$1,200.00</td></tr>
<tr><td>2012‑06‑02</td><td>ATM Withdrawal</td><td>-$150.00</td></tr>
<tr><td>2012‑09‑21</td><td>Deposit – Payroll</td><td>$3,500.00</td></tr>
<tr><td>2013‑01‑10</td><td>Bill Payment – Electricity</td><td>-$120.00</td></tr>
<tr><td>2013‑04‑05</td><td>Deposit – Refund</td><td>$250.00</td></tr>
</tbody>
</table>
</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.min.js"></script>
<script>
new Vue({
el:'
data:{username:'',password:'',loggedIn:false,error:null},
methods:{
login(){
if(this.username==='ashley.howard' && this.password==='password123'){
this.loggedIn=true;
this.error=null;
} else {
this.error='Invalid username or password';
}
}
}
});
</script>
</body>
</html>
