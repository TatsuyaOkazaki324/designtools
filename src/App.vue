<template>
  <div id="app">
    <div id="header">
      <p id="title">Design Tools</p>
      <p id="subtitle">by Tatsuya Okazaki</p>
    </div>
    <div
      v-for="(SiteInfo, SiteList_index) in SiteList"
      v-bind:key="SiteList_index"
      class="category_container"
    >
      <div class="category_label">{{ SiteInfo.Category }}</div>
      <div class="sites_container">
        <a
          v-for="(Site, Site_index) in SiteInfo.Sites"
          v-bind:key="Site_index"
          v-bind:href="Site.link"
          class="site_container"
        >
          <p class="silte_label">{{ Site.label }}</p>
          <img class="site_img" v-bind:src="Site.img" v-bind:alt="Site.label" />
          <p class="site_description">{{ Site.description }}</p>
        </a>
      </div>
    </div>
    <div id="footer">
      <div class="footer_conteiner">
        <span class="footer_title_conteiner">注意事項</span>
        <span class="footer_description_conteiner">
          <p>
            当サイトは<a
              class="anker"
              href="https://github.com/TatsuyaOkazaki324"
              >Tatsuya Okazaki</a
            >が管理運営しています。
          </p>
          <p>
            当サイトを利用される場合は、ここに記載した条件に準拠いただくものとします。当サイトをご利用いただいた時点で、以下利用条件の全てに同意頂いたものとさせて頂きます。
          </p>
          <ol>
            <li>
              当サイトは、有償・無償に関わらず便利と感じたサイトをまとめたものになります。ライセンスや権利問題については各サイトをご確認ください。
            </li>
            <li>
              第三者、または当サイトに損害や不利益を与える行為、第三者、または当サイトの信用や名誉を損なう行為は禁止とさせて頂きます。
            </li>
          </ol>
        </span>
      </div>
      <div class="footer_conteiner">
        <span class="footer_title_conteiner">免責事項</span>
        <span class="footer_description_conteiner">
          <p>
            <a class="anker" href="https://github.com/TatsuyaOkazaki324"
              >Tatsuya Okazaki</a
            >は、当サイトにコンテンツを掲載するにあたって、その内容、機能等について細心の注意を払っておりますが、コンテンツの内容が正確であるかどうか、最新のものであるかどうか、安全なものであるか等について保証をするものではなく、何らの責任を負うものではありません。また、当社は通知することなく当サイトに掲載した情報の訂正、修正、追加、中断、削除等をいつでも行うことができるものとします。
          </p>
          <p>
            また、当サイト、またはコンテンツのご利用により、万一、ご利用者様に何らかの不都合や損害が発生したとしても、当サイト及び管理人は何らの責任を負うものではありません。
          </p>
        </span>
      </div>
      <div class="footer_conteiner">
        <span class="footer_title_conteiner">リンクについて</span>
        <span class="footer_description_conteiner">
          <p>
            当サイトはリンクフリーです。但し、公序良俗に反したサイトからのリンクはお断り致します。
          </p>
          <p>
            又、
            当サイトから第三者のサイトにリンクを張っている場合や、第三者のサイトから当サイトにリンクを張っている場合、いずれの場合に於いても、第三者のサイトの内容は、第三者の責任で管理・運営されているものであり、それらを利用されたことによって生ずる如何なる不都合や損害についても、当サイトは責任を負いかねます。
          </p>
        </span>
      </div>
      <div class="footer_conteiner">
        <span class="footer_title_conteiner">当サイトについて</span>
        <span class="footer_description_conteiner">
          <p>
            当サイトはHTML5で作成されています。また、モバイル対応をしていないため、ご注意ください。
          </p>
          <p>
            当サイトはスタイルでFlexBoxを用いているため、ブラウザによってはデザインが正しく表示されないことがありますので、ご注意ください。
          </p>
          <p>
            当サイトはGitHubPagesにて公開しております。何かあれば<a
              class="anker"
              href="https://github.com/TatsuyaOkazaki324/designtools"
              >リポジトリ</a
            >のIssueからお知らせください。
          </p>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      SiteList: [
        {
          Category: "Color",
          Sites: [
            {
              label: "Picular",
              link: "https://picular.co/",
              img: require("./images/sites/picular.png"),
              description:
                "自由な表現でその言葉が持つイメージの色を表示してくれる。絶妙な淡い色も提案してくれるところもポイント。",
            },
            {
              label: "原色大辞典",
              link: "https://www.colordic.org/",
              img: require("./images/sites/colordic.png"),
              description:
                "色の名前とカラーコードが一目でわかる。気になる色から明度、彩度、輝度を少しずつ変化させたものを簡単に見ることができる。",
            },
            {
              label: "uiGradients",
              link: "https://uigradients.com/",
              img: require("./images/sites/uiGradients.png"),
              description:
                "グラデーションカラーを生成してくれる。メニューから好みの色を選ぶことができる。欲しいグラデーションのCSSをコピーすることも可能。",
            },
            {
              label: "配色の見本帳",
              link: "https://ironodata.info/search/",
              img: require("./images/sites/ironodata.png"),
              description:
                "色の検索が簡単にできる。気になるいろの派生色をサジェストしてくれる。人気色！よく見られている色ランキングが意外と便利。",
            },
            {
              label: "SCHEME COLOR",
              link: "https://www.schemecolor.com/",
              img: require("./images/sites/schemecolor.png"),
              description:
                "大量のカラースキームが存在している。ここのカラースキームにしたがってデザインすれば大概よく見える。",
            },
            {
              label: "HUE360",
              link: "https://uigradients.com/",
              img: require("./images/sites/hue360.png"),
              description:
                "1つの色を選択するとそれに合う色に絞って表示してくれる。配色を決めていきたいときに用いると初心者でも簡単に良い配色を作れる。",
            },
          ],
        },
        {
          Category: "Materials",
          Sites: [
            {
              label: "Loose Drawing",
              link: "https://loosedrawing.com/",
              img: require("./images/sites/loosedrawing.png"),
              description:
                "かわいいイラストがたくさん存在する。色も数パターンになっており淡い色が多いため用途が広い。",
            },
            {
              label: "ソコスト",
              link: "https://soco-st.com/",
              img: require("./images/sites/sokosuto.png"),
              description:
                "アイコンやイラストがタグやカテゴリーから絞り込んで検索することが可能。イラストの塗りがしっかりしていてかわいい。",
            },
            {
              label: "ちょうどいいイラスト",
              link: "https://tyoudoii-illust.com/",
              img: require("./images/sites/choudoiiilust.png"),
              description:
                "イラストをカテゴリーから検索できる。フォーマルなイラストが多いイメージがある。用途に合わせるとデザインが合わせられて便利。",
            },
            {
              label: "Linustock",
              link: "https://www.linustock.com/vectors",
              img: require("./images/sites/linustock.png"),
              description:
                "イラストのジャンルが幅広く色々な場面で使える。色有りと色無しを選べるため、使い勝手が良い。",
            },
            {
              label: "Open Peeps",
              link: "https://www.openpeeps.com/",
              img: require("./images/sites/openpeeps.png"),
              description:
                "人物のイラストが数多く存在する。完成したイラストをダウンロードでき、イラストをカスタマイズすることも可能。",
            },
            {
              label: "SHiGURENi",
              link: "https://shigureni.com/",
              img: require("./images/sites/shigureni.png"),
              description:
                "女の子の素朴なイラストが数多く存在する。画風を統一したい時は便利になるかも。",
            },
            {
              label: "manypixels",
              link: "https://www.manypixels.co/gallery/",
              img: require("./images/sites/manypixels.png"),
              description:
                "おしゃれなイラストがある。イラストのテーマ色を決めることができ、作りたいテーマ色に色を合わせることも可能。",
            },
            {
              label: "ISOMETRIC",
              link: "https://isometric.online/",
              img: require("./images/sites/isometric.png"),
              description:
                "モノとヒトのイラストが多い。他のサイトに無いようなジャンルのイラストが有るため、困ったら頼れるサイト。",
            },
            {
              label: "unDraw",
              link: "https://undraw.co/illustrations",
              img: require("./images/sites/unDraw.png"),
              description:
                "テーマカラーを指定してイラストをカスタマイズできる。ヒトとコンピュータのイラストが多いイメージ。",
            },
            {
              label: "ICOON MONO",
              link: "https://icooon-mono.com/",
              img: require("./images/sites/icoonmono.png"),
              description:
                "ロゴマークやデザインが多く存在する。日本語でも検索ができ、色の選択も可能。",
            },
            {
              label: "Material icons",
              link: "https://material.io/resources/icons/",
              img: require("./images/sites/materialicons.png"),
              description:
                "Googleが提供してるアイコン。小さくて多種多様なアイコンが多く存在する。",
            },
            {
              label: "Icon-rainbow",
              link: "https://icon-rainbow.com/",
              img: require("./images/sites/iconrainbow.png"),
              description:
                "日本語で検索が可能。アイコンの色も自由に指定ができる。サイズの種類も豊富。",
            },
            {
              label: "ダ鳥獣ギ画",
              link: "https://chojugiga.com/",
              img: require("./images/sites/choujugiga.png"),
              description:
                "鳥獣戯画がモチーフとなったイラストがたくさん存在する。種類も豊富で見てても飽きない。かわいい。",
            },
            {
              label: "Human Pictogram 2.0",
              link: "http://pictogram2.com/",
              img: require("./images/sites/humanpictogram.png"),
              description:
                "日本語で検索可能。豊富なピクトグラムが存在する。色の種類は少ない。",
            },
            {
              label: "いらすとや",
              link: "https://www.irasutoya.com/",
              img: require("./images/sites/irasutoya.png"),
              description:
                "みんなに人気のいらすとや。ニッチなイラストまで圧倒的なカバー力を持つ。フランクな場面で使いやすい。",
            },
            {
              label: "Bootstrap Icons",
              link: "https://icons.getbootstrap.com/",
              img: require("./images/sites/BootstrapIcons.png"),
              description:
                "Bootstrapが提供するアイコン集。npmでインストールできる。ニッチなアイコンが多くてSVGでダウンロードができる。",
            },
            {
              label: "Facebook Design",
              link: "https://design.facebook.com/",
              img: require("./images/sites/facebookdesign.png"),
              description:
                "英語ベースだが、サイトそのもののデザインが優れていることや、モックアップの画像をダウンロードできたりなど、汎用性が高い。",
            },
            {
              label: "lordicon",
              link: "https://lordicon.com/icons",
              img: require("./images/sites/lordicon.png"),
              description:
                "動きのあるアイコンを多数用意しているサイト。アイコンのパーツごとの色を指定することも可能。サイトそのものが思いため注意が必要。",
            },
          ],
        },
        {
          Category: "Style",
          Sites: [
            {
              label: "Neumorphism .io",
              link: "https://neumorphism.io/",
              img: require("./images/sites/Neumorphism.png"),
              description:
                "Neumorphismのデザインを簡単に作成できる。色や凹凸感もGUIで設定してCSSを生成してくれる。",
            },
            {
              label: "Glassmorphism .io",
              link: "https://glassmorphism.com/",
              img: require("./images/sites/glassmorphism.png"),
              description:
                "Glassmorphismのデザインを簡単に作成できる。ブラーなどもプレビューしながら調整可能",
            },
          ],
        },
        {
          Category: "Tips",
          Sites: [
            {
              label: "ヒューマンインターフェース ガイドライン",
              link: "https://www.sociomedia.co.jp/category/shig",
              img: require("./images/sites/Sociomedia.png"),
              description:
                "デザインに関する知識が集まっているサイト。ここを見れば一通りのデザインについての原則を勉強できそう。",
            },
          ],
        },
        {
          Category: "Skills",
          Sites: [
            {
              label: "exercism",
              link: "https://exercism.io/",
              img: require("./images/sites/exercism.png"),
              description:
                "プログラミングの52言語の教育ツールが存在している。日本のプログラミング教育サービスとの違いは英語かどうか。無料。",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=M+PLUS+Rounded+1c&display=swap");
#app {
  font-family: "M PLUS Rounded 1c", sans-serif;
  background-color: #e0e9fd;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
#header {
  width: 60%;
  max-width: 600px;
  min-width: 300px;
  padding: 10px;
  margin: 20px 0;
  border-radius: 0 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: #eff3fc;
  box-shadow: 10px 10px 20px #83868b, -10px -10px 20px #ffffff;
  #title {
    font-size: 40px;
  }
  #subtitle {
    font-size: 20px;
  }
}
.category_container {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  .category_label {
    width: 15%;
    min-width: 250px;
    border-bottom: solid 2px #333333;
    font-size: 30px;
    margin-top: 15px;
    margin-bottom: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .sites_container {
    width: 90%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    flex-wrap: wrap;
    .site_container {
      color: #000;
      text-decoration: none;
      width: 300px;
      padding: 10px;
      margin: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      border-radius: 50px 0;
      box-shadow: 10px 10px 20px #868c98, -10px -10px 20px #ffffff;
      .silte_label {
        font-size: 25px;
        width: 200px;
        padding: 5px 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        box-shadow: inset 2px 2px 3px #868c98, inset -2px -2px 3px #ffffff;
      }
      .site_img {
        width: 220px;
        border: solid 1px #246cac;
        margin: 30px 0;
        border-radius: 0 70px;
        box-shadow: 1px 1px 2px #868c98, -1px -1px 2px #ffffff;
      }
      .site_description {
        font-size: 15px;
        width: 250px;
        padding: 5px 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 10px;
        box-shadow: inset 3px 3px 5px #868c98, inset -3px -3px 5px #ffffff;
      }
      &:hover {
        box-shadow: 3px 3px 4px #868c98, -3px -3px 4px #ffffff;
      }
    }
  }
}
#footer {
  background-color: #e0e9fd;
  width: 100%;
  margin: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  .footer_conteiner {
    width: 90%;
    max-width: 1000px;
    padding: 10px;
    margin: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    border-radius: 10px;
    box-shadow: 10px 10px 20px #868c98, -10px -10px 20px #ffffff;
    .footer_title_conteiner {
      font-size: 20px;
    }
    .footer_description_conteiner {
      width: 100%;
      margin: 10px;
      padding: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      border-radius: 10px;
      box-shadow: inset 2px 2px 3px #868c98, inset -2px -2px 3px #ffffff;
    }
  }
}
/* A Modern CSS Reset */
*,
*::before,
*::after {
  box-sizing: border-box;
}
body,
h1,
h2,
h3,
h4,
p,
figure,
blockquote,
dl,
dd {
  margin: 0;
}
ul[role="list"],
ol[role="list"] {
  list-style: none;
}
html:focus-within {
  scroll-behavior: smooth;
}
body {
  min-height: 100vh;
  text-rendering: optimizeSpeed;
  line-height: 1.5;
}
a:not([class]) {
  text-decoration-skip-ink: auto;
}
img,
picture {
  max-width: 100%;
  display: block;
}
input,
button,
textarea,
select {
  font: inherit;
}
@media (prefers-reduced-motion: reduce) {
  html:focus-within {
    scroll-behavior: auto;
  }
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
</style>
