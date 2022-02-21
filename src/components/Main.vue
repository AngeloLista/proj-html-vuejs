<template>
  <main>
    <!-- Pro Barbers -->
    <section id="pro-barbers" class="d-flex flex-column align-items-center">
      <!-- Section text -->
      <div class="content text-center">
        <SectionTitle title="Pro Barbers" description="award winning" />
        <ButtonLink text="meet your new barber" />
      </div>
      <!-- Triangle Sepator -->
      <div class="triangle-separetor"></div>
    </section>

    <!-- Services -->
    <section id="services">
      <!-- Title -->
      <div class="content d-flex flex-column align-items-center py-5">
        <SectionTitle title="Services" description="mens grooming" />
        <div class="cards-container container d-flex align-items-center">
          <!-- Card -->
          <ServiceCard
            v-for="(service, index) in services"
            :key="index"
            :name="service.name"
            :text="service.text"
            :imgUrl="service.imgUrl"
          />
        </div>
        <ButtonLink text="read about our services" />
      </div>
      <div class="triangle-separetor"></div>
    </section>

    <!-- Products -->
    <section id="products">
      <div class="content d-flex flex-column align-items-center pt-5">
        <!-- Title -->
        <SectionTitle
          title="Avada Grooming Products"
          description="we have you covered"
        />
        <div class="cards-container container d-flex align-items-center mb-5">
          <!-- Card -->
          <ProductCard
            v-for="(product, index) in products"
            :key="index"
            :name="product.name"
            :price="product.price"
            :imgUrl="product.imgUrl"
          />
        </div>
        <ButtonLink text="shop our product range" />
      </div>
    </section>

    <!-- Featured Product -->
    <section id="featured" class="container w-75">
      <div class="row">
        <div id="featured-product-img" class="col-4 d-flex align-items-center">
          <img
            src="../assets/img/shaving_butter.png"
            alt=""
            class="img-fluid"
          />
        </div>
        <div class="col-8 p-5">
          <!-- Title -->
          <span>this month featured product</span>
          <h2>Shaving Butter</h2>
          <p class="text-muted">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam
            provident perferendis dolorum non. Ipsum placeat fugit minima quas
            inventore? Perspiciatis sit similique quis voluptates molestiae
            minus ducimus id quia dolores.
          </p>
          <ButtonLink text="buy now" />
        </div>
      </div>
    </section>

    <!-- Reviews -->
    <section id="reviews" class="container w-75 py-5">
      <SectionTitle title="Reviews" description="what people say" />
      <div class="row">
        <!-- Review -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <p class="text-muted text-center">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam
            aliquid rerum pariatur quisquam, deserunt autem culpa quis in alias
            magnam perspiciatis placeat necessitatibus impedit sit quo
            perferendis non totam doloremque.
          </p>
          <img
            class="img-fluid my-3"
            src="../assets/img/avadabarbers-trimcut-gallery6.jpg"
            alt="John Doe"
          />
          <h5>John Doe</h5>
        </div>
        <!-- Review -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <p class="text-muted text-center">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam
            aliquid rerum pariatur quisquam, deserunt autem culpa quis in alias
            magnam perspiciatis placeat necessitatibus impedit sit quo
            perferendis non totam doloremque.
          </p>
          <img
            class="img-fluid my-3"
            src="../assets/img/avadabarbers-trimcut-gallery7.jpg"
            alt="Pete Jones"
          />
          <h5>Pete Jones</h5>
        </div>
        <!-- Review -->
        <div class="col-4 p-3 d-flex align-items-center flex-column">
          <p class="text-muted text-center">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quam
            aliquid rerum pariatur quisquam, deserunt autem culpa quis in alias
            magnam perspiciatis placeat necessitatibus impedit sit quo
            perferendis non totam doloremque.
          </p>
          <img
            class="img-fluid my-3"
            src="../assets/img/avadabarbers-trimcut-gallery3.jpg"
            alt="Mark Wilson"
          />
          <h5>Mark Wilson</h5>
        </div>
      </div>
    </section>

    <!-- Recent Blog Posts -->
    <section id="blog">
      <div class="triangle-separetor top-white"></div>
      <div
        class="container w-75 py-5 mt-5 d-flex flex-column align-items-center"
      >
        <SectionTitle
          title="Recent Blog Posts"
          description="tales from the barber shop"
        />
        <div class="row">
          <div class="col-4 p-3 d-flex align-items-center flex-column">
            <BlogPostCard
              :title="this.posts[0].title"
              :imgUrl="this.posts[0].imgUrl"
            />
          </div>
          <div class="col-4 p-3 d-flex align-items-center flex-column">
            <BlogPostCard
              :title="this.posts[1].title"
              :imgUrl="this.posts[1].imgUrl"
            />
          </div>
          <div class="col-4 p-3 d-flex align-items-center flex-column">
            <BlogPostCard
              :title="this.posts[2].title"
              :imgUrl="this.posts[2].imgUrl"
            />
          </div>
        </div>
        <div class="my-5">
          <ButtonLink text="read more from our blog" />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import ButtonLink from "./ButtonLink.vue";
