<template>
  <div id="footer">
    <footer class="footer">
      <div class="container">
        <div class="content has-text-centered">
          <p>
            <strong>Blog</strong> by <a href="https://frozencreeks.com">Jeremy Barr</a>.
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
  footer.footer {
      margin-top: 10rem;
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
      background-color: #209cee;
  }
  .footer p,
  .footer strong{
    color: #ffffff;
  }
  .footer a:link,
  .footer a:visited {
    text-decoration: none;
    border: 0;
    color: #ffffff;
    transition: color 0.2s;
  }
  .footer a:hover,
  .footer a:active {
    border-bottom: 2px solid #ffffff;
}
</style>
