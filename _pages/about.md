---
layout: page
permalink: /
title: about
nav: about

<!--description:
address: <a href="https://g.co/kgs/Po6uFcK" class="page-description" target="_blank">1616 Guadalupe St., Shool of Information, UT Austin. Austin, TX 78701  </a>
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
        <div class="col-xs-12 col-sm-6 p-0 pt-2 pb-sm-2 pb-4 pl-sm-4 text-center" style="width:250px; float: right;">
          <img class="profile-img img-responsive" src="{{ 'me.png' | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}">
        </div>

        <p>
            I am a PhD student at the <a href="https://ischool.utexas.edu/" target="_blank">the School of Information at UT Austin</a>. I am extremely fortunate to be advised by <a href="https://ischool.utexas.edu/profiles/soo-young-rieh" target="_blank">Prof. Soo Young Rieh</a>. My research focuses on advancing Human-Computer Interaction and Search. Specifically, I am interested in rethinking technologies that can bridge thinking and reflection.
        </p>

        <p>
            Previously, I was a research associate at <a href="https://www.mingmingfan.com/lab/" target="_blank">the APEX Group of Hong Kong University of Science and Techology (HKUST)</a> in Guangzhou, China, working on accessibility technology research, advised by <a href="https://www.mingmingfan.com" target="_blank">Prof. Mingming Fan</a>. I also worked as a Product Manager in the <a href="https://www.wechat.com/" target="_blank">WeChat Group</a> of <a href="https://www.tencent.com/" target="_blank">Tencent Holdings Ltd.</a>, overseeing a myriad of products.
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
