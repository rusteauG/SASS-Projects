1)\_variables
$bg-image-cover:no-repeat center/cover;
$label-color:#ae81bf64;
$main-font:Branden Raulner;
$primary-font:'Roboto',sans-serif;
$gradient:linear-gradient(to left,#35d08f,#e32e64);

---

2)\_resets
\*{
margin:0;
padding:0;
box-sizing:border-box;
}

---

3)import in styles.scss
@import "./components/resets";
@import "./components/variables";
@import "./components/nav";
@import "./components/header";
@import "./components/about";
@import "./components/projects";
@import "./components/reviews";
@import "./components/footer";

---

4)Work on index.html , 3 li "ul>(li>a)\*4"

    <div class="container">
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
          <li><a href="#">Blog</a></li>

        </ul>
      </nav>
    </div>
    ---------------------------------------

5)\_nav.scss

.container {
height: 50vh;
background: linear-gradient(to right, #4f2d62, #ac39ea);
nav {
display: flex;
justify-content: flex-end;
font-family: $primary-font;
ul {
margin-right: 40px;
margin-top: 20px;
li {
display: inline;
list-style: none;
margin-left: 30px;
a {
text-decoration: none;
color: #fff;
}
}
}
}
}

---

6)index.html >frame section

<!-- frame-container -->

      <div class="frame-container">
        <div class="grdient">
          <header>
            <section class="social">
              <div class="line"></div>

              <i class="fa-brands fa-x-twitter"></i>
              <i class="fa-brands fa-youtube"></i>
              <i class="fa-brands fa-instagram"></i>

              <div class="line"></div>
            </section>

            <h1>
              Neville<br />
              Kalebi
            </h1>
          </header>
        </div>
      </div>
      -----------------------------
      7)_header.scss

