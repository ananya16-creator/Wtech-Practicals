&lt;!DOCTYPE html
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Registration Form&lt;/title&gt;
&lt;style&gt;
body {
font-family: Arial;
margin: 40px;
}
form {
width: 350px;
margin: auto;
}
input {
width: 100%;
padding: 8px;
margin: 5px 0;
}
.error {
color: red;
font-size: 14px;
}
#success {
color: green;
}
button {
padding: 8px 20px;
margin-top: 10px;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;form id=&quot;registrationForm&quot;&gt;
&lt;h2&gt;Registration Form&lt;/h2&gt;
&lt;label&gt;Name:&lt;/label&gt;

Nagar Yuwak Shikshan Sanstha’s

Yeshwantrao Chavan College of Engineering

(An Autonomous Institution affiliated to Rashtrasant Tukadoji Maharaj Nagpur University)

Hingna Road, Wanadongri, Nagpur - 441 110

NAAC A++

Ph.: 07104-237919, 234623, 329249, 329250 Fax: 07104-232376, Website: www.ycce.edu

Department of Computer Technology
Vision Statement of the Department.

To be a preferred hub for nurturing computer engineering aspirants through innovative, ethical, value-based technical education, impactful research, and
industry collaboration, to become successful professionals contributing for the betterment of society.
Mission Statement of the Department.

 To nurture computer engineering professionals by offering Dynamic learning environment that encourages problem-solving using emerging technology,
National Education Policy aligned evidence-based technical education, fostering ,innovation, research, and industry–institute collaboration &amp; Holistic,
ethical and sustainable development for lifelong success.

&lt;input type=&quot;text&quot; id=&quot;name&quot;&gt;
&lt;span id=&quot;nameError&quot; class=&quot;error&quot;&gt;&lt;/span&gt;
&lt;br&gt;&lt;br&gt;
&lt;label&gt;Email:&lt;/label&gt;
&lt;input type=&quot;text&quot; id=&quot;email&quot;&gt;
&lt;span id=&quot;emailError&quot; class=&quot;error&quot;&gt;&lt;/span&gt;
&lt;br&gt;&lt;br&gt;
&lt;label&gt;Password:&lt;/label&gt;
&lt;input type=&quot;password&quot; id=&quot;password&quot;&gt;
&lt;span id=&quot;passwordError&quot; class=&quot;error&quot;&gt;&lt;/span&gt;
&lt;br&gt;&lt;br&gt;
&lt;label&gt;Phone Number:&lt;/label&gt;
&lt;input type=&quot;text&quot; id=&quot;phone&quot;&gt;
&lt;span id=&quot;phoneError&quot; class=&quot;error&quot;&gt;&lt;/span&gt;
&lt;br&gt;
&lt;button type=&quot;submit&quot;&gt;Register&lt;/button&gt;
&lt;p id=&quot;success&quot;&gt;&lt;/p&gt;
&lt;/form&gt;
&lt;script&gt;
document.getElementById(&quot;registrationForm&quot;).addEventListener(&quot;submit&quot;,
function(event) {
event.preventDefault();
let name = document.getElementById(&quot;name&quot;).value.trim();
let email = document.getElementById(&quot;email&quot;).value.trim();
let password = document.getElementById(&quot;password&quot;).value;
let phone = document.getElementById(&quot;phone&quot;).value.trim();
let valid = true;
// Clear previous messages
document.getElementById(&quot;nameError&quot;).innerHTML = &quot;&quot;;
document.getElementById(&quot;emailError&quot;).innerHTML = &quot;&quot;;
document.getElementById(&quot;passwordError&quot;).innerHTML = &quot;&quot;;
document.getElementById(&quot;phoneError&quot;).innerHTML = &quot;&quot;;
document.getElementById(&quot;success&quot;).innerHTML = &quot;&quot;;
// Name validation
if (name === &quot;&quot;) {
document.getElementById(&quot;nameError&quot;).innerHTML =
&quot;Name is required&quot;;
valid = false;
}
// Email validation
let emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
if (email === &quot;&quot;) {
document.getElementById(&quot;emailError&quot;).innerHTML =
&quot;Email is required&quot;;
valid = false;
}
else if (!emailPattern.test(email)) {
document.getElementById(&quot;emailError&quot;).innerHTML =
&quot;Enter a valid email&quot;;
valid = false;
}
// Password validation
if (password === &quot;&quot;) {
document.getElementById(&quot;passwordError&quot;).innerHTML =
&quot;Password is required&quot;;
valid = false;
}
else if (password.length &lt; 8) {
document.getElementById(&quot;passwordError&quot;).innerHTML =
&quot;Password must contain at least 8 characters&quot;;
valid = false;
}
// Phone validation using loop
let phoneValid = true;
if (phone.length !== 10) {
phoneValid = false;
}
else {
for (let i = 0; i &lt; phone.length; i++) {
if (phone[i] &lt; &#39;0&#39; || phone[i] &gt; &#39;9&#39;) {
phoneValid = false;
break;
}
}
}
if (!phoneValid) {
document.getElementById(&quot;phoneError&quot;).innerHTML =
&quot;Phone number must contain 10 digits&quot;;
valid = false;
}
// Final result
if (valid) {
document.getElementById(&quot;success&quot;).innerHTML =
&quot;Registration successful!&quot;;
}
});
&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
