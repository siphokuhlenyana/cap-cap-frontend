<template>
    <div class="container">
      <div class="sidebar">
        <div class="logo">
          <img src="https://i.imgur.com/g1g6K9C.png" alt="Logo" />
          <h1>DLOZIFY</h1>
        </div>
        <ul class="sidebar-menu">
          <li>
            <i class="fas fa-home"></i>
            <span>Home</span>
          </li>
          <li>
            <i class="fas fa-bookmark"></i>
            <span>Bookmarks</span>
          </li>
          <li>
            <i class="fas fa-bell"></i>
            <span>Notifications</span>
          </li>
          <li>
            <i class="fas fa-user"></i>
            <span>Profile</span>
          </li>
        </ul>
      </div>
      <div class="main-content">
        <div class="post-section">
          <div class="post-header">
            <textarea placeholder="What's on your mind?"></textarea>
            <button class="post-button">Post</button>
          </div>
          <div class="post-body">
            <img src="https://i.imgur.com/Z5b710A.jpg" alt="Post Image" />
            <div class="post-content">
              <h2>Made for your comfort!</h2>
              <div class="post-actions">
                <button class="follow-button">+Follow</button>
                <div class="suggested-users">
                  <h3>Suggested to follow</h3>
                  <div class="user-card">
                    <img src="https://i.imgur.com/q97bC5Z.jpg" alt="User Image" />
                    <div class="user-info">
                      <p>User 1</p>
                      <button class="follow-button">+Follow</button>
                    </div>
                  </div>
                  <div class="user-card">
                    <img src="https://i.imgur.com/o5N0y4Y.jpg" alt="User Image" />
                    <div class="user-info">
                      <p>User 2</p>
                      <button class="follow-button">+Follow</button>
                    </div>
                  </div>
                  <div class="user-card">
                    <img src="https://i.imgur.com/q5fX84T.jpg" alt="User Image" />
                    <div class="user-info">
                      <p>User 3</p>
                      <button class="follow-button">+Follow</button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="footer">
          <ul>
            <li>
              <i class="fas fa-envelope"></i>
            </li>
            <li>
              <i class="fas fa-info-circle"></i>
            </li>
            <li>
              <i class="fas fa-cog"></i>
            </li>
          </ul>
          <p>Dlozify©2024</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HomePage',
  };
  </script>
  
  <style scoped>
  .container {
    display: flex;
    height: 100vh;
  }
  
  .sidebar {
    background-color:#3F0639;
    width: 15%;
    padding: 20px;
  }
  
  .logo {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .logo img {
    width: 100px;
    height: 100px;
  }
  
  .sidebar-menu {
    list-style: none;
    padding: 0;
  }
  
  .sidebar-menu li {
    margin-bottom: 15px;
  }
  
  .sidebar-menu li i {
    color: #fff;
    font-size: 1.5rem;
    margin-right: 10px;
  }
  
  .sidebar-menu li span {
    color: #fff;
    font-weight: bold;
  }
  
  .main-content {
    background-color:rgb(95, 1, 95);
    background: rgb(120,9,121);
    background: linear-gradient(180deg, #3F0639 0%, #880E7C 72%,#A51196 100%);

    flex-grow: 1;
    padding: 20px;
  }
  
  /* .post-section {
    /* background-color: #fff; */
    /* padding: 20px;
    border-radius: 10px;
    background-color: #A51196;
  } */
   
  .post-header {
    display: flex;
    align-items: center;
    margin-bottom: 15px;
    
  }
  
  .post-header textarea {
    flex-grow: 1;
    padding: 10px;
    border: 1px solid #A51196;
    border-radius: 5px;
    resize: none;
  }
  
  .post-button {
    padding: 10px 20px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-left: 10px;
  }
  
  .post-body {
    display: flex;
    align-items: center;
  }
  
  .post-body img {
    width: 50%;
    height: auto;
    border-radius: 10px;
  }
  
  .post-content {
    width: 50%;
    padding: 20px;
  }
  
  .post-content h2 {
    margin-bottom: 10px;
  }
  
  .post-actions {
    margin-top: 20px;
  }
  
  .follow-button {
    padding: 10px 20px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-right: 10px;
  }
  
  .suggested-users {
    margin-top: 20px;
  }
  
  .suggested-users h3 {
    margin-bottom: 10px;
  }
  
  .user-card {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
  }
  
  .user-card img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    margin-right: 10px;
  }
  
  .user-info {
    display: flex;
    align-items: center;
  }
  
  .user-info p {
    margin-right: 10px;
  }
  
  .footer {
    background-color: #A51196;
    color: #fff;
    /* padding: 20px; */
    text-align: center;
  }
  
  .footer ul {
    list-style: none;
    padding: 0;
    /* margin-bottom: 10px; */
  }
  
  .footer ul li {
    display: inline-block;
    margin: 0 10px;
  }
  
  .footer ul li i {
    font-size: 1.5rem;
  }
  </style>