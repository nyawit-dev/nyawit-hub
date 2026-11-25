<script>
  import { photos, statements, facts } from '$lib/data.js';

  const groups = [
    { key: 'Dasar Hukum', label: 'Dasar hukum' },
    { key: 'Hak Aspirasi', label: 'Hak menyampaikan aspirasi' },
    { key: 'Makna Salam', label: 'Makna salam tiga jari' },
    { key: 'Data Rakyat', label: 'Data yang tidak bisa diabaikan' },
    { key: 'Linimasa Aspirasi', label: 'Linimasa aspirasi 2024 sampai 2026' },
    { key: 'Arsip Perjuangan', label: 'Arsip perjuangan 1945 sampai 1998' }
  ];

  const byGroup = (key) => facts.filter((f) => f.category === key);
  const legal = byGroup('Dasar Hukum').concat(byGroup('Hak Aspirasi')).concat(byGroup('Makna Salam'));
  const masterSources = [...new Map(facts.map((f) => [f.sourceUrl, f.sourceName])).entries()];
</script>

<svelte:head>
  <title>Suara Rakyat Indonesia: data, arsip, dan aspirasi</title>
  <meta name="description" content="Sarana menyuarakan suara rakyat Indonesia dengan 60 fakta terverifikasi dari 44 sumber, dasar hukum, linimasa aspirasi, dan arsip perjuangan." />
</svelte:head>

<header class="topbar">
  <a class="wordmark" href="#top">SUARA RAKYAT / INDONESIA</a>
  <nav aria-label="Navigasi utama">
    <a href="#mengapa">Mengapa</a>
    <a href="#hak">Hak</a>
    <a href="#data">Data</a>
    <a href="#linimasa">Linimasa</a>
    <a href="#sumber">Sumber</a>
  </nav>
</header>

