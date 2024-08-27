<template>
    <div class="feeds-page">
      <div class="sidebar">
        <div class="logo">
          <img src="https://i.imgur.com/W8eJ0wI.png" alt="Dlozify Logo">
        </div>
        <div class="sidebar-links">
          <router-link to="/home">
            <i class="fa fa-home"></i> Home
          </router-link>
          <router-link to="/bookmarks">
            <i class="fa fa-bookmark"></i> Bookmarks
          </router-link>
          <router-link to="/notifications">
            <i class="fa fa-bell"></i> Notifications
          </router-link>
          <router-link to="/profile">
            <i class="fa fa-user"></i> Profile
          </router-link>
        </div>
      </div>
      <div class="content">
        <div class="create-post">
          <textarea placeholder="What's on your mind?"></textarea>
          <button>Post</button>
        </div>
        <div class="feed-items">
          <div class="feed-item" v-for="item in feedItems" :key="item.id">
            <div class="user-info">
              <img :src="item.user.avatar" alt="User Avatar">
              <span>{{ item.user.name }}</span>
            </div>
            <div class="post-content">
              {{ item.content }}
            </div>
            <div class="post-actions">
              <button>Like</button>
              <button>Comment</button>
              <button>Share</button>
            </div>
          </div>
        </div>
      </div>
      <div class="sidebar">
        <div class="sidebar-title">
          Made for your comfort!
        </div>
        <button class="follow-button">+ Follow</button>
        <div class="suggested-users">
          <h3>Suggested to follow</h3>
          <div class="suggested-user" v-for="user in suggestedUsers" :key="user.id">
            <img :src="user.avatar" alt="User Avatar">
            <span>{{ user.name }}</span>
            <button>Follow</button>
          </div>
        </div>
      </div>
      <div class="bottom-nav">
        <router-link to="/home">
          <i class="fa fa-envelope"></i>
        </router-link>
        <router-link to="/discover">
          <i class="fa fa-info"></i>
        </router-link>
        <router-link to="/settings">
          <i class="fa fa-cog"></i>
        </router-link>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        feedItems: [
          {
            id: 1,
            user: {
              name: 'John Doe',
              avatar: 'https://i.imgur.com/W8eJ0wI.png',
            },
            content: 'This is a sample post.',
          },
          // Add more feed items here
        ],
        suggestedUsers: [
          {
            id: 1,
            name: 'Jane Doe',
            avatar: 'https://i.imgur.com/W8eJ0wI.png',
          },
          // Add more suggested users here
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .feeds-page {
    display: flex;
    height: 100vh;
  }
  
  .sidebar {
    width: 200px;
    background-color: #222;
    color: #fff;
    padding: 20px;
  }
  
  .logo {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .logo img {
    width: 100px;
  }
  
  .sidebar-links {
    display: flex;
    flex-direction: column;
  }
  
  .sidebar-links a {
    color: #fff;
    text-decoration: none;
    padding: 10px;
    margin-bottom: 10px;
  }
  
  .sidebar-links a i {
    margin-right: 10px;
  }
  
  .content {
    flex: 1;
    padding: 20px;
  }
  
  .create-post {
    background-color: #f2f2f2;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
  }
  
  .create-post textarea {
    width: 100%;
    height: 100px;
    padding: 10px;
    border: none;
    resize: none;
  }
  
  .create-post button {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .feed-items {
    display: flex;
    flex-direction: column;
  }
  
  .feed-item {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
  }
  
  .user-info {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
  }
  
  .user-info img {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    margin-right: 10px;
  }
  
  .post-content {
    margin-bottom: 10px;
  }
  
  .post-actions {
    display: flex;
    justify-content: space-between;
  }
  
  .post-actions button {
    background-color: transparent;
    border: none;
    color: #007bff;
    cursor: pointer;
    margin-right: 10px;
  }
  
  .sidebar-title {
    text-align: center;
    margin-bottom: 20px;
  }
  
  .follow-button {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin-bottom: 20px;
  }
  
  .suggested-users {
    margin-bottom: 20px;
  }
  
  .suggested-user {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
  }
  
  .suggested-user img {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    margin-right: 10px;
  }
  
  .suggested-user button {
    background-color: #007bff;
    color: #fff;
    border: none;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .bottom-nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: #fff;
    padding: 10px;
  }
  
  .bottom-nav a {
    color: #007bff;
    text-decoration: none;
  }
  
  .bottom-nav a i {
    font-size: 24px;
  }
  </style>