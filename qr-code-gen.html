<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>WiFi QR Code Generator</title>
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@500&family=Material+Icons&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: #f1f5f9;
      display: flex;
      align-items: center;     /* vertical center */
      justify-content: center; /* horizontal center */
      height: 100vh;           /* full viewport height */
      margin: 0;
      padding: 30px 15px;
    }

    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      max-width: 420px;
    }

    .card {
      background: #ffffff;
      padding: 24px;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      width: 100%;
    }

    h2 {
      text-align: center;
      margin-bottom: 24px;
      font-size: 22px;
      color: #374151;
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-weight: 500;
      color: #4b5563;
    }

    input, select {
      width: 100%;
      padding: 14px 12px;
      border: 1px solid #d1d5db;
      border-radius: 12px;
      font-size: 14px;
      margin-bottom: 18px;
      background: #f9fafb;
      color: #111827;
      transition: border 0.2s;
    }

    input:focus, select:focus {
      border-color: #6366f1;
      outline: none;
    }

    .password-wrapper {
      position: relative;
    }

    .password-wrapper .toggle-btn {
      position: absolute;
      right: 12px;
      top: 50%;
      transform: translateY(-50%);
      background: none;
      border: none;
      color: #ce2e2e;
      font-size: 20px;
      cursor: pointer;
      line-height: 1;           /* Add this */
      padding: 0;               /* Remove default button padding */
      display: flex;            /* Use flex for perfect vertical align */
      align-items: center;      /* Center icon vertically */
      justify-content: center;  /* Center icon horizontally */
      width: 28px;              /* Fix button size */
      height: 28px;             /* Fix button size */
    }

    #encodedString {
      background: #f3f4f6;
      padding: 12px;
      border-radius: 10px;
      font-size: 13px;
      color: #374151;
      word-break: break-word;
      margin-top: 10px;
      border: 1px dashed #cbd5e1;
      min-height: 42px;
    }

    #qrcode {
      text-align: center;
      margin-top: 24px;
    }

    .material-icons {
      font-family: 'Material Icons';
      font-weight: normal;
      font-style: normal;
      font-size: 20px;
      line-height: 1;
      letter-spacing: normal;
      text-transform: none;
      display: inline-block;
      white-space: nowrap;
      direction: ltr;
    }

    footer {
      font-size: 0.9rem;
      color: #666;
      text-align: center;
      margin-top: 20px;
      font-family: 'Roboto', sans-serif;
      user-select: none;
      width: 100%;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="card">
      <h2>📶 WiFi QR Generator</h2>

      <label for="ssid">WiFi Name (SSID)</label>
      <input type="text" id="ssid" placeholder="e.g., Home_Network" maxlength="32" required>

      <label for="encryption">Security</label>
      <select id="encryption">
        <option value="WPA">WPA/WPA2</option>
        <option value="WEP">WEP</option>
        <option value="nopass">None</option>
      </select>

      <label for="password">Password</label>
      <div class="password-wrapper">
        <input type="password" id="password" placeholder="Enter password" maxlength="63">
        <button id="toggleBtn" class="toggle-btn material-icons" type="button">visibility</button>
      </div>

      <div id="encodedString"></div>
      <div id="qrcode"></div>
    </div>

    <footer>
      © 2025 QR WiFi Tool
    </footer>
  </div>

  <script>
    const ssidInput = document.getElementById('ssid');
    const passwordInput = document.getElementById('password');
    const encryptionInput = document.getElementById('encryption');
    const toggleBtn = document.getElementById('toggleBtn');
    const encodedString = document.getElementById('encodedString');
    const qrcodeContainer = document.getElementById('qrcode');

    function updateQRCode() {
      const ssid = ssidInput.value.trim();
      const password = passwordInput.value;
      const encryption = encryptionInput.value;

      // Required validation
      if (!ssid) {
        encodedString.textContent = '⚠️ Please enter a WiFi name (SSID).';
        qrcodeContainer.innerHTML = '';
        return;
      }

      if (encryption !== 'nopass' && !password) {
        encodedString.textContent = '⚠️ Password is required for selected security.';
        qrcodeContainer.innerHTML = '';
        return;
      }

      let qrData = encryption === 'nopass'
        ? `WIFI:T:nopass;S:${ssid};;`
        : `WIFI:T:${encryption};S:${ssid};P:${password};;`;

      encodedString.textContent = "📄 " + qrData;

      qrcodeContainer.innerHTML = "";
      QRCode.toCanvas(qrData, { width: 220 }, (err, canvas) => {
        if (!err) qrcodeContainer.appendChild(canvas);
      });
    }

    function togglePasswordVisibility() {
      if (passwordInput.type === "password") {
        passwordInput.type = "text";
        toggleBtn.textContent = "visibility_off";
      } else {
        passwordInput.type = "password";
        toggleBtn.textContent = "visibility";
      }
    }

    encryptionInput.addEventListener("change", () => {
      const isNone = encryptionInput.value === "nopass";
      passwordInput.disabled = isNone;
      if (isNone) passwordInput.value = "";
      updateQRCode();
    });

    [ssidInput, passwordInput].forEach(input => {
      input.addEventListener("input", updateQRCode);
    });

    toggleBtn.addEventListener("click", togglePasswordVisibility);

    updateQRCode();
  </script>

</body>
</html>