import ServiceCard from "./Main/ServiceCard.vue";
import ProductCard from "./Main/ProductCard.vue";
import SectionTitle from "./Main/SectionTitle.vue";
import BlogPostCard from "./Main/BlogPostCard.vue";

export default {
  name: "Main",
  components: {
    ButtonLink,
    ServiceCard,
    ProductCard,
    SectionTitle,
    BlogPostCard,
  },
  props: ["services", "products", "posts"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_utils.scss";

main {
  font-family: $lato;
  // Pro Barbers
  #pro-barbers {
    background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
    background-size: cover;
    .content {
      padding: 100px 0;
    }
    .triangle-separetor {
      width: 0;
      height: 0;
      line-height: 0;
      border-bottom: 100px solid white;
      border-left: 49.39vw solid transparent;
      border-right: 49.39vw solid transparent;
    }
  }
  // Services
  #services {
    // Title
    .content {
      height: 100vh;
    }
    .triangle-separetor {
      width: 0;
      height: 0;
      line-height: 0;
      border-bottom: 100px solid #121315;
      border-left: 49.39vw solid transparent;
      border-right: 49.39vw solid transparent;
    }
    // Card
    .cards-container {
      margin-bottom: 50px;
      .service-card {
        height: 300px;
        width: calc(100% / 3);
        padding: 30px 70px;
        img {
          margin-bottom: 30px;
          height: 35%;
        }
        h3 {
          font-family: $abril;
          color: $driftwood;
          margin-bottom: 30px;
          padding: 0 15px;
        }
        p {
          text-align: center;
        }
      }
    }
  }
  // Products
  #products {
    background-image: url("../assets/img/avadabarbers-reviewsbackground.jpg");
    background-size: cover;
    padding-bottom: 150px;
  }
  // Featured Product
  #featured {
    background-color: $cod-gray;
    border-top: 6px solid $driftwood;
    margin-top: -35px;
    margin-bottom: 70px;
    span {
      color: $driftwood;
      font-weight: bold;
      display: block;
      text-transform: uppercase;
    }
    h2 {
      font-family: $abril;
      font-size: 70px;
      color: $silver-chalice;
      margin-bottom: 3rem;
    }
    p {
      padding-right: 30px;
      margin-bottom: 50px;
    }
    #featured-product-img {
      background-image: url("../assets/img/avadabarbers-cta-background.jpg");
      background-size: cover;
      img {
        object-fit: contain;
      }
    }
  }
  // Reviews
  #reviews {
    img {
      border-radius: 50%;
      width: 30%;
    }
    h5 {
      color: $driftwood;
      font-style: italic;
      font-weight: bold;
    }
  }
  // Traingle Separetor
  .triangle-separetor {
    width: 0;
    height: 0;
    line-height: 0;
    border-left: 49.39vw solid transparent;
    border-right: 49.39vw solid transparent;
    &.top-white {
      border-top: 100px solid white;
    }
  }
  // Recent Blog Posts
  #blog {
    background-color: $recent-blog-bg;
    a {
      text-decoration: none;
    }
    h3 {
      color: $driftwood;
      font-family: $abril;
      text-align: center;
      margin-bottom: 15px;
    }
  }
}
</style>