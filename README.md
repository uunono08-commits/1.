<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>더나은생활연구소 | 전문 컨설팅</title>
<meta name="description" content="더나은생활연구소 - GMP, 화장품, HACCP, 의약외품 전문 컨설팅">
<style>
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:"Noto Sans KR","Apple SD Gothic Neo",sans-serif;color:#222;line-height:1.7;background:#fff}
a{text-decoration:none;color:inherit}
.container{width:90%;max-width:1180px;margin:auto}
section{padding:100px 0}

/* =========================
   Scroll Fade Animation
========================= */

section {
    opacity: 0;
    transform: translateY(35px);
    transition:
        opacity 0.8s ease,
        transform 0.8s ease;
}

section.is-visible {
    opacity: 1;
    transform: translateY(0);
}

section.has-passed {
    opacity: 0.18;
    transform: translateY(-25px);
}

section.is-current {
    opacity: 1;
    transform: translateY(0);
}

@media (prefers-reduced-motion: reduce) {
    section {
        opacity: 1;
        transform: none;
        transition: none;
    }

    section.has-passed {
        opacity: 1;
        transform: none;
    }
}

.section-title{text-align:center;margin-bottom:55px}
.section-title .eng{display:block;color:#050990;font-size:13px;font-weight:800;letter-spacing:2px;margin-bottom:8px}
.section-title h2{font-size:34px;color:#111;margin-bottom:10px}
.section-title p{color:#777}
header{position:fixed;top:0;left:0;width:100%;height:76px;background:rgba(255,255,255,.96);border-bottom:1px solid #eee;z-index:1000}
.header-inner{height:100%;display:flex;align-items:center;justify-content:space-between}
.logo{display:flex;align-items:center;justify-content:center;height:42px}
.logo img{max-height:42px;width:auto;display:block}
nav{display:flex;gap:32px}
nav a{font-size:14px;font-weight:600;transition:.3s}
nav a:hover{color:#050990}
.hero{min-height:760px;padding-top:76px;display:flex;align-items:center;background:linear-gradient(135deg,#f5f7ff,#fff 55%,#fffaf0)}
.hero-content{max-width:760px}
.hero-label{display:inline-block;color:#050990;font-size:14px;font-weight:800;letter-spacing:2px;margin-bottom:18px}
.hero h1{font-size:clamp(42px,6vw,72px);line-height:1.25;letter-spacing:-3px;margin-bottom:25px}
.hero h1 strong{color:#050990}
.hero-description{font-size:18px;color:#666;margin-bottom:35px}
.hero-buttons{display:flex;gap:12px;flex-wrap:wrap}
.btn{display:inline-flex;align-items:center;justify-content:center;min-width:150px;padding:14px 25px;border-radius:4px;font-weight:700;font-size:14px;transition:.3s}
.btn-primary{background:#050990;color:#fff}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(5,9,144,.2)}
.btn-yellow{background:#ffc107;color:#111}
.btn-yellow:hover{transform:translateY(-2px)}

/* Vision & Mission Layout */
.vision-mission{display:grid;grid-template-columns:1fr 1fr;gap:40px}
.vm-item{display:flex;flex-direction:column;align-items:center;text-align:center}
.vm-title-outside{display:block;font-size:32px;font-weight:900;letter-spacing:4px;margin-bottom:18px;text-align:center;width:100%}
.vm-item.vision-item .vm-title-outside{color:#ffc107}
.vm-item.mission-item .vm-title-outside{color:#050990}

.vm-card{
    position:relative;
    padding:42px;
    border:2px solid #e8e8e8;
    border-radius:24px;
    background:#fff;
    overflow:hidden;
    width:100%;
    flex-grow:1;
    display:flex;
    flex-direction:column;
    justify-content:center;
}
.vm-card.vision{
    border-color:#ffc107;
    background:linear-gradient(135deg,#fffdf5 0%,#fff 72%);
}
.vm-card.mission{
    border-color:#050990;
    background:linear-gradient(135deg,#f7f8ff 0%,#fff 72%);
}
.vm-top{
    display:flex;
    flex-direction:column;
    align-items:center;
    text-align:center;
    gap:16px;
    margin-bottom:20px;
}
.vm-icon{
    width:110px;
    height:110px;
    flex:0 0 110px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
}
.vision .vm-icon{background:#fff7d6}
.mission .vm-icon{background:#eef1ff}
.vm-icon svg{width:75px;height:75px}
.vm-card h3{
    font-size:25px;
    line-height:1.35;
    margin-bottom:0;
    color:#050990;
}
.vm-card p{
    color:#5f6d88;
    font-size:15px;
    text-align:center;
    max-width:520px;
    margin:0 auto;
}

/* Certificates Marquee */
.certificates{background:#f7f8fc;overflow:hidden}
.certificates-marquee{
    display:flex;
    width:100%;
    overflow:hidden;
    position:relative;
    padding:10px 0;
}
.certificates-track{
    display:flex;
    gap:22px;
    width:max-content;
    animation: marqueeSlide 25s linear infinite;
}
.certificates-track:hover{
    animation-play-state: paused;
}
@keyframes marqueeSlide {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
}
.certificate-card{
    flex:0 0 340px;
    min-height:250px;
    background:#fff;
    border:1px solid #e8e8e8;
    border-radius:12px;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:30px;
    box-shadow:0 4px 15px rgba(0,0,0,.03);
}
.certificate-placeholder{color:#aaa}
.certificate-placeholder strong{display:block;color:#050990;font-size:17px;margin-bottom:7px}

.service-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px}
.service-card{position:relative;padding:38px 27px;min-height:290px;border:1px solid #e6e6e6;background:#fff;transition:.3s;overflow:hidden}
.service-card::before{content:"";position:absolute;top:0;left:0;width:100%;height:4px;background:#050990}
.service-card:nth-child(even)::before{background:#ffc107}
.service-card:hover{transform:translateY(-6px);box-shadow:0 18px 40px rgba(0,0,0,.08)}
.service-number{color:#ccc;font-size:13px;font-weight:800;margin-bottom:18px}
.service-card h3{font-size:23px;color:#050990;margin-bottom:13px}
.service-card:nth-child(even) h3{color:#333}
.service-card p{color:#777;font-size:14px}
.service-list{margin-top:15px;padding-left:17px;color:#666;font-size:13px}
.contact{
    background:#f7f8fc;
    color:#222;
}
.contact .section-title .eng{color:#050990}
.contact .section-title h2{color:#111}
.contact .section-title p{color:#777}

.contact-box{
    max-width:1000px;
    margin:auto;
    background:#fff;
    border:1px solid #e7e9f2;
    border-radius:24px;
    padding:55px 60px;
    box-shadow:0 15px 40px rgba(5,9,144,.06);
}

.contact-intro{
    text-align:center;
    margin-bottom:35px;
}
.contact-intro h3{
    font-size:28px;
    color:#050990;
    margin-bottom:10px;
}
.contact-intro p{
    color:#777;
    font-size:15px;
}

.contact-methods{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
    margin-bottom:30px;
}

.contact-method{
    display:flex;
    align-items:center;
    gap:18px;
    padding:24px;
    border:1px solid #e8e9ef;
    border-radius:16px;
    background:#fff;
}
.contact-method.kakao{
    border-color:#ffe08a;
    background:#fffdf5;
}
.contact-method.phone{
    border-color:#cfd4ff;
    background:#f9faff;
}

.contact-icon{
    width:54px;
    height:54px;
    flex:0 0 54px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:24px;
    font-weight:800;
}
.contact-method.kakao .contact-icon{
    background:#ffc107;
    color:#111;
}
.contact-method.phone .contact-icon{
    background:#050990;
    color:#fff;
}

.contact-method small{
    display:block;
    color:#888;
    font-size:12px;
    font-weight:700;
    margin-bottom:3px;
}
.contact-method strong{
    display:block;
    color:#222;
    font-size:17px;
}

.contact-buttons{
    display:flex;
    justify-content:center;
    gap:12px;
    flex-wrap:wrap;
}
.contact-buttons .btn{
    min-width:190px;
}

.contact-notice{
    margin-top:22px;
    text-align:center;
    color:#999;
    font-size:12px;
}

@media(max-width:650px){
    .contact-box{
        padding:35px 20px;
        border-radius:18px;
    }
    .contact-intro h3{font-size:23px}
    .contact-methods{grid-template-columns:1fr}
    .contact-method{padding:20px}
}
.kakao-button{position:fixed;right:25px;bottom:25px;z-index:999;background:#ffc107;color:#111;width:65px;height:65px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:800;line-height:1.3;text-align:center;box-shadow:0 12px 28px rgba(255,193,7,.35)}
.kakao-button:hover{transform:scale(1.08)}
footer{background:#111;color:#888;padding:35px 0;font-size:13px}
.footer-inner{display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap}
.footer-logo{color:#fff;font-weight:800;font-size:17px}
@media(max-width:900px){
nav{gap:15px}nav a{font-size:12px}.service-grid{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:650px){
section{padding:70px 0}header{height:65px}.logo{height:34px}.logo img{max-height:34px}nav{display:none}.hero{min-height:650px;padding-top:65px}.hero h1{font-size:42px;letter-spacing:-2px}.hero-description{font-size:15px}.section-title h2{font-size:28px}.vision-mission{grid-template-columns:1fr}.kakao-button{width:58px;height:58px;right:15px;bottom:15px;font-size:12px}.contact-buttons .btn{width:100%}}
</style>
</head>
<body>

<header>
<div class="container header-inner">
<a href="#home" class="logo">
    <img src="logo.png" alt="더나은생활연구소">
</a>
<nav>
<a href="#about">회사소개</a>
<a href="#certificates">인증서</a>
<a href="#services">컨설팅</a>
<a href="#contact">문의하기</a>
</nav>
</div>
</header>

<section class="hero" id="home">
<div class="container">
<div class="hero-content">
<span class="hero-label">BETTER LIFE LAB</span>
<h1>더 나은 생활을 위한<br><strong>전문 컨설팅 솔루션</strong></h1>
<p class="hero-description">식품 안전부터 여성위생, 환경 분야까지<br>전문적인 컨설팅으로 더 나은 생활환경을 만들어갑니다.</p>
<div class="hero-buttons">
<a href="#services" class="btn btn-primary">컨설팅 서비스</a>
<a href="#contact" class="btn btn-yellow">상담 문의하기</a>
</div>
</div>
</div>
</section>

<section id="about">
<div class="container">
<div class="section-title">
<span class="eng">ABOUT US</span><h2>회사소개</h2>
<p>전문성과 경험을 바탕으로 더 나은 생활환경을 만들어갑니다.</p>
</div>
<div class="vision-mission">

<div class="vm-item vision-item">
<div class="vm-title-outside">VISION</div>
<div class="vm-card vision">
<div class="vm-top">
<div class="vm-icon" aria-hidden="true">
<svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
<circle cx="50" cy="27" r="10" stroke="#ffc107" stroke-width="5"/>
<path d="M38 43C38 37 43 34 50 34C57 34 62 37 62 43V58C62 64 57 68 50 68C43 68 38 64 38 58V43Z" stroke="#ffc107" stroke-width="5"/>
<path d="M43 68L39 82M57 68L61 82" stroke="#ffc107" stroke-width="5" stroke-linecap="round"/>
<path d="M25 18L27 23L32 25L27 27L25 32L23 27L18 25L23 23L25 18Z" fill="#ffc107"/>
<path d="M75 18L77 23L82 25L77 27L75 32L73 27L68 25L73 23L75 18Z" fill="#ffc107"/>
<path d="M24 58L27 65L34 68L27 71L24 78L21 71L14 68L21 65L24 58Z" fill="#ffc107"/>
<path d="M50 58L54 68L64 72L54 76L50 86L46 76L36 72L46 68L50 58Z" fill="#ffc107"/>
<path d="M76 58L79 65L86 68L79 71L76 78L73 71L66 68L73 65L76 58Z" fill="#ffc107"/>
</svg>
</div>
<div>
<h3>신뢰받는<br>전문기관으로 성장한다.</h3>
</div>
</div>
<p>식약처 인허가 컨설팅과 여성위생 DOA 분야에서 신뢰받는 전문기관으로 성장한다.</p>
</div>
</div>

<div class="vm-item mission-item">
<div class="vm-title-outside">MISSION</div>
<div class="vm-card mission">
<div class="vm-top">
<div class="vm-icon" aria-hidden="true">
<svg viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
<rect x="25" y="19" width="50" height="66" rx="4" stroke="#050990" stroke-width="5"/>
<path d="M38 19V13C38 10 40 8 43 8H57C60 8 62 10 62 13V19" stroke="#050990" stroke-width="5"/>
<path d="M36 39L40 43L47 35" stroke="#050990" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M52 39H66" stroke="#050990" stroke-width="5" stroke-linecap="round"/>
<path d="M36 55L40 59L47 51" stroke="#050990" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M52 55H66" stroke="#050990" stroke-width="5" stroke-linecap="round"/>
<path d="M36 71L40 75L47 67" stroke="#050990" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/>
<path d="M52 71H66" stroke="#050990" stroke-width="5" stroke-linecap="round"/>
</svg>
</div>
<div>
<h3>더 나은<br>생활환경을 만든다.</h3>
</div>
</div>
<p>식품 안전, 여성위생, 환경 분야에서 전문 솔루션을 제공하여 더 나은 생활환경을 만든다.</p>
</div>
</div>

</div>
</div>
</section>

<section class="certificates" id="certificates">
<div class="container" style="max-width:100%; width:100%;">
<div class="section-title">
<span class="eng">CERTIFICATES</span><h2>인증서</h2>
<p>전문성과 신뢰를 뒷받침하는 인증 및 자격을 소개합니다.</p>
</div>
</div>
<div class="certificates-marquee">
<div class="certificates-track">
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 01</strong>실제 인증서 이미지로 교체해주세요.</div></div>
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 02</strong>실제 인증서 이미지로 교체해주세요.</div></div>
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 03</strong>실제 인증서 이미지로 교체해주세요.</div></div>
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 01</strong>실제 인증서 이미지로 교체해주세요.</div></div>
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 02</strong>실제 인증서 이미지로 교체해주세요.</div></div>
<div class="certificate-card"><div class="certificate-placeholder"><strong>인증서 이미지 03</strong>실제 인증서 이미지로 교체해주세요.</div></div>
</div>
</div>
</section>

<section id="services">
<div class="container">
<div class="section-title">
<span class="eng">CONSULTING SERVICE</span><h2>컨설팅 서비스</h2>
<p>제품과 제조환경에 맞는 전문적인 컨설팅을 제공합니다.</p>
</div>
<div class="service-grid">

<div class="service-card">
<div class="service-number">01</div><h3>GMP</h3>
<p>의약품 등의 제조 및 품질관리를 위한 GMP 관련 컨설팅을 제공합니다.</p>
<ul class="service-list"><li>GMP 기준 검토</li><li>시설 및 제조환경 검토</li><li>기준서 및 문서 관리</li><li>현장 적용 및 준비</li></ul>
</div>

<div class="service-card">
<div class="service-number">02</div><h3>화장품</h3>
<p>화장품 제조 및 품질관리와 관련된 전문 컨설팅을 제공합니다.</p>
<ul class="service-list"><li>제품 및 제조공정 검토</li><li>시설 및 위생관리</li><li>관련 기준 검토</li><li>현장 적용 지원</li></ul>
</div>

<div class="service-card">
<div class="service-number">03</div><h3>HACCP 인증</h3>
<p>안전한 식품 제조환경을 위한 HACCP 인증 준비를 지원합니다.</p>
<ul class="service-list"><li>제품 및 제조공정 검토</li><li>시설 및 위생관리</li><li>HACCP 기준서 작성 및 관리</li><li>현장 적용 및 심사 준비</li></ul>
</div>

<div class="service-card">
<div class="service-number">04</div><h3>의약외품</h3>
<p>의약외품 제품의 인허가 및 제조·품질관리 관련 컨설팅을 제공합니다.</p>
<ul class="service-list"><li>제품 관련 검토</li><li>인허가 관련 검토</li><li>제조 및 품질관리 검토</li><li>관련 문서 준비 지원</li></ul>
</div>

</div>
</div>
</section>

<section class="contact" id="contact">
<div class="container">
<div class="section-title">
<span class="eng">CONTACT</span>
<h2>문의하기</h2>
<p>제품과 제조환경에 맞는 준비 방향부터 전문적으로 상담해드립니다.</p>
</div>
<div class="contact-box">

<div class="contact-intro">
<h3>궁금한 점이 있으신가요?</h3>
<p>제품과 제조환경에 맞는 준비 방향부터 전문적으로 상담해드립니다.</p>
</div>

<div class="contact-methods">

<div class="contact-method kakao">
<div class="contact-icon">K</div>
<div>
<small>KAKAO TALK</small>
<strong>카카오톡 상담</strong>
</div>
</div>

<div class="contact-method phone">
<div class="contact-icon">☎</div>
<div>
<small>PHONE CONSULTATION</small>
<strong>전화 상담</strong>
</div>
</div>

</div>

<div class="contact-buttons">
<a href="http://pf.kakao.com/_gTXBX/chat" target="_blank" class="btn btn-yellow">
카카오톡 상담하기
</a>
<a href="tel:070-8800-0330" class="btn btn-primary">
☎전화 상담하기
</a>
</div>

<p class="contact-notice"></p>

</div>
</div>
</section>

<footer>
<div class="container footer-inner">
<div><div class="footer-logo">더나은생활연구소</div><p>Better Life Lab</p></div>
<div>© 2026 더나은생활연구소. All Rights Reserved.</div>
</div>
</footer>

<a href="http://pf.kakao.com/_gTXBX/chat" target="_blank" class="kakao-button" aria-label="카카오톡 상담">카카오톡<br>상담</a>

<script>
(function () {
    const sections = document.querySelectorAll("section");

    if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
        sections.forEach(section => section.classList.add("is-visible"));
        return;
    }

    const observer = new IntersectionObserver(
        (entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add("is-visible");
                    entry.target.classList.remove("has-passed");
                    entry.target.classList.add("is-current");
                }
            });
        },
        {
            threshold: 0.12
        }
    );

    sections.forEach(section => observer.observe(section));

    function updatePassedSections() {
        const viewportTop = window.scrollY;
        const viewportBottom = viewportTop + window.innerHeight;

        sections.forEach(section => {
            const rect = section.getBoundingClientRect();
            const top = rect.top + window.scrollY;
            const bottom = top + rect.height;

            if (bottom < viewportTop + 70) {
                section.classList.add("has-passed");
                section.classList.remove("is-current");
            } else if (top < viewportBottom && bottom > viewportTop) {
                section.classList.remove("has-passed");
                section.classList.add("is-visible");
                section.classList.add("is-current");
            } else if (top > viewportBottom) {
                section.classList.remove("has-passed");
                section.classList.remove("is-current");
            }
        });
    }

    window.addEventListener("scroll", updatePassedSections, { passive: true });
    window.addEventListener("resize", updatePassedSections);
    updatePassedSections();
})();
</script>

</body>
</html>
