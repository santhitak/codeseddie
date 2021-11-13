<section style="height: auto;">
  <div class="container footer">
    <div class="listWrap">
      <p>made with curiousity</p>
      <p>&copy; All rights reserved 2021</p>
    </div>
  </div>
</section>

<style>
  p {
    font-size: 0.8rem;
    user-select: none;
  }
  .footer {
    height: 20vh;
  }
  .listWrap {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
  @media only screen and (max-width: 812px) {
    .listWrap {
      width: 100%;
      display: flex;
      flex-direction: column;
      text-align: center;
    }
    .footer {
      height: 15vh;
    }
  }
  @media only screen and (max-width: 1024px) {
    p{
      font-size: 1rem;
    }
    .footer {
      height: 10vh;
    }
  }
</style>
