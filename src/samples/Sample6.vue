<template>
  <div class="body">
    <div class="bgImage"/>
    <div class="card">
      <div class="poster">
        <img src="../assets/img_film.jpg">
      </div>
      <div class="details">
        <h2>
          Beauty and the Beast (2017)
          <br>
          <span>Directed by Bill Condor</span>
        </h2>
        <div class="rating">
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="far fa-star"></i>
          <span>4/5</span>
        </div>
        <div class="tags">
          <span class="fantasy">Fantasy</span>
          <span class="romance">Romance</span>
        </div>
        <div class="info">
          <p>
            Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            Excepturi accusamus magni placeat autem quo. Rem obcaecati ...
          </p>
        </div>
        <div class="star">
          <h4>Cast</h4>
          <ul>
            <li>
              <img src="../assets/cast1.jpg">
            </li>
            <li>
              <img src="../assets/cast2.jpg">
            </li>
            <li>
              <img src="../assets/cast3.jpg">
            </li>
            <li>
              <img src="../assets/cast4.jpg">
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=PT+Sans');
.body {
  margin: 0;
  padding: 0;
  font-family: 'PT+Sans', sans-serif;
}
.bgImage {
  background: url('http://cineramaplus.com.ar/wp-content/uploads/2017/03/Beauty-and-the-Beast-2017-after-credits-hq-750x430.jpg');
  background-size: cover;
  filter: blur(8px);
  -webkit-filter: blur(8px);
  width: 100%;
  height: 100vh;
}
.card {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  height: 450px;
  background: #000;
  overflow: hidden;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.5);
}
.card .poster {
  position: relative;
  overflow: hidden;
}
.card .poster:before {
  content: '';
  position: absolute;
  bottom: -46%;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(0deg, #000 50%, transparent);
  z-index: 1;
  transition: 0.5s;
}
.card:hover .poster:before {
  bottom: 0;
}
.card .poster img {
  width: 100%;
  transition: 0.5s;
}
.card:hover .poster img {
  filter: blur(5px);
  transform: translateY(-50px);
}
.details {
  position: absolute;
  padding: 20px;
  width: 100%;
  height: 75%;
  bottom: -46%;
  left: 0;
  box-sizing: border-box;
  transition: 0.5s;
  z-index: 2;
}
.card:hover .details {
  bottom: 0;
}
.details h2 {
  color: #fff;
  margin: 0;
  padding: 0;
  font-size: 18px;
}
.details h2 span {
  font-size: 14px;
  color: #ff9800;
}
.rating {
  position: relative;
  padding: 5px 0;
}
.rating i {
  color: #f7f406;
  margin-right: 2px;
  font-size: 16px;
}
.rating span {
  color: #fff;
  padding: 0 5px;
}
.tags {
  position: relative;
  margin-top: 5px;
}
.tags span {
  padding: 2px 5px;
  margin-right: 2px;
  color: #fff;
  border-radius: 4px;
}
.tags span.fantasy {
  background: #7206f7;
}
.tags span.romance {
  background: #720661;
}
.info {
  color: #fff;
}
.info p {
  margin: 15px 0 10px;
}
.star {
  position: relative;
}
.star h4 {
  margin: 0;
  padding: 0;
  font-size: 20px;
  color: #f7f406;
}
.star ul {
  margin: 10px 0 0;
  padding: 0;
  display: flex;
}
.star ul li {
  list-style: none;
  padding: 0;
  width: 35px;
  height: 35px;
  background: #fff;
  border-radius: 50%;
  overflow: hidden;
  margin-right: 2px;
  border: 2px solid #fff;
}
.star ul li img {
  width: 100%;
}
</style>
