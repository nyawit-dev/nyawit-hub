<script>
  import { photos, statements, sources } from '$lib/data.js';
</script>

<svelte:head>
  <title>Suara Rakyat Indonesia: tiga jari untuk rakyat</title>
  <meta name="description" content="Halaman untuk menyuarakan suara rakyat Indonesia. Salam tiga jari menjadi penanda aspirasi rakyat." />
</svelte:head>

<header class="topbar">
  <a class="wordmark" href="#top">SUARA RAKYAT / INDONESIA</a>
  <nav aria-label="Navigasi utama">
    <a href="#mengapa">Mengapa</a>
    <a href="#suara">Suara</a>
    <a href="#arsip">Arsip</a>
    <a href="#sumber">Sumber</a>
  </nav>
</header>

<main id="top">
  <section class="hero" aria-labelledby="hero-title">
    <div class="hero-left">
      <p class="kicker">Halaman ini diperuntukkan untuk suara rakyat Indonesia.</p>
      <p class="deck">Salam tiga jari menjadi penanda aspirasi yang disampaikan rakyat kepada negara. Tidak ada katalog. Tidak ada daftar aplikasi. Hanya suara yang ingin didengar.</p>
      <a class="action" href="#suara">Baca suara rakyat</a>
    </div>
    <div class="hero-right">
      <h1 id="hero-title"><span class="line"><span>Tiga jari,</span></span><span class="line"><span>untuk rakyat</span></span></h1>
      <p class="hero-note">Kami bukan tak sayang. Kami marah negara dikelola orang bodoh.</p>
      <figure class="hero-figure">
        <img src={photos.salute.src} width={photos.salute.width} height={photos.salute.height} alt={photos.salute.alt} fetchpriority="high" />
        <figcaption class="red-block"><strong>3</strong><span>jari untuk rakyat</span></figcaption>
      </figure>
    </div>
  </section>

  <section id="mengapa" class="section about" aria-labelledby="mengapa-title">
    <h2 id="mengapa-title" class="axis-title">Kenapa suara ini naik</h2>
    <div class="about-grid">
      <aside class="facts"><span>Indonesia</span><span>2026</span><span>Sumber: RRI, NU Online</span></aside>
      <div class="prose">
        <img class="drop" src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
        <p class="lead">Tiga jari muncul ketika rakyat berdiri dan menyampaikan aspirasi. RRI menyebutnya lambang keberanian, solidaritas, dan perlawanan terhadap kekuasaan otoriter. NU Online mencatat salam ini dipakai saat rakyat berbicara kepada pejabat. Kami menaruhnya di sini sebagai penanda. Aplikasi tidak menjadi urusan halaman ini.</p>
        <blockquote>Gerakan rakyat bukan makar. Kami ingin Indonesia menjadi negara yang lebih baik. Kami bukan tak sayang, tapi kami marah negara dikelola orang bodoh.</blockquote>
        <p class="body-copy">Kalimat itu bukan seruan untuk membenci negeri. Kalimat itu datang dari kepedulian yang sudah terlalu lama dibungkam. Kami menuliskannya apa adanya, tanpa menerjemahkannya menjadi bahasa yang lebih sopan.</p>
        <p class="source-line">Makna salam: <a href="https://rri.co.id/sorong/regional/2857518/dibalik-tiga-jari-makna-perjuangan-dan-kebebasan" rel="external">RRI</a> dan <a href="https://islam.nu.or.id/khutbah/khutbah-jumat-salam-tiga-jari-dan-pesan-kepedulian-terhadap-rakyat-SRIqk" rel="external">NU Online</a></p>
      </div>
    </div>
  </section>

  <section id="suara" class="section voices" aria-labelledby="suara-title">
    <h2 id="suara-title" class="big-title">Yang kami suarakan</h2>
    <p class="section-intro">Empat kalimat ini merangkum suara yang dibawa oleh salam tiga jari di halaman ini. Kalimat pertama dan terakhir berasal langsung dari pemilik halaman.</p>
    <ul class="statements">
      {#each statements as item}
        <li>{item}</li>
      {/each}
    </ul>
  </section>

  <section id="arsip" class="section archive" aria-labelledby="arsip-title">
    <h2 id="arsip-title" class="axis-title">Jejak yang mendahului</h2>
    <p class="archive-intro">Rakyat Indonesia sudah lama berdiri sebelum salam ini viral. Kami meletakkan arsip di samping suara hari ini supaya tidak ada yang mengira kemarahan ini muncul tiba tiba.</p>
    <div class="archive-grid">
      <figure class="archive-photo">
        <img src={photos.montage.src} width={photos.montage.width} height={photos.montage.height} alt={photos.montage.alt} loading="lazy" />
        <figcaption>{photos.montage.credit}</figcaption>
      </figure>
      <ul class="names">
        {#each sources as source}
          <li><a href={source.href} rel="external">{source.label}</a><span>{source.detail}</span></li>
        {/each}
      </ul>
    </div>
  </section>

  <section id="sumber" class="section sources" aria-labelledby="sumber-title">
    <h2 id="sumber-title" class="axis-title">Sumber suara</h2>
    <div class="source-grid">
      <p>RRI menyebut salam tiga jari sebagai lambang keberanian, solidaritas, dan perlawanan terhadap kekuasaan otoriter. NU Online mencatat penggunaannya saat rakyat menyampaikan aspirasi.</p>
      <p>Foto aksi dan arsip berasal dari Wikimedia Commons dengan lisensi CC0, CC BY-SA 4.0, dan public domain. Setiap kredit foto tercantum di bagian Arsip.</p>
    </div>
    <p class="body-copy"><a class="underlined" href="https://rri.co.id/sorong/regional/2857518/dibalik-tiga-jari-makna-perjuangan-dan-kebebasan" rel="external">Baca laporan RRI</a></p>
  </section>

  <section class="closing" aria-labelledby="closing-title">
    <div class="strip">
      <img src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
      <img src={photos.ikj.src} width={photos.ikj.width} height={photos.ikj.height} alt={photos.ikj.alt} loading="lazy" />
      <img src={photos.guerrilla.src} width={photos.guerrilla.width} height={photos.guerrilla.height} alt={photos.guerrilla.alt} loading="lazy" />
    </div>
    <div class="field">
      <h2 id="closing-title">Suara rakyat tidak berhenti di arsip.</h2>
      <p class="field-copy">Ia berlanjut setiap kali orang berani mengangkat tiga jari dan mengatakan bahwa negeri ini harus dikelola lebih baik.</p>
      <p><a class="underlined" href="#sumber">Baca sumbernya</a></p>
    </div>
  </section>
</main>

<footer class="footer">
  <p class="footer-mark">SUARA RAKYAT</p>
  <div class="footer-links">
    <div class="footer-big">
      <a href="#mengapa">Mengapa</a>
      <a href="#suara">Suara</a>
      <a href="#arsip">Arsip</a>
    </div>
    <div class="footer-small">
      <a href="#sumber">Sumber</a>
      <a href="https://rri.co.id/sorong/regional/2857518/dibalik-tiga-jari-makna-perjuangan-dan-kebebasan" rel="external">RRI</a>
      <a href="https://islam.nu.or.id/khutbah/khutbah-jumat-salam-tiga-jari-dan-pesan-kepedulian-terhadap-rakyat-SRIqk" rel="external">NU Online</a>
    </div>
  </div>
  <div class="legal"><span>Halaman suara rakyat, dibangun dengan SvelteKit dan GitHub Pages</span><a href="#top">Kembali ke atas</a></div>
</footer>
