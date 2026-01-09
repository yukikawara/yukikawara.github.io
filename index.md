---
layout: default
---

<div class="home">
  <div class="hero-section">
    <h1 class="page-heading">瓦祐希 / Yuki Kawara</h1>

    <div class="hero-description">
      <p>IT 会社でエンジニアをしています。業務では MLOps をやったり、クラウドでのインフラ構築をしたりしています。個人では自然言語処理の論文を読んだりモデルを作ったりして遊んでいます。</p>
    </div>
  </div>

  <section class="skills-section">
    <h2>スキル</h2>
    <div class="skills-grid">
      <div class="skill-item">
        <h3>プログラミング言語</h3>
        <ul>
          <li>Python</li>
          <li>Rust</li>
          <li>Typescript</li>
          <li>Go</li>
          <li>変な言語（Brainf**k, Piet）</li>
        </ul>
      </div>

      <div class="skill-item">
        <h3>フレームワーク・ライブラリ</h3>
        <ul>
          <li>PyTorch</li>
          <li>Hugginface</li>
          <li>Mastra</li>
          <li>React</li>
        </ul>
      </div>

      <div class="skill-item">
        <h3>インフラ・ツール</h3>
        <ul>
          <li>Docker / Kubernetes</li>
          <li>AWS</li>
          <li>Terraform</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="projects-section">
    <h2>プロジェクト</h2>
    <div class="project-list">
      <div class="project-item">
        <h3>プロジェクト 1</h3>
        <p>プロジェクトの説明がここに入ります。</p>
      </div>

      <div class="project-item">
        <h3>プロジェクト 2</h3>
        <p>プロジェクトの説明がここに入ります。</p>
      </div>
    </div>
  </section>

  <section class="latest-posts">
    <h2>最新のブログ記事</h2>
    <ul class="post-list">
      {% for post in site.posts limit:3 %}
        <li>
          <span class="post-meta">{{ post.date | date: "%Y年%m月%d日" }}</span>
          <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </h3>
          {% if post.excerpt %}
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 100 }}</p>
          {% endif %}
        </li>
      {% endfor %}
    </ul>

    <p><a href="{{ '/blog' | relative_url }}">すべての記事を見る →</a></p>
  </section>

  <section class="contact-section">
    <h2>連絡先</h2>
    <p>お気軽にご連絡ください！</p>
    <div class="contact-links">
      {% if site.github_username %}
        <a href="https://github.com/{{ site.github_username }}" target="_blank">GitHub</a>
      {% endif %}
      {% if site.email %}
        <a href="mailto:{{ site.email }}">Email</a>
      {% endif %}
    </div>
  </section>
</div>