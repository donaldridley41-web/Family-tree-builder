
<!-- PayPal JS SDK with Venmo -->
<script 
  src="https://www.paypal.com/sdk/js?client-id=YOUR_PAYPAL_CLIENT_ID&components=hosted-buttons&enable-funding=venmo&currency=USD">
</script>

<!-- Profile Card UI -->
<div style="width:300px;background:#23232b;color:#ffd600;border-radius:12px;padding:24px;text-align:center;margin:16px auto;font-family:sans-serif;">
  <h2 style="color:#ffd600;">Your Profile</h2>
  <img src="https://api.dicebear.com/6.x/identicon/svg?seed=User123" alt="avatar" width="48" style="border-radius:50%;margin-bottom:12px;">
  <div><strong>Username:</strong> <span id="profile-username">User123</span></div>
  <div><strong>Coins:</strong> <span id="profile-coins">500</span></div>
  <div>
    <strong>Status:</strong>
    <span id="profile-vip">Standard</span>
  </div>
  <button style="background:#444;color:#fff;border:none;padding:10px 26px;border-radius:6px;margin-top:14px;">Logout</button>
</div>

<!-- Coin Store UI -->
<div style="width:340px;background:#222;border-radius:18px;padding:18px;margin:auto;text-align:center;font-family:sans-serif;">
  <h2 style="color:#FFD600;margin-bottom:24px;">Coin Store</h2>
  
  <div style="margin-bottom:16px;">
    <div style="background:#4f97ff;border-radius:8px;padding:18px 12px;color:#fff;font-weight:700;margin-bottom:3px;">500 Coins</div>
    <div id="paypal-500"></div>
    <script>
      paypal.HostedButtons({hostedButtonId:"YOUR_500_BUTTON_ID"}).render('#paypal-500');
    </script>
  </div>
  
  <div style="margin-bottom:16px;">
    <div style="background:#338AF0;border-radius:8px;padding:18px 12px;color:#fff;font-weight:700;margin-bottom:3px;">1,000 Coins</div>
    <div id="paypal-1000"></div>
    <script>
      paypal.HostedButtons({hostedButtonId:"YOUR_1000_BUTTON_ID"}).render('#paypal-1000');
    </script>
  </div>
  
  <div style="margin-bottom:16px;">
    <div style="background:#1976d2;border-radius:8px;padding:18px 12px;color:#fff;font-weight:700;margin-bottom:3px;">5,000 Coins</div>
    <div id="paypal-5000"></div>
    <script>
      paypal.HostedButtons({hostedButtonId:"YOUR_5000_BUTTON_ID"}).render('#paypal-5000');
    </script>
  </div>
  
  <div style="margin-bottom:16px;">
    <div style="background:#FFD600;padding:18px 12px;color:#222;font-weight:700;border-radius:8px;margin-bottom:3px;">
      10,000 Coins (Best Value)
    </div>
    <div id="paypal-10000"></div>
    <script>
      paypal.HostedButtons({hostedButtonId:"YOUR_10000_BUTTON_ID"}).render('#paypal-10000');
    </script>
  </div>
  
  <button style="background:#666;color:#fff;padding:12px 32px;font-size:1.12em;border-radius:8px;border:0;font-weight:700;margin-top:10px;">Close</button>
</div>

<!-- Tawk.to Live Chat Widget -->
<script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/68f9ae2903c0d7194f5d0eb1/1j87l0koc';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>

<script>
// JS to update the profile info dynamically (optional/expand as needed)
function updateProfile(user) {
  document.getElementById('profile-username').textContent = user.username;
  document.getElementById('profile-coins').textContent = user.coins;
  document.getElementById('profile-vip').textContent = user.vip ? "VIP Member" : "Standard";
}
// Example user object
let user = { username: 'User123', coins: 500, vip: false };
updateProfile(user);
</script>