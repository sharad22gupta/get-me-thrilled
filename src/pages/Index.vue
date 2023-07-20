<template>
  <q-page>
    <div class="container">
      <div class="content-container">
        <div class="animated-svg-bg" style="width: 100%">
          <div class="limit-container">
            <div class="animated-bg-text">
              <div class="w-100 heading-text">
                <span class="gradiant-text"> GetMeThrilled </span> - Your Smart
                Adventure Buddy
              </div>
              <div class="subheading-text q-mt-md">
                Unleash your inner adventurer and unlock exhilarating
                experiences. Embark on extraordinary journeys with our
                cutting-edge platform for booking adrenaline-packed adventures.
                Are you ready to take the leap?
              </div>
              <div class="w-100 q-mt-xl">
                <q-btn
                  label="Get Started"
                  no-caps
                  color="black"
                  to="/explore"
                  padding="10px 40px"
                  size="lg"
                  unelevated
                  class="toolbar-btn"
                  filled
                ></q-btn>
              </div>
            </div>
            <div class="svg-container">
              <q-img
                :src="getImgUrl('skydiver-top.png')"
                style="width: 500px"
                class="banner-img"
              ></q-img>
            </div>
          </div>
        </div>

        <div class="search-container">
          <div class="w-100 flex justify-center">
            <q-item clickable @click="scrollBottom()" class="mouse"></q-item>
          </div>
        </div>
        <div class="w-100 explore-wrapper" ref="target-div">
          <div class="collage-wrapper q-mb-xl">
            <div class="row space-between limit-container">
              <div class="gradiant-container">
                <q-img
                  class="collage-overlap hang-glider-img"
                  :src="getImgUrl('glider.png')"
                ></q-img>
              </div>
              <div class="collage-content">
                <div class="collage-heading">
                  Explore endless<br />
                  possibilities with
                  <span class="gradiant-text"> GMT </span>
                </div>
                <div class="collage-sub-heading q-mt-xl">
                  GMT provides a one stop solution for all adventure seekers and
                  sports enthusiasts by providing features like adventure
                  sports, activities booking, membership plans and more.<br /><br />
                  At it's core GMT is all about providing hassle-free bookings,
                  help train individuals and organisations, build great memories
                  and experiences with friends family and loved ones.
                </div>
                <!-- <q-btn
                class="gradiant-btn q-mt-xl"
                unelevated
                label="Get Started"
                padding="10px 40px"
                size="lg"
                no-caps
              ></q-btn> -->
              </div>
            </div>
          </div>
        </div>
        <div class="w-100 explore-wrapper bg-white">
          <div class="collage-wrapper q-mb-xl">
            <div class="row space-between limit-container-reverse">
              <div class="collage-content">
                <div class="collage-heading">
                  Why book with
                  <span class="gradiant-text"> GMT </span>
                </div>
                <div class="collage-sub-heading q-mt-xl">
                  Choose us for your next adventure and experience peace of mind
                  with our top-notch safety measures, verified reviews, and
                  expert guidance. With a wide selection, easy booking, and
                  transparent pricing, our 24/7 customer support ensures a
                  seamless journey.<br /><br />
                  Enjoy flexibility, a vibrant adventure community, and create
                  unforgettable memories.
                  <i>Your ultimate thrill awaits!</i>
                </div>
                <q-btn
                  class="gradiant-btn q-mt-xl"
                  unelevated
                  @click="showWhyUsers = true"
                  label="Know More"
                  padding="10px 40px"
                  size="lg"
                  no-caps
                ></q-btn>
              </div>
              <div class="gradiant-container">
                <q-img
                  class="collage-overlap paddle-surf"
                  :src="getImgUrl('paddle-surf.png')"
                ></q-img>
              </div>
            </div>
          </div>
        </div>
        <div class="w-100 explore-wrapper">
          <div class="collage-wrapper q-mb-xl">
            <div class="row space-between limit-container">
              <div class="gradiant-container">
                <q-img
                  class="collage-overlap skydiver"
                  :src="getImgUrl('skydiver-left.png')"
                ></q-img>
              </div>
              <div class="collage-content">
                <div class="collage-heading">
                  Why work with
                  <span class="gradiant-text"> GMT </span> - For adventure
                  sports provider
                </div>
                <div class="collage-sub-heading q-mt-xl">
                  Boost your adventure sports business by registering on our
                  platform. Expand your reach to a targeted audience of
                  adventure enthusiasts, leading to increased bookings and
                  enhanced visibility. Enjoy streamlined operations, access to
                  reviews, and exposure to new markets. Benefit from promotional
                  opportunities, networking, data insights, and become part of a
                  thriving adventure community.<br /><br />
                  By registering on our platform, adventure sports providers can
                  supercharge their business, gain exposure, and be part of an
                  ever-growing adventure community. Don't miss the opportunity
                  to thrive in the exhilarating world of adventure sports with
                  us!
                </div>
                <q-btn
                  class="gradiant-btn q-mt-xl"
                  unelevated
                  @click="showWhyProvider = true"
                  label="Know More"
                  padding="10px 40px"
                  size="lg"
                  no-caps
                ></q-btn>
              </div>
            </div>
          </div>
        </div>
        <div class="w-100 explore-wrapper bg-white">
          <div class="collage-wrapper row">
            <div class="collage-heading w-100 text-center q-mb-lg">
              Why adventure seekers love
              <span class="gradiant-text"> GetMeThrilled </span>
            </div>
            <div class="w-100 q-mt-xl">
              <div class="row space-between limit-container">
                <div class="gradiant-container">
                  <q-img
                    class="collage-overlap hang-glider-img"
                    :src="getImgUrl('hang-glide.png')"
                  ></q-img>
                </div>
                <div
                  data-aos="fade-up-left"
                  class="collage-content row q-px-xl"
                >
                  <div class="w-100 flex no-wrap">
                    <q-img
                      :src="getImgUrl('safety_money.png')"
                      style="width: 80px; height: 80px"
                    ></q-img>
                    <div class="benifit-content">
                      <div class="benifit-heading">Safe, Easy & Trusted</div>
                      <div class="benifit-sub-heading">
                        Your safety is our top priority, making the entire
                        process hassle-free and convenient.
                      </div>
                    </div>
                  </div>
                  <div class="w-100">
                    <q-separator class="q-mb-md" />
                    <div class="w-100 flex no-wrap">
                      <q-img
                        :src="getImgUrl('bot.png')"
                        style="width: 55px; height: 70px; margin-left: 15px"
                      ></q-img>
                      <div class="benifit-content">
                        <div class="benifit-heading">
                          Personalized Experience
                        </div>
                        <div class="benifit-sub-heading">
                          GMT uses cutting edge AI tech to suggest adventure
                          sports based on your choices and preferences.
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="w-100">
                    <q-separator class="q-mb-md" />
                    <div class="w-100 flex no-wrap">
                      <q-img
                        :src="getImgUrl('personalised-search.png')"
                        style="width: 80px; height: 80px"
                      ></q-img>
                      <div class="benifit-content">
                        <div class="benifit-heading">
                          Search from wide variety
                        </div>
                        <div class="benifit-sub-heading">
                          Discover a vast array of exhilarating activities and
                          destinations to choose from, catering to all levels of
                          adventurers, from beginners to seasoned pros.
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div data-aos="fade-up-right" class="w-100 mission-wrapper">
          <div class="collage-wrapper w-100">
            <div class="limit-container">
              <div class="our-mission">
                <div class="collage-heading text-white">
                  Our Mission with
                  <span class="gradiant-text"> GetMeThrilled </span>
                </div>
                <div class="collage-sub-heading q-mt-xl text-white">
                  At our platform, our mission is to ignite the spirit of
                  adventure in every soul by providing a seamless and
                  exhilarating platform for thrill-seekers to discover, book,
                  and experience extraordinary adventures worldwide.<br /><br />
                  We strive to connect adventure sports enthusiasts with
                  reputable providers, ensuring unparalleled safety, memorable
                  experiences, and boundless opportunities to push the
                  boundaries of their comfort zones. With unwavering dedication,
                  we aim to inspire a global community of adventurers, uniting
                  them through their shared passion for exploration, adrenaline,
                  and the transformative power of stepping into the unknown.<br /><br />
                  Together, we're on a mission to redefine adventure, unlocking
                  a world of endless possibilities and empowering individuals to
                  embark on journeys that leave them with indelible memories and
                  a profound sense of accomplishment.<br /><br />
                  Join us as we unleash the adventurer within and make every
                  heartbeat pulse with excitement on this exhilarating quest for
                  extraordinary experiences.
                </div>
                <!-- <q-btn
                class="gradiant-btn q-mt-xl"
                unelevated
                label="Join Us"
                padding="10px 40px"
                size="lg"
                no-caps
              ></q-btn> -->
              </div>
            </div>
          </div>
          <!-- <div class="w-100 text-white q-pa-xl q-mt-xl flex no-wrap">
            <q-img
              :src="getImgUrl('loudspeaker.png')"
              style="width: 200px"
            ></q-img>
            <span
              class="annuncement-content  collage-sub-heading text-white"
            >
              <span class="collage-heading text-white"
                >Our ChatUX API is coming soon!</span
              ><br /><br />
              With our API, you can integrate ChatUX into your own user
              experience and provide your customers with a more engaging and
              personalized search experience.<br /><br />
              Contact us to integrate Chat UX into your application</span
            >
          </div> -->
        </div>
      </div>
    </div>
    <q-dialog
      v-model="showWhyUsers"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card class="collage-sub-heading q-pa-lg" style="max-width: 800px">
        <q-card-section>
          <div class="collage-heading">
            Why book with
            <span class="gradiant-text"> GMT </span>
          </div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <ol>
            <li>
              <span class="text-bold text-black">Safety First:</span> Your
              safety is our top priority. We partner only with reputable and
              certified adventure providers to ensure every activity meets the
              highest safety standards.
            </li>
            <li>
              <span class="text-bold text-black">Verified Reviews:</span> Read
              genuine reviews from fellow thrill-seekers who have experienced
              our adventures firsthand, helping you make informed decisions.
            </li>
            <li>
              <span class="text-bold text-black">Expert Guidance:</span> Benefit
              from expert advice and personalized recommendations from our
              experienced team, ensuring you find the perfect adventure that
              matches your preferences and skill level.
            </li>
            <li>
              <span class="text-bold text-black">Wide Selection:</span> Discover
              a vast array of exhilarating activities and destinations to choose
              from, catering to all levels of adventurers, from beginners to
              seasoned pros.
            </li>
            <li>
              <span class="text-bold text-black">Easy Booking Process:</span>
              Our user-friendly platform allows you to book your dream adventure
              with just a few clicks, making the entire process hassle-free and
              convenient.
            </li>
            <li>
              <span class="text-bold text-black">Transparent Pricing:</span> No
              hidden costs or surprises. We provide transparent pricing for all
              our adventures, so you know exactly what you're paying for.
            </li>
            <li>
              <span class="text-bold text-black">24/7 Customer Support:</span>
              Have questions or need assistance? Our dedicated customer support
              team is available around the clock to help you at every step of
              your adventure journey.
            </li>
            <li>
              <span class="text-bold text-black">Flexibility and Refunds:</span>
              Life can be unpredictable, and we understand that. Enjoy flexible
              booking options and hassle-free refund policies for added peace of
              mind.
            </li>
            <li>
              <span class="text-bold text-black">Adventure Community:</span>
              Join a vibrant community of like-minded adventure enthusiasts,
              share stories, and connect with fellow travelers who share your
              passion for thrill-seeking.
            </li>
            <li>
              <span class="text-bold text-black">Memorable Experiences:</span>
              We're committed to curating unforgettable adventures that create
              lasting memories, leaving you with stories to share for a
              lifetime.
            </li>
          </ol>
          Book with us and embark on a journey filled with adrenaline,
          excitement, and unforgettable moments. Your adventure of a lifetime
          awaits!
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="Close" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    <q-dialog
      v-model="showWhyProvider"
      transition-show="rotate"
      transition-hide="rotate"
    >
      <q-card class="collage-sub-heading q-pa-lg" style="max-width: 800px">
        <q-card-section>
          <div class="collage-heading">
            Why work with
            <span class="gradiant-text"> GMT </span>
          </div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <ol>
            <li>
              <span class="text-bold text-black"> Expanded Reach:</span> By
              registering on our platform, adventure sports providers can tap
              into a larger audience of adventure enthusiasts actively seeking
              thrilling experiences, expanding their reach beyond their current
              marketing efforts.
            </li>
            <li>
              <span class="text-bold text-black"> Targeted Audience: </span>Our
              platform caters specifically to adventure seekers, ensuring that
              adventure sports providers connect with their ideal target
              audience, increasing the chances of converting potential customers
              into bookings.
            </li>
            <li>
              <span class="text-bold text-black"> Increased Bookings:</span>
              With our established user base and marketing efforts, adventure
              sports providers can expect a steady stream of bookings, helping
              them maximize their business potential and revenue.
            </li>
            <li>
              <span class="text-bold text-black"> Enhanced Visibility:</span>
              Being featured on our platform enhances the visibility and
              credibility of adventure sports providers, as users trust our
              carefully curated selection of activities and destinations.
            </li>
            <li>
              <span class="text-bold text-black">
                Access to Reviews and Feedback:</span
              >
              Our platform allows adventure sports providers to receive valuable
              feedback and reviews from customers, providing insights for
              improvement and boosting their reputation based on positive
              experiences.
            </li>
            <li>
              <span class="text-bold text-black"> Streamlined Operations:</span>
              Our user-friendly booking system simplifies the reservation
              process, making it easy for adventure sports providers to manage
              bookings, availability, and customer inquiries efficiently.
            </li>
            <li>
              <span class="text-bold text-black">
                Exposure to New Markets:</span
              >
              Registering on our platform opens doors to new markets and
              demographics, attracting adventure enthusiasts from different
              regions and backgrounds.
            </li>
            <li>
              <span class="text-bold text-black">
                Promotional Opportunities:</span
              >
              Adventure sports providers can take advantage of promotional
              opportunities and special offers on our platform, further
              incentivizing potential customers to choose their services.
            </li>
            <li>
              <span class="text-bold text-black">
                Networking and Collaboration:</span
              >
              Joining our platform allows adventure sports providers to network
              and collaborate with other industry professionals, fostering
              potential partnerships and business growth.
            </li>
            <li>
              <span class="text-bold text-black"> Data Insights:</span>
              Adventure sports providers gain access to valuable data and
              analytics, enabling them to understand customer preferences,
              trends, and demand, leading to more informed business decisions.
            </li>
          </ol>
          By registering on our platform, adventure sports providers can
          supercharge their business, gain exposure, and be part of an
          ever-growing adventure community. Don't miss the opportunity to thrive
          in the exhilarating world of adventure sports with us!
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="Close" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script>
import mixin from 'src/mixins/mixin.js';

