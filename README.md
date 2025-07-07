# Login-Page

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Login Page</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: url('https://images.pexels.com/photos/838413/pexels-photo-838413.jpeg') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-box {
      background: rgba(255, 255, 255, 0.95);
      padding: 2rem 2.5rem;
      border-radius: 10px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
      width: 100%;
      max-width: 400px;
      position: relative;
      backdrop-filter: blur(3px);
    }

    .login-box h2 {
      text-align: center;
      margin-bottom: 1.5rem;
      color: #333;
    }

    .form-group {
      margin-bottom: 1.2rem;
    }

    .form-group label {
      display: block;
      margin-bottom: 0.5rem;
      font-weight: 600;
    }

    .form-group input {
      width: 100%;
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
    }

    .login-btn {
      width: 100%;
      padding: 0.75rem;
      background-color: #667eea;
      color: white;
      font-size: 1rem;
      font-weight: bold;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s ease;
      text-align: center;
      display: inline-block;
    }

    .login-btn:hover {
      background-color: #5a67d8;
    }

    .signup-text {
      margin-top: 1rem;
      text-align: center;
      font-size: 0.9rem;
    }

    .signup-text a {
      color: #667eea;
      text-decoration: none;
    }

    /* Hidden checkbox */
    #showCongrats {
      display: none;
    }

    /* Show congratulations box when checkbox is checked */
    #showCongrats:checked ~ .congrats-message {
      display: flex;
    }

    .congrats-message {
      display: none;
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(255, 255, 255, 0.98);
      border-radius: 10px;
      padding: 2rem;
      text-align: center;
      color: #333;
      font-size: 1.5rem;
      font-weight: bold;
      justify-content: center;
      align-items: center;
    }

    .congrats-message span {
      font-size: 2rem;
      display: block;
      margin-bottom: 1rem;
    }

    @media (max-width: 500px) {
      .login-box {
        padding: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <div class="login-box">
    <input type="checkbox" id="showCongrats" />

    <form>
      <h2>Login</h2>

      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" placeholder="you@example.com" required />
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" placeholder="••••••••" required />
      </div>

      <!-- Fake login button triggers checkbox -->
      <label for="showCongrats" class="login-btn">Login</label>

      <p class="signup-text">Don't have an account? <a href="#">Sign up</a></p>
    </form>

    <!-- Hidden Congratulations Message -->
    <div class="congrats-message">
      <span>🎉</span>
      Congratulations Login Successful!!
    </div>
  </div>
</body>
</html>