<main id="top">
  <section class="hero" aria-labelledby="hero-title">
    <div class="hero-left">
      <p class="kicker">Halaman suara rakyat Indonesia.</p>
      <p class="deck">Enam puluh fakta dari 44 sumber. Dasar hukum, makna salam tiga jari, data sosial ekonomi, linimasa aspirasi, dan arsip perjuangan dalam satu tempat.</p>
      <a class="action" href="#data">Baca data rakyat</a>
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
      <aside class="facts"><span>Indonesia</span><span>1945 sampai 2026</span><span>60 fakta, 44 sumber</span></aside>
      <div class="prose">
        <img class="drop" src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
        <p class="lead">Tiga jari muncul ketika rakyat berdiri dan menyampaikan aspirasi. RRI menyebutnya lambang keberanian, solidaritas, dan perlawanan terhadap kekuasaan otoriter. NU Online mencatat salam ini dipakai saat rakyat berbicara kepada pejabat. Kami menaruhnya di sini sebagai penanda.</p>
        <blockquote>Gerakan rakyat bukan makar. Kami ingin Indonesia menjadi negara yang lebih baik. Kami bukan tak sayang, tapi kami marah negara dikelola orang bodoh.</blockquote>
        <p class="body-copy">Halaman ini mengumpulkan data supaya kemarahan tidak berhenti sebagai slogan. Ada dasar hukum, ada angka, ada arsip, ada sumber yang bisa dibuka satu per satu.</p>
      </div>
    </div>
    <ul class="statements">
      {#each statements as item}<li>{item}</li>{/each}
    </ul>
  </section>

  <section id="hak" class="section law" aria-labelledby="hak-title">
    <h2 id="hak-title" class="axis-title">Hak dan makna salam</h2>
    <p class="section-intro">{legal.length} fakta tentang kebebasan berserikat, hak menyampaikan pendapat, dan makna salam tiga jari menurut RRI, NU Online, Liputan6, dan Kompas.</p>
    <ol class="fact-list">
      {#each legal as f, i}
        <li>
          <span class="num">{String(i + 1).padStart(2, '0')}</span>
          <div><h3>{f.topic}</h3><p>{f.claim}</p>{#if f.quote}<p class="quote">{f.quote}</p>{/if}<p class="source"><a href={f.sourceUrl} rel="external">{f.sourceName}</a> {#if f.date}<span>· {f.date}</span>{/if}</p></div>
        </li>
      {/each}
    </ol>
  </section>

  <section id="data" class="section data-section" aria-labelledby="data-title">
    <h2 id="data-title" class="axis-title">Data yang tidak bisa diabaikan</h2>
    <p class="section-intro">Angka berikut diambil dari BPS, Bank Indonesia, World Bank, Transparency International, UNDP, dan kementerian. Tahun dan sumbernya dicantumkan berdampingan.</p>
    <dl class="metrics">
      {#each byGroup('Data Rakyat') as f}
        <div><dt>{f.topic}</dt><dd>{f.claim}</dd><dd class="source"><a href={f.sourceUrl} rel="external">{f.sourceName}</a> {#if f.date}<span>· {f.date}</span>{/if}</dd></div>
      {/each}
    </dl>
  </section>

  <section id="linimasa" class="section timeline-section" aria-labelledby="linimasa-title">
    <h2 id="linimasa-title" class="axis-title">Linimasa aspirasi 2024 sampai 2026</h2>
    <ol class="timeline">
      {#each byGroup('Linimasa Aspirasi') as f}
        <li><span class="when">{f.date}</span><div><h3>{f.topic}</h3><p>{f.claim}</p><p class="source"><a href={f.sourceUrl} rel="external">{f.sourceName}</a></p></div></li>
      {/each}
    </ol>
  </section>

  <section id="arsip" class="section archive" aria-labelledby="arsip-title">
    <h2 id="arsip-title" class="axis-title">Arsip perjuangan 1945 sampai 1998</h2>
    <p class="archive-intro">Rakyat Indonesia sudah lama berdiri sebelum salam ini viral. Arsip di bawah mengingatkan bahwa aspirasi hari ini punya akar panjang.</p>
    <figure class="archive-photo">
      <img src={photos.montage.src} width={photos.montage.width} height={photos.montage.height} alt={photos.montage.alt} loading="lazy" />
      <figcaption>{photos.montage.credit}</figcaption>
    </figure>
    <ol class="timeline light">
      {#each byGroup('Arsip Perjuangan') as f}
        <li><span class="when">{f.date}</span><div><h3>{f.topic}</h3><p>{f.claim}</p><p class="source"><a href={f.sourceUrl} rel="external">{f.sourceName}</a></p></div></li>
      {/each}
    </ol>
  </section>

  <section id="sumber" class="section sources" aria-labelledby="sumber-title">
    <h2 id="sumber-title" class="axis-title">Sumber, {masterSources.length} tautan</h2>
    <p class="section-intro">Setiap fakta di halaman ini bisa ditelusuri. Klik nama sumber untuk membuka dokumen aslinya.</p>
    <ul class="master-sources">
      {#each masterSources as [url, name]}<li><a href={url} rel="external">{name}</a></li>{/each}
    </ul>
  </section>

  <section class="closing" aria-labelledby="closing-title">
    <div class="strip">
      <img src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
      <img src={photos.ikj.src} width={photos.ikj.width} height={photos.ikj.height} alt={photos.ikj.alt} loading="lazy" />
      <img src={photos.guerrilla.src} width={photos.guerrilla.width} height={photos.guerrilla.height} alt={photos.guerrilla.alt} loading="lazy" />
    </div>
    <div class="field">
      <h2 id="closing-title">Suara rakyat tidak berhenti di arsip.</h2>
      <p class="field-copy">Ia berlanjut setiap kali orang berani mengangkat tiga jari, membaca data, lalu meminta negara bekerja lebih baik.</p>
      <p><a class="underlined" href="#sumber">Baca semua sumber</a></p>
    </div>
  </section>
</main>

<footer class="footer">
  <p class="footer-mark">SUARA RAKYAT</p>
  <div class="footer-links">
    <div class="footer-big"><a href="#mengapa">Mengapa</a><a href="#hak">Hak</a><a href="#data">Data</a></div>
    <div class="footer-small"><a href="#linimasa">Linimasa</a><a href="#arsip">Arsip</a><a href="#sumber">Sumber</a></div>
  </div>
  <div class="legal"><span>60 fakta, 44 sumber, dibangun dengan SvelteKit dan GitHub Pages</span><a href="#top">Kembali ke atas</a></div>
</footer>