export default {
  name: 'PageIndex',
  data() {
    return {
      showWhyUsers: false,
      showWhyProvider: false,
    };
  },
  mixins: [mixin],
  methods: {
    scrollBottom() {
      this.$refs['target-div'].scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>
<style lang="scss">
.banner-img {
  animation-name: floating;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}
@keyframes floating {
  0% {
    transform: translate(0, 0px);
  }
  50% {
    transform: translate(0, 15px);
  }
  100% {
    transform: translate(0, -0px);
  }
}
.mouse {
  width: 50px;
  height: 90px;
  border: 1px solid rgb(165, 165, 165);
  border-radius: 60px;
  position: relative;
  &::before {
    content: '';
    width: 12px;
    height: 12px;
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgb(165, 165, 165);
    border-radius: 50%;
    opacity: 1;
    animation: wheel 2s infinite;
    -webkit-animation: wheel 2s infinite;
  }
}
@keyframes wheel {
  to {
    opacity: 0;
    top: 60px;
  }
}

@-webkit-keyframes wheel {
  to {
    opacity: 0;
    top: 60px;
  }
}
</style>
<style scoped>
.limit-container,
.limit-container-reverse {
  max-width: 1500px;
  margin: auto;
  position: relative;
}
.benifit-content {
  width: calc(100% - 80px);
}
.annuncement-content {
  width: calc(100% - 250px);
}
.benifit-heading {
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 500;
  font-size: 25px;
  line-height: 129.7%;
  /* identical to box height, or 39px */

  text-transform: capitalize;

  color: #212326;
  padding-left: 20px;
}
.benifit-sub-heading {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  /* or 29px */
  margin-top: 10px;
  padding-left: 20px;

  color: #797979;
}
.collage-sub-heading {
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 1.4;
  color: #797979;
}
.explore-wrapper {
  padding: 100px;
  background: rgba(234, 238, 241, 0.55);
}
.mission-wrapper {
  background-color: #263238;
  padding: 100px;
  /* background-image: url('../assets/mission-bg.png'); */
  background-repeat: no-repeat;
  background-size: cover;
  background-position: bottom;
}

.collage-wrapper {
  width: 100%;
  display: flex;
  justify-content: space-between;
}
.collage-heading {
  font-size: 40x;
  font-weight: 600;
  font-family: 'Ubuntu';
  font-style: normal;
  font-weight: 700;
  font-size: 40px;
  line-height: 129.7%;
  color: #212326;
}
.collage-container {
  width: 50%;
  border-radius: 10px;
  overflow: hidden;
}
.gradiant-container {
  width: 50%;
  max-width: 550px;
  min-height: 400px;
  border-radius: 10px;
  position: relative;
  background: url('../assets/Background.png');
  background-repeat: no-repeat;
  background-size: contain;
  background-position: top;
}
.animated-svg-bg {
  width: 100%;
  height: 100vh;
  max-height: 800px;
  background: url('../assets/animated-bg.svg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top;
}
.collage-overlap {
  width: 300px;
  height: auto;
  position: absolute;
  top: 10px;
  border-radius: 10px;
  left: 0;
  right: 0;
  margin: auto;
  animation-name: floating;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}
.notepad-overlap {
  width: 100%;
  height: auto;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
}
.collage-content {
  padding-left: 24px;
  width: 50%;
}
.container {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  background: white;
  font-family: 'Poppins';
}
.bottom-div {
  width: 100%;
  max-width: 1000px;
  height: auto;
  margin: auto;
}
.search-bar {
  background: #eef3ff;
  color: #a3aed0;
  border-radius: 8px;
  padding: 10px 20px;
  font-size: 15px;
  align-items: center;
  box-shadow: 0 2px 4px rgba(45, 35, 66, 0.35),
    0 7px 13px -3px rgba(45, 35, 66, 0.25);
  transition: transform 0.2s ease-out, box-shadow 0.2s ease-out;
}
.search-bar:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px 0 rgba(45, 35, 66, 0.4),
    0 4px 18px 0 rgba(45, 35, 66, 0.3);
}
.animated-bg-text {
  width: 50%;
  padding: 0 50px 0 100px;
  text-align: left;
  height: 80vh;
  max-height: 800px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.svg-container {
  width: 50%;
  position: absolute;
  right: 0;
  top: 0;
  display: flex;
  height: 70vh;
  justify-content: center;
  align-items: center;
}
.search-container {
  width: 200px;
  height: auto;
  border-radius: 10px;
  background: transparent;
  margin: auto;
  padding: 20px;
  left: 0;
  right: 0;
  margin-top: -200px;
  position: absolute;
  cursor: pointer;
}
.featured-container {
  width: 100%;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  display: grid;
  column-gap: 20px;
  row-gap: 20px;
}
.heading-text {
  font-weight: 700;
  font-size: 60px;
  line-height: 129.7%;
  text-transform: capitalize;
  font-family: 'Ubuntu';
  color: #212326;
}
.gradiant-text {
  background: linear-gradient(
    103.93deg,
    rgba(51, 226, 255, 1) 10.35%,
    rgba(106, 147, 255, 1) 49.75%,
    rgba(253, 95, 178, 1) 90.17%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-fill-color: transparent;
}
.content-holder {
  display: flex;
  column-gap: 20px;
  margin-top: 100px;
}
.trending-heading {
  font-family: 'Poppins';
  font-weight: 600;
  font-size: 20px;
  line-height: 160%;
}
.subheading-text {
  font-weight: 400;
  font-size: 20px;
  line-height: 160%;
  /* or 26px */

  text-transform: capitalize;

  color: #797979;
}
.hang-glider-img {
  width: 550px !important;
  top: 100px !important;
}
.paddle-surf {
  width: 400px !important;
  top: 70px !important;
}

@media (max-width: 900px) {
  .content-holder {
    flex-direction: column;
  }
  .animated-svg-bg {
    height: auto;
  }
  .animated-bg-text {
    width: 100%;
    padding: 20px;
    text-align: left;
    height: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .heading-text {
    font-size: 30px;
  }
  .subheading-text {
    font-size: 16px;
  }
  .search-container,
  .svg-container {
    display: none;
  }
  .limit-container {
    display: flex;
    flex-direction: column;
  }
  .gradiant-container {
    width: 100%;
  }
  .explore-wrapper {
    padding: 20px;
  }
  .hang-glider-img {
    width: 300px !important;
    top: 10px !important;
  }
  .gradiant-container {
    min-height: 300px;
  }
  .collage-content {
    width: 100%;
    padding-left: 0;
    padding-right: 0;
  }
  .limit-container-reverse {
    display: flex;
    flex-direction: column-reverse;
  }
  .collage-heading {
    font-size: 30px;
  }
  .collage-sub-heading {
    font-size: 16px;
  }
  .paddle-surf {
    width: 200px !important;
    top: 0 !important;
  }
  .skydiver {
    width: 150px !important;
    top: 0 !important;
  }
  .benifit-heading {
    padding-left: 10px;
    font-size: 20px;
  }
  .benifit-sub-heading {
    padding-bottom: 20px;
    padding-left: 10px;
  }
  .mission-wrapper {
    padding: 20px;
  }
}
</style>
