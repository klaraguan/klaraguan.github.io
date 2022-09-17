---
layout: page
permalink: /
title: about
nav: about

<!--description:
address: <a href="https://www.google.com/maps/place/Du+Xue+Lu,+Nan+Shan+Qu,+Shen+Zhen+Shi,+Guang+Dong+Sheng,+China,+518071/@22.5938948,113.9895813,17z/data=!3m1!4b1!4m5!3m4!1s0x3403f2e52bee6d63:0x1cd59a51b71ee809!8m2!3d22.5938899!4d113.99177" class="page-description" target="_blank">HKUST GZ Campus, Guangzhou, Guangdong, China </a>
---

<div class="col p-0 pt-4 pb-4">
  <h1 class="pb-3 title text-left font-weight-bold">Zhitong "Klara" Guan</h1>
  <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.description }}</h6>
  {% if page.address %}
      <h6 class="m-0 mb-2" style="font-size: 0.83em;">{{ page.address }}</h6>
  {% endif %}
</div>

<!-- Introduction -->

<div style="display: flex; flex-wrap: wrap;">
    <div class="text-justify p-0">
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="float: right;">
          <img class="profile-img img-responsive" src="{{ 'me.jpg' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
            I am a Research Associate at <a href="https://www.mingmingfan.com/lab/" target="_blank">the APEX Group of Hong Kong University of Science and Techology (HKUST)</a> in Guangzhou, China, working on accessibility technology research. I am extremely fortunate to be advised by <a href="https://www.mingmingfan.com" target="_blank">Prof. Mingming Fan</a>. My research focuses on advancing Human-Computer Interaction. Specifically, I am interested in developing accessible technologies for people with disabilities. I hope to use technology to improve quality of life.
        </p>

        <p>
            Previously, I was a Product Manager in the <a href="https://www.wechat.com/" target="_blank">WeChat Group</a> of <a href="https://www.tencent.com/" target="_blank">Tencent Holdings Ltd.</a>, overseeing a myriad of products.
        </p>
    </div>

</div>

<div class="col text-justify p-0">
    <p>
        Before I joined WeChat, I obtained a Master's degree in Industrial Engineering and Operations Research
        from <a href="https://ieor.berkeley.edu/" target="_blank">UC Berkeley</a>, where I was advised by <a href="https://zheng.ieor.berkeley.edu/" target="_blank">Prof. Zeyu Zheng</a> working on practical machine learning and optimization problems. I earned my B.A. degree with Honors from UC Berkeley as well, where I double majored in <a href="https://math.berkeley.edu/" target="_blank">Math</a> and <a href="https://data.berkeley.edu/" target="_blank">Data Science</a>.
    </p>
</div>

<!-- News -->
<div class="news mt-3 p-0">
  <h1 class="title mb-4 p-0">news</h1>
  {% assign news = site.news | reverse %}
  {% for item in news limit: site.news_limit %}
    <div class="row p-0">
      <div class="col-sm-2 p-0">
        <span class="badge light-green darken-1 font-weight-bold text-uppercase align-middle date ml-3">
          {{ item.date | date: "%b %-d, %Y" }}
        </span>
      </div>
      <div class="col-sm-10 mt-2 mt-sm-0 ml-3 ml-md-0 p-0 font-weight-light text">
        <p>{{ item.content | remove: '<p>' | remove: '</p>' | emojify }}</p>
      </div>
    </div>
  {% endfor %}
</div>
