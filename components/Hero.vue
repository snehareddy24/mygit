 <template>
    <div class="container">
    <nav class="navbar navbar-light bg-dark">
        <div class="container-fluid">
            <button class="btn btn-danger" data-bs-toggle="modal" data-bs-target="#loginModal" @click="showModal">LOG IN</button>
        </div>
    </nav>
    <Modal 
        v-show="isModalVisible" 
        @close="closeModal"
    />
    <div class="main-banner" id="top">
        <img src="~/assets/images/1.jpg" id="bg-video" alt="">

        <div class="video-overlay header-text">
            <div class="caption">
                <h6>WATCH THOUSANDS OF TV SHOWS AND MOVIES. HBO MAX™, SHOWTIME®, CINEMAX® AND STARZ® AVAILABLE AS ADD-ONS.</h6>
                <h2>STREAMX</h2>
                <div class="main-button scroll-to-section">
                       <nuxt-link to="/about-us"><button style="background-color:crimson;color: cornsilk;"><h3>Find your FREE trail</h3></button></nuxt-link>
                </div>
            </div>
        </div>
    </div>
    
    <section class="py-5 text-center container">
        <div class="row py-lg-5">
            <div class="col-lg-6 col-md-8 mx-auto">
                <h1 class="fw-light">ALL THE TV YOU LOVE</h1>
                <p class="lead text-muted">Stream full seasons of exclusive series, current-season episodes, hit movies, Hulu Originals, kids shows, and more.</p>
            </div>
        </div>
    </section>
     </div>
 </template>
 
 <script>
 import Modal from './Modal.vue';
     
     export default {
        name:'Hero',
        data:function(){
            return{
                isModalVisible: false
            }
        },
        methods:{
            showModal(){
                this.isModalVisible = true;
            },
            closeModal(){
                this.isModalVisible = false
            }
        },
        components:{Modal},
     }
 </script>
 <style scoped>
  .main-banner {
               position: relative;
           }
           
           #bg-video {
               min-width: 100%;
               min-height: 100vh;
               max-width: 100%;
               max-height: 100vh;
               object-fit: cover;
               z-index: -1;
           }
           
           #bg-video::-webkit-media-controls {
               display: none !important;
           }
           
           .video-overlay {
               position: absolute;
               background-color: rgba(35, 45, 57, 0.8);
               top: 0;
               left: 0;
               bottom: 7px;
               width: 100%;
           }
           
           .main-banner .caption {
               text-align: center;
               position: absolute;
               width: 80%;
               left: 50%;
               top: 50%;
               transform: translate(-50%, -50%);
           }
           
           .main-banner .caption h6 {
               margin-top: 0px;
               font-size: 13px;
               text-transform: uppercase;
               font-weight: 800;
               color: #fff;
               letter-spacing: 0.5px;
           }
           
           .main-banner .caption h2 {
               margin-top: 30px;
               margin-bottom: 25px;
               font-size: 40px;
               text-transform: uppercase;
               font-weight: 800;
               color: #fff;
               letter-spacing: 1px;
           }
           
           .main-banner .caption h2 em {
               font-style: normal;
               color: #ed563b;
               font-weight: 900;
           }
 </style>