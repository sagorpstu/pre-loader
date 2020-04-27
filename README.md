# pre-loader
Pre-Loader Before Webpage Appears.


<-------------HTML-------------->

     <!-- preloader  -->
        <div id="preloader">
            <div id="ctn-preloader" class="ctn-preloader">
                <div class="animation-preloader">
                    <div class="spinner"></div>
                    <div class="txt-loading">
                         <span data-text-preloader="F." class="letters-loading">
                            F.
                        </span>
                         <span data-text-preloader="H." class="letters-loading">
                            H. 
                        </span>
                        
                        <span data-text-preloader="S" class="letters-loading">
                            S
                        </span>
                        <span data-text-preloader="A" class="letters-loading">
                            A
                        </span>
                        <span data-text-preloader="G" class="letters-loading">
                            G
                        </span>
                        <span data-text-preloader="O" class="letters-loading">
                            O
                        </span>
                        <span data-text-preloader="R" class="letters-loading">
                            R
                        </span>
                    </div>
                </div>
                <div class="loader">
                    <div class="row">
                        <div class="col-3 loader-section section-left">
                            <div class="bg"></div>
                        </div>
                        <div class="col-3 loader-section section-left">
                            <div class="bg"></div>
                        </div>
                        <div class="col-3 loader-section section-right">
                            <div class="bg"></div>
                        </div>
                        <div class="col-3 loader-section section-right">
                            <div class="bg"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- preloader end -->

<-------------HTML-------------->



<-------------CSS-------------->


/* Preloader */
.ctn-preloader {
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  cursor: default;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  height: 100%;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  z-index: 9000;
}

.ctn-preloader .animation-preloader {
  z-index: 1000;
}

.ctn-preloader .animation-preloader .spinner {
  -webkit-animation: spinner 1s infinite linear;
  animation: spinner 1s infinite linear;
  border-radius: 50%;
  border: 3px solid rgba(0, 0, 0, 0.2);
  border-top-color: #FF5B5B;
  height: 150px;
  margin: 0 auto 3.5em auto;
  width: 150px;
}

.ctn-preloader .animation-preloader .txt-loading {
  font: bold 5em "Poppins", sans-serif;
  text-align: center;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading {
  color: rgba(0, 0, 0, 0.2);
  position: relative;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:before {
  -webkit-animation: letters-loading 4s infinite;
  animation: letters-loading 4s infinite;
  color: #000000;
  content: attr(data-text-preloader);
  left: 0;
  opacity: 0;
  font-family: "Poppins", sans-serif;
  position: absolute;
  top: -3px;
  -webkit-transform: rotateY(-90deg);
  transform: rotateY(-90deg);
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(2):before {
  -webkit-animation-delay: 0.2s;
  animation-delay: 0.2s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(3):before {
  -webkit-animation-delay: 0.4s;
  animation-delay: 0.4s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(4):before {
  -webkit-animation-delay: 0.6s;
  animation-delay: 0.6s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(5):before {
  -webkit-animation-delay: 0.8s;
  animation-delay: 0.8s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(6):before {
  -webkit-animation-delay: 1s;
  animation-delay: 1s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(7):before {
  -webkit-animation-delay: 1.2s;
  animation-delay: 1.2s;
}

.ctn-preloader .animation-preloader .txt-loading .letters-loading:nth-child(8):before {
  -webkit-animation-delay: 1.4s;
  animation-delay: 1.4s;
}

.ctn-preloader.dark .animation-preloader .spinner {
  border-color: rgba(255, 255, 255, 0.2);
  border-top-color: #fff;
}

.ctn-preloader.dark .animation-preloader .txt-loading .letters-loading {
  color: rgba(255, 255, 255, 0.2);
}

.ctn-preloader.dark .animation-preloader .txt-loading .letters-loading:before {
  color: #fff;
}

.ctn-preloader p {
  font-size: 14px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 8px;
  color: #3b3b3b;
}

.ctn-preloader .loader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  font-size: 0;
  z-index: 1;
  pointer-events: none;
}

.ctn-preloader .loader .row {
  height: 100%;
}

.ctn-preloader .loader .loader-section {
  padding: 0px;
}

.ctn-preloader .loader .loader-section .bg {
  background-color: #ffffff;
  height: 100%;
  left: 0;
  width: 100%;
  -webkit-transition: all 800ms cubic-bezier(0.77, 0, 0.175, 1);
  -o-transition: all 800ms cubic-bezier(0.77, 0, 0.175, 1);
  transition: all 800ms cubic-bezier(0.77, 0, 0.175, 1);
}

.ctn-preloader .loader.dark_bg .loader-section .bg {
  background: #111339;
}

.ctn-preloader.loaded .animation-preloader {
  opacity: 0;
  -webkit-transition: 0.3s ease-out;
  -o-transition: 0.3s ease-out;
  transition: 0.3s ease-out;
}

.ctn-preloader.loaded .loader-section .bg {
  width: 0;
  -webkit-transition: 0.7s 0.3s allcubic-bezier(0.1, 0.1, 0.1, 1);
  -o-transition: 0.7s 0.3s allcubic-bezier(0.1, 0.1, 0.1, 1);
  transition: 0.7s 0.3s allcubic-bezier(0.1, 0.1, 0.1, 1);
}

@-webkit-keyframes spinner {
  to {
    -webkit-transform: rotateZ(360deg);
    transform: rotateZ(360deg);
  }
}

@keyframes spinner {
  to {
    -webkit-transform: rotateZ(360deg);
    transform: rotateZ(360deg);
  }
}

@-webkit-keyframes letters-loading {
  0%,
  75%,
  100% {
    opacity: 0;
    -webkit-transform: rotateY(-90deg);
    transform: rotateY(-90deg);
  }
  25%,
  50% {
    opacity: 1;
    -webkit-transform: rotateY(0deg);
    transform: rotateY(0deg);
  }
}

@keyframes letters-loading {
  0%,
  75%,
  100% {
    opacity: 0;
    -webkit-transform: rotateY(-90deg);
    transform: rotateY(-90deg);
  }
  25%,
  50% {
    opacity: 1;
    -webkit-transform: rotateY(0deg);
    transform: rotateY(0deg);
  }
}

@media screen and (max-width: 767px) {
  .ctn-preloader .animation-preloader .spinner {
    height: 8em;
    width: 8em;
  }
  .ctn-preloader .animation-preloader .txt-loading {
    font: bold 3.5em "Poppins", sans-serif;
  }
}

@media screen and (max-width: 500px) {
  .ctn-preloader .animation-preloader .spinner {
    height: 7em;
    width: 7em;
  }
  .ctn-preloader .animation-preloader .txt-loading {
    font: bold 2em "Poppins", sans-serif;
  }
}

<-------------CSS-------------->



<-------------JS-------------->

 function loader() {
        $(window).on('load', function () {
            $('#ctn-preloader').addClass('loaded');
            $("#loading").fadeOut(500);
            // Una vez haya terminado el preloader aparezca el scroll

            if ($('#ctn-preloader').hasClass('loaded')) {
                // Es para que una vez que se haya ido el preloader se elimine toda la seccion preloader
                $('#preloader').delay(900).queue(function () {
                    $(this).remove();
                });
            }
        });
    }
    loader();


<-------------JS-------------->









