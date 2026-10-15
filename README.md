[index (2).html](https://github.com/user-attachments/files/33495818/index.2.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#020817">
<title>집성량계 | 대성고등학교 천문 동아리</title>
<style>
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  margin:0;color:#eef4ff;background:#020817;
  font-family:-apple-system,BlinkMacSystemFont,"Apple SD Gothic Neo","Noto Sans KR",
  "Noto Sans",Roboto,"Malgun Gothic",Arial,sans-serif;
  overflow-x:hidden;
}
body:before{
  content:"";position:fixed;inset:0;z-index:-3;
  background:
    radial-gradient(circle at 20% 15%,rgba(65,105,225,.22),transparent 28%),
    radial-gradient(circle at 80% 80%,rgba(100,60,200,.18),transparent 30%),
    linear-gradient(#010611,#07152f 48%,#020817);
}
.stars{
  position:fixed;inset:0;z-index:-2;pointer-events:none;opacity:.75;
  background-image:
    radial-gradient(circle,#fff 1px,transparent 1.5px),
    radial-gradient(circle,#9ec5ff 1px,transparent 1.5px),
    radial-gradient(circle,#fff 1.5px,transparent 2px);
  background-size:73px 73px,113px 113px,191px 191px;
  background-position:5px 12px,41px 27px,90px 70px;
  animation:stars 14s linear infinite;
}
@keyframes stars{50%{transform:translateY(-12px);opacity:1}100%{transform:translateY(-25px);opacity:.7}}
nav{
  position:sticky;top:0;z-index:20;padding:15px 6%;
  display:flex;justify-content:space-between;align-items:center;
  background:rgba(2,8,23,.82);backdrop-filter:blur(16px);
  border-bottom:1px solid rgba(170,200,255,.12)
}
.brand{font-size:21px;font-weight:800;color:#ffe2a3;cursor:pointer}
nav button{border:0;background:none;color:#c8d7f5;font:inherit;cursor:pointer}
section{padding:85px 6%;max-width:1400px;margin:auto}
.hero{min-height:calc(100vh - 64px);display:flex;flex-direction:column;justify-content:center;text-align:center}
.logo-frame{
  width:min(900px,100%);margin:0 auto 34px;padding:10px;
  border:1px solid rgba(255,220,160,.25);border-radius:28px;
  background:rgba(2,8,23,.45);box-shadow:0 0 55px rgba(80,120,255,.16)
}
.logo-frame img{width:100%;display:block;border-radius:20px}
h1{font-size:clamp(48px,8vw,92px);margin:8px 0;color:#ffe2a3;text-shadow:0 0 30px rgba(255,226,163,.28)}
.kicker{color:#a9c6ff;font-size:18px}
.lead{max-width:850px;margin:0 auto 30px;line-height:1.9;color:#d9e5fa;word-break:keep-all}
.btn{
  display:inline-block;border:1px solid #7799e8;border-radius:999px;
  padding:14px 27px;background:linear-gradient(135deg,#2947a6,#6042b5);
  color:#fff;font:inherit;cursor:pointer;box-shadow:0 0 25px rgba(70,100,220,.25)
}
.btn:hover{transform:translateY(-2px)}
.title{text-align:center;font-size:clamp(38px,6vw,64px);margin:0 0 12px;color:#ffe2a3}
.sub{text-align:center;color:#aebfdf;margin:0 auto 42px}
.two{
  display:grid;grid-template-columns:repeat(2,1fr);gap:25px;max-width:1150px;margin:45px auto
}
.card{
  padding:28px;border-radius:24px;background:rgba(9,23,55,.78);
  border:1px solid rgba(140,175,245,.25);box-shadow:0 15px 40px rgba(0,0,0,.18)
}
.card h2{color:#aecdff;margin-top:0}
.card p{line-height:1.9;color:#dce7fa;word-break:keep-all}
.image-slot{
  aspect-ratio:16/10;border-radius:18px;overflow:hidden;margin-bottom:20px;
  display:flex;align-items:center;justify-content:center;background:#07142e;
  border:1px solid rgba(150,180,255,.22)
}
.image-slot img{width:100%;height:100%;object-fit:cover}
.image-slot .symbol{font-size:85px;color:#ffe2a3;text-shadow:0 0 25px #fff}
.grid{
  display:grid;grid-template-columns:repeat(4,1fr);gap:18px;max-width:1250px;margin:auto
}
.zodiac{
  padding:15px;border-radius:20px;background:linear-gradient(145deg,rgba(20,40,85,.88),rgba(4,11,29,.9));
  border:1px solid rgba(145,175,240,.22);cursor:pointer;transition:.25s
}
.zodiac:hover{transform:translateY(-6px);border-color:#ffe2a3;box-shadow:0 0 28px rgba(255,220,160,.18)}
.zodiac .image-slot{aspect-ratio:1;margin-bottom:12px}
.zodiac h3{margin:7px 0;font-size:19px}
.zodiac small{color:#9eb4d8}
.detail{
  display:none;max-width:1100px;margin:auto;
  grid-template-columns:1fr 1.25fr;gap:45px;align-items:center
}
.detail.show{display:grid}
.detail .image-slot{aspect-ratio:1;border-radius:50%}
.detail h2{font-size:clamp(42px,6vw,70px);color:#ffe2a3;margin:0}
.detail .date{color:#9fc2ff}
.detail-box{margin-top:14px;padding:18px 20px;border-radius:17px;background:rgba(15,32,72,.72);border:1px solid rgba(140,175,245,.2)}
.detail-box h3{margin:0 0 8px;color:#aecdff}
.detail-box p{margin:0;line-height:1.85;word-break:keep-all}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:25px}
.survey{width:min(750px,100%);max-width:750px;margin:0 auto;display:block;position:relative;left:auto;right:auto;float:none}
.question{margin:28px 0}
.stars-rate{display:flex;flex-direction:row-reverse;justify-content:flex-end;gap:7px}
.stars-rate input{display:none}
.stars-rate label{font-size:34px;color:#52627f;cursor:pointer}
.stars-rate input:checked~label,.stars-rate label:hover,.stars-rate label:hover~label{color:#ffe2a3}
textarea{width:100%;min-height:130px;background:#07142e;color:#fff;border:1px solid #425c9b;border-radius:15px;padding:14px;font:inherit;resize:vertical}
.thanks{display:none;text-align:center}
footer{text-align:center;padding:45px 20px;color:#7f91b3;font-size:13px}
@media(max-width:1050px){.grid{grid-template-columns:repeat(3,1fr)}}
@media(max-width:760px){
  nav{padding:13px 5%}
  section{padding:65px 5%}
  .two,.detail{grid-template-columns:1fr}
  .grid{grid-template-columns:repeat(2,1fr);gap:12px}
  .zodiac{padding:10px}.zodiac h3{font-size:17px}.zodiac small{font-size:12px}
  .logo-frame{padding:6px;border-radius:20px}
}
@media(max-width:430px){
  body{font-size:15px}
  h1{font-size:48px}
  .grid{grid-template-columns:repeat(2,1fr)}
  .title{font-size:40px}
}
</style>
</head>
<body>
<div class="stars"></div>

<nav>
  <div class="brand" onclick="home()">集星量計</div>
  <button onclick="home()">메인</button>
</nav>

<main id="homePage">
<section>
  <h2 class="title">메인 페이지</h2>
  <p class="sub">동아리 로고와 북극성을 중심으로 천문학을 알아갑니다.</p>
  <div class="two">
    <article class="card">
      <div class="image-slot"><img src="images/logo.png" alt="동아리 로고"></div>
      <h2>집성량계 로고</h2>
      <p>별을 관측하는 데서 그치지 않고 별과 우주를 직접 탐구하고, 천문학과에서 배우게 될 내용을 미리 경험한다는 의미를 담은 로고입니다.</p>
    </article>
    <article class="card">
      <div class="image-slot">
        <img id="polarisImage" src="images/polaris.jpg" alt="북극성" onerror="this.style.display='none';document.getElementById('polarisSymbol').style.display='block'">
        <div id="polarisSymbol" class="symbol" style="display:none">★</div>
      </div>
      <h2>북극성</h2>
      <p>북극성은 지구의 북쪽 하늘에서 거의 움직이지 않는 것처럼 보이며 방향을 찾는 기준으로 오랫동안 이용되어 온 별입니다. 현재의 북극성은 작은곰자리의 폴라리스입니다.</p>
    </article>
  </div>
</section>
<section class="hero">
  <div class="logo-frame">
    <img src="images/logo.png" alt="집성량계 동아리 로고">
  </div>
  <div class="kicker">대성고등학교 천문 동아리</div>
  <h1>集星量計</h1>
  <p class="lead">모을 집 · 별 성 · 헤아릴 량 · 셀 계<br>
  별을 모아, 밝기를 재고, 우주를 계산하다.</p>
  <button class="btn" onclick="showZodiacList()">다음 → 황도 12궁</button>
</section>



<section>
  <h2 class="title">동아리 소개</h2>
  <div class="card">
    <p>
      대성고등학교 학우분들은 천문학과를 지원할 때 별을 관측하는 것만 생각하고 입학하여
      대학교 2, 3학년 때 당황하거나 전과를 선택하는 일이 없도록, 그리고 친구가 천문학과를
      목표로 한다고 하였을 때 점성술과 혼동하지 않도록 이를 알리고자 합니다.
    </p>
    <p>
      또한 천문학과를 선택하여 대학교에 입학했을 때 어떤 것을 배우게 되는지 미리 경험하고
      알아가는 시간을 동아리원들과 함께 나누고자 이 동아리를 만들려고 합니다.
    </p>
  </div>
</section>
</main>

<section id="zodiacPage" style="display:none">
  <h2 class="title">황도 12궁</h2>
  <p class="sub">별자리를 클릭하면 사진과 설명, 성격, 응원 메시지를 확인할 수 있습니다.</p>
  <div id="zodiacGrid" class="grid"></div>
</section>

<section id="detailPage" style="display:none">
  <div id="detail" class="detail">
    <div class="image-slot" id="detailImage"></div>
    <div>
      <h2 id="detailName"></h2>
      <p class="date" id="detailDate"></p>
      <div class="detail-box"><h3>설명</h3><p id="detailDesc"></p></div>
      <div class="detail-box"><h3>성격</h3><p id="detailPersonality"></p></div>
      <div class="detail-box"><h3>응원 메시지</h3><p id="detailMessage"></p></div>
      <div class="actions">
        <button class="btn" onclick="showZodiacList()">← 목록</button>
        <button class="btn" onclick="nextZodiac()">다음 →</button>
      </div>
    </div>
  </div>
</section>

<section id="surveyPage" style="display:none;width:100%;margin-left:auto;margin-right:auto">
  <div class="card survey" style="margin-left:auto;margin-right:auto;float:none">
    <div id="surveyForm">
      <h2 class="title">만족도 조사</h2>
      <p class="sub">집성량계 홈페이지를 둘러본 후 의견을 남겨주세요.</p>
      <div class="question">
        <h3>콘텐츠가 재미있었나요?</h3>
        <div class="stars-rate">
          <input id="f5" name="fun" type="radio"><label for="f5">★</label>
          <input id="f4" name="fun" type="radio"><label for="f4">★</label>
          <input id="f3" name="fun" type="radio"><label for="f3">★</label>
          <input id="f2" name="fun" type="radio"><label for="f2">★</label>
          <input id="f1" name="fun" type="radio"><label for="f1">★</label>
        </div>
      </div>
      <div class="question">
        <h3>디자인은 만족스러웠나요?</h3>
        <div class="stars-rate">
          <input id="d5" name="design" type="radio"><label for="d5">★</label>
          <input id="d4" name="design" type="radio"><label for="d4">★</label>
          <input id="d3" name="design" type="radio"><label for="d3">★</label>
          <input id="d2" name="design" type="radio"><label for="d2">★</label>
          <input id="d1" name="design" type="radio"><label for="d1">★</label>
        </div>
      </div>
      <div class="question">
        <h3>남기고 싶은 말</h3>
        <textarea placeholder="자유롭게 의견을 적어주세요."></textarea>
      </div>
      <button class="btn" onclick="submitSurvey()">제출하기</button>
    </div>
    <div id="thanks" class="thanks">
      <h2 class="title">감사합니다.</h2>
      <p class="sub">여러분의 의견은 더 좋은 집성량계를 만드는 데 도움이 됩니다.</p>
      <button class="btn" onclick="home()">처음으로</button>
    </div>
  </div>
</section>

<footer>집성량계 · 대성고등학교 천문 동아리</footer>

<script>
const data=[
["양자리","3월 21일 ~ 4월 19일","aries.jpg","황도 12궁의 첫 번째 별자리입니다. 새로운 시작과 도전을 상징하며 봄의 시작과 함께 알려져 있습니다.","적극적이고 도전적인 성향을 가지고 있습니다.","새로운 도전을 두려워하지 말고 한 걸음씩 나아가세요."],
["황소자리","4월 20일 ~ 5월 20일","taurus.jpg","황소의 모습을 상징하는 별자리입니다. 밝은 별 알데바란이 있는 것으로 잘 알려져 있습니다.","꾸준하고 책임감이 강한 편입니다.","천천히 가더라도 끝까지 나아가세요."],
["쌍둥이자리","5월 21일 ~ 6월 21일","gemini.jpg","두 형제의 이야기를 바탕으로 한 별자리입니다. 카스토르와 폴룩스가 대표적인 별입니다.","호기심이 많고 다양한 것에 관심이 많습니다.","당신의 호기심이 새로운 길을 만들어 줍니다."],
["게자리","6월 22일 ~ 7월 22일","cancer.jpg","게의 모습을 나타낸 별자리입니다. 황도 12궁 가운데 하나로 여름철 밤하늘에서 찾아볼 수 있습니다.","감정이 풍부하고 주변 사람을 잘 챙깁니다.","당신의 따뜻함은 주변에 큰 힘이 됩니다."],
["사자자리","7월 23일 ~ 8월 22일","leo.jpg","사자를 상징하는 별자리이며 밝은 별 레굴루스가 유명합니다. 용기와 자신감을 상징합니다.","자신감이 있고 리더십을 발휘하는 편입니다.","자신감을 가지고 앞으로 나아가세요."],
["처녀자리","8월 23일 ~ 9월 22일","virgo.jpg","황도 12궁의 하나이며 밝은 별 스피카로 유명합니다. 봄과 초여름 밤하늘에서 관찰하기 좋습니다.","꼼꼼하고 성실한 성향을 가지고 있습니다.","당신의 꾸준한 노력은 반드시 빛날 것입니다."],
["천칭자리","9월 23일 ~ 10월 22일","libra.jpg","저울을 상징하는 별자리입니다. 균형과 조화를 나타내며 황도 12궁 중 유일하게 물건을 표현합니다.","공정함을 중요하게 생각하고 균형을 추구합니다.","당신만의 균형을 찾아 자신 있게 나아가세요."],
["전갈자리","10월 23일 ~ 11월 22일","scorpio.jpg","전갈을 나타내는 별자리이며 붉은 별 안타레스로 유명합니다.","목표를 향한 집중력이 강한 편입니다.","당신의 열정을 끝까지 믿으세요."],
["궁수자리","11월 23일 ~ 12월 21일","sagittarius.jpg","활을 든 궁수의 모습을 나타내는 별자리입니다. 우리 은하 중심 방향과 가까운 하늘에 위치합니다.","자유롭고 새로운 경험을 좋아합니다.","더 넓은 세상을 향해 나아가세요."],
["염소자리","12월 22일 ~ 1월 19일","capricorn.jpg","염소와 물고기의 모습이 결합된 별자리로 오래된 신화와 관련되어 있습니다.","목표를 정하면 꾸준히 노력하는 편입니다.","꾸준함은 가장 강한 힘입니다."],
["물병자리","1월 20일 ~ 2월 18일","aquarius.jpg","물을 나르는 사람을 나타내는 별자리입니다. 겨울철 밤하늘에서 찾아볼 수 있습니다.","독창적이고 새로운 생각을 좋아합니다.","당신만의 특별한 생각을 믿으세요."],
["물고기자리","2월 19일 ~ 3월 20일","pisces.jpg","두 마리의 물고기를 나타내는 별자리입니다. 황도 12궁의 마지막 별자리입니다.","상상력이 풍부하고 감수성이 높은 편입니다.","당신의 상상력은 무한한 가능성입니다."]
];
let current=0;

function imageHTML(file,symbol){
  return `<img src="images/${file}" alt="" onerror="this.style.display='none';this.nextElementSibling.style.display='block"><div class="symbol" style="display:none">${symbol}</div>`;
}
const symbols=["♈","♉","♊","♋","♌","♍","♎","♏","♐","♑","♒","♓"];

function showZodiacList(){
  hideAll(); document.getElementById("zodiacPage").style.display="block";
  window.scrollTo(0,0);
}
function showDetail(i){
  current=i; hideAll(); document.getElementById("detailPage").style.display="block";
  const d=data[i];
  document.getElementById("detail").classList.add("show");
  document.getElementById("detailImage").innerHTML=imageHTML(d[2],symbols[i]);
  document.getElementById("detailName").textContent=d[0];
  document.getElementById("detailDate").textContent=d[1];
  document.getElementById("detailDesc").textContent=d[3];
  document.getElementById("detailPersonality").textContent=d[4];
  document.getElementById("detailMessage").textContent=d[5];
  window.scrollTo(0,0);
}
function nextZodiac(){
  if(current<data.length-1) showDetail(current+1);
  else {hideAll();document.getElementById("surveyPage").style.display="block";window.scrollTo(0,0)}
}
function home(){hideAll();document.getElementById("homePage").style.display="block";window.scrollTo(0,0)}
function hideAll(){
  ["homePage","zodiacPage","detailPage","surveyPage"].forEach(id=>document.getElementById(id).style.display="none");
  document.getElementById("detail").classList.remove("show");
}
function submitSurvey(){
  document.getElementById("surveyForm").style.display="none";
  document.getElementById("thanks").style.display="block";
}

const grid=document.getElementById("zodiacGrid");
data.forEach((d,i)=>{
  grid.innerHTML+=`<article class="zodiac" onclick="showDetail(${i})">
    <div class="image-slot">${imageHTML(d[2],symbols[i])}</div>
    <h3>${d[0]}</h3><small>${d[1]}</small>
  </article>`;
});
</script>
</body>
</html>
