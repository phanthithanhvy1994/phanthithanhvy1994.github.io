<template>
  <header>
    <div class="container header-container">
      <div class="logo-container">
        <img src="/logo.png" alt="Logo" />
        <h1>Vy Phan</h1>
      </div>
      <nav>
        <ul>
          <li><a href="#">Indie Game</a></li>
          <li><a href="#">Entry Game</a></li>
          <li><a href="#">Community</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
header {
  background-color: #2ecc71;
  position: fixed;
  width: 100%;
  top: 0;
  padding: 10px 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  z-index: 1;
  box-sizing: border-box;

  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap; /* Allow items to wrap */
  }

  .logo-container {
    display: flex;
    align-items: center;

    img {
      width: 50px;
      margin-right: 10px;
    }

    h1 {
      margin: 0;
      color: #fff;
    }
  }

  nav ul {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;

    li {
      margin-left: 20px;
    }

    a {
      padding: 5px 10px;
    }
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  .header-container {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo-container {
    margin-bottom: 10px;
  }

  nav ul {
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
  }

  nav ul li {
    margin-left: 0;
    margin-bottom: 10px;
  }

  nav ul li a {
    width: 100%;
    text-align: center;
  }
}
</style>
