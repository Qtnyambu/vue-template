<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-top">
        <h2>My Website</h2>
        <nav>
          <ul class="footer-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
      </div>

      <div class="footer-bottom">
        <p>© {{ new Date().getFullYear() }} My Website. All Rights Reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style scoped>
.footer {
  background: #333;
  color: white;
  padding: 20px 0;
  text-align: center;
}
.container {
  max-width: 1200px;
  margin: auto;
  padding: 0 20px;
}
.footer-top {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.footer-bottom {
  margin-top: 12px;
}
.footer-links {
  list-style: none;
  padding: 0;
  display: flex;
  gap: 15px;
  margin-top: 10px;
}
.footer-links li a {
  color: white;
  text-decoration: none;
}
</style>
