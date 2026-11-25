<script>
  import { photos, apps, sources } from '$lib/data.js';
</script>

<svelte:head>
  <title>Nyawit Hub: tiga jari untuk rakyat</title>
  <meta name="description" content="Satu daerah untuk aplikasi nyawit-dev, dengan salam tiga jari sebagai penanda perjuangan rakyat Indonesia." />
</svelte:head>

<header class="topbar">
  <a class="wordmark" href="#top">NYAWIT / HUB</a>
  <nav aria-label="Navigasi utama">
    <a href="#tentang">Tentang</a>
    <a href="#aplikasi">Aplikasi</a>
    <a href="#jejak">Jejak</a>
    <a href="https://github.com/nyawit-dev" rel="external">GitHub</a>
  </nav>
</header>

<main id="top">
  <section class="hero" aria-labelledby="hero-title">
    <div class="hero-left">
      <p class="deck">Nyawit Hub mengumpulkan aplikasi nyawit-dev dalam satu daerah: katalog, unduhan, dan jejak perjuangan digital.</p>
      <a class="action" href="#aplikasi">Lihat aplikasi</a>
    </div>

    <div class="hero-right">
      <h1 id="hero-title"><span class="line"><span>Tiga jari,</span></span><span class="line"><span>untuk rakyat</span></span></h1>
      <figure class="hero-figure">
        <img src={photos.salute.src} width={photos.salute.width} height={photos.salute.height} alt={photos.salute.alt} fetchpriority="high" />
        <figcaption class="red-block">
          <strong>3</strong>
          <span>jari untuk rakyat</span>
        </figcaption>
      </figure>
    </div>
  </section>

  <section id="tentang" class="section about" aria-labelledby="tentang-title">
    <h2 id="tentang-title" class="axis-title">Salam tiga jari</h2>
    <div class="about-grid">
      <aside class="facts">
        <span>Indonesia</span>
        <span>2026</span>
        <span>Sumber: RRI, NU Online</span>
      </aside>
      <div class="prose">
        <img class="drop" src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
        <p class="lead">Tiga jari muncul ketika rakyat berdiri dan menyampaikan aspirasi. RRI menyebutnya lambang keberanian, solidaritas, dan perlawanan terhadap kekuasaan otoriter. NU Online mencatat salam ini dipakai saat rakyat berbicara kepada pejabat. Kami menaruhnya di sini sebagai penanda. Aplikasi ini lahir dari keinginan melihat Indonesia lebih baik.</p>
        <blockquote>Gerakan rakyat bukan makar. Kami ingin Indonesia menjadi negara yang lebih baik. Kami bukan tak sayang, tapi kami marah negara dikelola orang bodoh.</blockquote>
        <p class="source-line">Sumber: <a href="https://rri.co.id/sorong/regional/2857518/dibalik-tiga-jari-makna-perjuangan-dan-kebebasan" rel="external">RRI</a> dan <a href="https://islam.nu.or.id/khutbah/khutbah-jumat-salam-tiga-jari-dan-pesan-kepedulian-terhadap-rakyat-SRIqk" rel="external">NU Online</a></p>
      </div>
    </div>
  </section>

  <section id="aplikasi" class="section apps-section" aria-labelledby="aplikasi-title">
    <h2 id="aplikasi-title" class="big-title">Aplikasi untuk<br />rakyat</h2>
    <p class="table-word">Rilis</p>
    <div class="apps-layout">
      <figure class="apps-photo">
        <img src={photos.women.src} width={photos.women.width} height={photos.women.height} alt={photos.women.alt} loading="lazy" />
        <figcaption>{photos.women.credit}</figcaption>
      </figure>
      <table>
        <tbody>
          {#each apps as app}
            <tr>
              <td>{app.kind}</td>
              <td><a href={'https://github.com/nyawit-dev/' + app.repo + '/releases/latest'} rel="external">{app.name}</a></td>
              <td>{app.version}</td>
            </tr>
          {/each}
        </tbody>
      </table>
    </div>
  </section>

  <section id="jejak" class="section archive" aria-labelledby="jejak-title">
    <h2 id="jejak-title" class="axis-title">Jejak perjuangan</h2>
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

  <section class="closing" aria-labelledby="closing-title">
    <div class="strip">
      <img src={photos.students.src} width={photos.students.width} height={photos.students.height} alt={photos.students.alt} loading="lazy" />
      <img src={photos.ikj.src} width={photos.ikj.width} height={photos.ikj.height} alt={photos.ikj.alt} loading="lazy" />
      <img src={photos.guerrilla.src} width={photos.guerrilla.width} height={photos.guerrilla.height} alt={photos.guerrilla.alt} loading="lazy" />
    </div>
    <div class="field">
      <h2 id="closing-title">Lima aplikasi. Satu akun. Semua rilis di GitHub.</h2>
      <p><a class="underlined" href="https://github.com/nyawit-dev?tab=repositories" rel="external">Buka rilis terbaru</a></p>
      <p class="field-note">Katalog ini tidak menyimpan data pribadi dan tidak memakai server.</p>
    </div>
  </section>
</main>

<footer class="footer">
  <p class="footer-mark">NYAWIT / HUB</p>
  <div class="footer-links">
    <div class="footer-big">
      <a href="https://github.com/nyawit-dev" rel="external">GitHub</a>
      <a href="https://github.com/nyawit-dev?tab=repositories" rel="external">Releases</a>
      <a href="https://github.com/nyawit-dev/nyawit-launcher/releases/latest" rel="external">Nyawit Launcher</a>
    </div>
    <div class="footer-small">
      <a href="#tentang">Tentang</a>
      <a href="#aplikasi">Aplikasi</a>
      <a href="#jejak">Jejak</a>
      <a href="#jejak">Sumber foto</a>
    </div>
  </div>
  <div class="legal">
    <span>Dibangun dengan SvelteKit dan GitHub Pages</span>
    <a href="#top">Kembali ke atas</a>
  </div>
</footer>
