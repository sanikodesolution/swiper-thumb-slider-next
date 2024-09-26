import React, { useLayoutEffect, useRef, useState } from "react";
import { Swiper, SwiperSlide } from "swiper/react";
import { FreeMode, Navigation, Thumbs } from 'swiper/modules';

const DemoSlider = () => {
  const [thumbsSwiper, setThumbsSwiper] = useState(null);
  return (
  <>
  <section className="testimonial-section-five pt-0">
    <div className="auto-container">
      <div className="sec-title text-center">
        <span className="sub-title">Testimonial</span>
        <h2>Designs that leave a lasting <br/> impression</h2>
      </div>
      <div className="testimonials">
        <div className="swiper-container testimonial-thumbs">
          <Swiper
            onSwiper={setThumbsSwiper}
            slidesPerView={3}
            modules={[Thumbs]}
            loop={true}
            spaceBetween={10}
            autoPlay={500}
            centeredSlides={true}
            className="testimonial-thumbs">
            <SwiperSlide className="swiper-slide">
              <img src="https://swiperjs.com/demos/images/nature-1.jpg" alt=""/>
            </SwiperSlide>
            <SwiperSlide className="swiper-slide">
              <img src="https://swiperjs.com/demos/images/nature-2.jpg" alt=""/>
            </SwiperSlide>
            <SwiperSlide className="swiper-slide">
              <img src="https://swiperjs.com/demos/images/nature-3.jpg" alt=""/>
            </SwiperSlide>
            <SwiperSlide className="swiper-slide">
              <img src="https://swiperjs.com/demos/images/nature-4.jpg" alt=""/>
            </SwiperSlide>
          </Swiper>       
        </div>
        <div className="swiper-container testimonial-slider">
          <Swiper
            spaceBetween={10}
            slidesPerView={1}
            loop={true}
            thumbs={{swiper: thumbsSwiper && !thumbsSwiper.destroyed ? thumbsSwiper : null}}
            modules={[FreeMode, Navigation, Thumbs]}
            className="testimonial-slider">
            <SwiperSlide>
              <div className="testimonial-block-five swiper-slide">
                <img src="https://swiperjs.com/demos/images/nature-1.jpg" alt=""/>
              </div>
            </SwiperSlide>
            <SwiperSlide>
              <div className="testimonial-block-five swiper-slide">
                <img src="https://swiperjs.com/demos/images/nature-2.jpg" alt=""/>
              </div>
            </SwiperSlide>
            <SwiperSlide>
              <div className="testimonial-block-five swiper-slide">
                <img src="https://swiperjs.com/demos/images/nature-3.jpg" alt=""/>
              </div>
            </SwiperSlide>
            <SwiperSlide>
              <div className="testimonial-block-five swiper-slide">
                <img src="https://swiperjs.com/demos/images/nature-4.jpg" alt=""/>
              </div>
            </SwiperSlide>
          </Swiper>     
        </div>
      </div>
    </div>
  </section>
  </>
  );
};
export default DemoSlider