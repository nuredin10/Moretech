<template>
  <div class="body-main">
    <HeaderPages :src="src" headline="Contact Us" />

    <section class="contact-info">
      <img class="decor" src="../assets/Icons/decor.svg" alt="" />

      <div class="container">
        <div class="contact-hour">
          <h4>Contact hour</h4>
          <div class="desc">
            <p>
              MoreTech is a company that imports and distributes laboratory
              equipment, materials, and chemicals. In each area, our suppliers
              provide the finest prices and well-known brands, allowing us to be
              a trusted and reliable extension of our clients.
            </p>
          </div>
        </div>
        <div class="contactinfo">
          <h4>Contact Information</h4>
          <div class="desc">
            <p>
              Use the links below to contact us through our social media
              platforms.
            </p>
            <!-- <p><a href="">https://www.facebook.com</a></p>
            <p><a href="">https://www.youtube.com</a></p>
            <p><a href="">https://www.linkedin.com</a></p>
            <p><a href="">https://www.googleplus.com</a></p> -->
            <p>
              Yeka subsicty,wereda 07,COMOROS AVE B78.32 Kebena, opposite to the
              Kenya Embassy
            </p>
          </div>
        </div>
      </div>
    </section>
    <ContactApp />
    <section class="map">
      <h1 class="map-title text-center"></h1>
      <div class="map-container">
        <div class="location">
          <div class="map-responsive">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.3454806684717!2d38.78044861533832!3d9.032215191424143!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x164b8fbd21b0901b%3A0x8b85b87620e90d53!2sMoretech%20industry%20PLC%2C%20Ethiopia!5e0!3m2!1sen!2sru!4v1665126860490!5m2!1sen!2sru"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
            ></iframe>
          </div>
        </div>
      </div>
    </section>
    <FooterApp />
  </div>
</template>
<script>
import AOS from "aos";
import "aos/dist/aos.css";
import HeaderPages from "../components/HeaderPages.vue";
export default {
  components: {
    HeaderPages,
  },
  data() {
    return {
      src: require("../assets/Images/contact.jpg"),
    };
  },
  mounted() {
    AOS.init({
      duration: 900,
      offset: 120,
      easing: "ease",
      once: false,
      anchorPlacement: "top-bottom",
    });
  },
};
</script>

<style lang="scss">
.body-main {
  .contact-info {
    margin-top: 8rem;
    .decor {
      position: absolute;
      width: 90rem;
      height: 50rem;
      object-fit: cover;
      z-index: -1;
    }
    .container {
      .contact-hour {
        margin-top: 3rem;
        border: 2px solid $M-blue;
        padding: 1rem;
        position: relative;
        h4 {
          background: $M-white;

          padding: 0.4rem;
          width: 10rem;
          margin-top: -2.3rem;
          margin-left: 1rem;
          color: $M-red;
          @extend .h3;
          font-size: 0.9rem;

          line-height: 1.3rem;
          font-weight: 600;
          text-align: left;
        }
        .desc {
          p {
            margin-left: 1rem;
            color: $M-blue;
            @extend .title;
            font-size: 0.9rem;
            margin-top: 0.94rem;
            line-height: 1.3rem;
            text-align: center;
          }
        }
      }
      .contactinfo {
        margin-top: 3rem;
        border: 2px solid $M-blue;
        padding: 1rem;
        position: relative;
        h4 {
          background: $M-white;

          padding: 0.4rem;
          width: 10rem;
          margin-top: -2.3rem;
          margin-left: 1rem;
          color: $M-red;
          @extend .h3;
          font-size: 0.9rem;

          line-height: 1.3rem;
          font-weight: 600;
          text-align: left;
        }
        .desc {
          p {
            margin-left: 1rem;
            color: $M-blue;
            @extend .title;
            font-size: 0.9rem;
            margin-top: 0.94rem;
            line-height: 1.3rem;
            text-align: center;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .contact-info {
      .container {
        display: flex;
        gap: 2rem;
        .contact-hour {
          padding: 3rem;
          h4 {
            padding: 0.6rem;

            margin-top: -4.5rem;
          }
          .desc {
            p {
              margin-top: 2rem;
            }
          }
        }
        .contactinfo {
          padding: 3rem;
          h4 {
            padding: 0.6rem;

            margin-top: -4.5rem;
          }
          .desc {
            p {
              margin-top: 2rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .contact-info {
      .container {
        display: flex;
      }
    }
  }
  .map {
    margin-top: 8rem;
    overflow: hidden;
    // padding-bottom: 5.06rem;
    // height: 31.94rem;
    .map-container {
      .location {
        .map-responsive {
          overflow: hidden;
          // padding-bottom: 56.25%;
          position: relative;
          height: 18rem;
          max-height: 50.94rem;
          iframe {
            left: 0;
            top: 0;
            height: 100%;
            width: 100%;
            position: absolute;
          }
        }
      }
    }
  }
  // @include responsive($lg) {
  //   height: 81.94rem;
  // }
}
</style>
