<script>
  import { Splide, SplideSlide, SplideTrack } from '@splidejs/svelte-splide';
  import { inview } from 'svelte-inview';

  import Image from '$lib/components/Image.svelte';
  import Quote from "$lib/components/Quote.svelte";
  import {onMount} from "svelte";

  let backgroundImage;
  let heroSection;
  let logo;

  let logoPosition;

  // $effect(() => {
  //   console.log(heroSection.clientHeight - backgroundImage.clientHeight);
  //   logoPosition = heroSection.clientHeight - backgroundImage.clientHeight;
  //   console.log(logoPosition);
  // });

  onMount(() => {
    logoPosition = heroSection.clientHeight - backgroundImage.clientHeight - (logo.clientHeight / 4.25);
    backgroundImage.play();
  });

  function scrollSpy(event) {
    document.querySelectorAll('header a.is-active').forEach((item) => {
      item.classList.remove('is-active');
    });
    document.querySelector('header a[href="#' + event.target.id + '"]').classList.add('is-active');
  }
</script>

<section id="hero" bind:this={heroSection}>
    <video class="section--background" autoplay muted playsinline loop bind:this={backgroundImage}>
        <source src="videos/header.webm" type="video/webm">
        <source src="videos/header.mp4" type="video/mp4">
    </video>
    <img class="logo" src="logo_claim.svg">
    <svg id="logo-large" xmlns="http://www.w3.org/2000/svg" version="1.1" viewBox="0 0 921.8 520" width="921.8" height="520" style="--logo-bottom: {logoPosition}px" bind:this={logo}>
        <defs>
            <pattern id='image' width="1" height="1" viewBox="0 0 100 100" preserveAspectRatio="none">
                <image xlink:href='/images/logo_background.jpg' width="100" height="100" preserveAspectRatio="none"></image>
            </pattern>
        </defs>
        <path class="st0" d="M155,57.2c-14.8-5.2-31.2,2.1-36.6,16.4L0,394.9h60.5L172.1,92.3c5.4-14.2-2.2-29.9-17.1-35.1Z"/>
        <path class="st0" d="M453.1,483.3L265,18c-5.4-14.2-21.8-21.5-36.6-16.3-14.8,5.2-22.4,20.9-17.1,35.1l105.8,261.5h-120.5c-15.8,0-28.6,12.3-28.6,27.4s12.8,27.4,28.6,27.4h142.6l60.3,149c5.4,14.2,21.8,21.5,36.6,16.3,14.8-5.2,22.4-20.9,17.1-35.1Z"/>
        <path class="st0" d="M893.3,54.8c-15.8,0-28.5,12.2-28.5,27.4v187.7h-274.5V27.5c0-15.1-12.8-27.4-28.5-27.4s-28.6,12.3-28.6,27.4v367.4h57.1v-70.3h274.5v125.5c0,15.1,12.8,27.4,28.5,27.4s28.5-12.2,28.5-27.4V82.2c0-15.1-12.8-27.4-28.5-27.4Z"/>
    </svg>
</section>
<main>
    <section id="intro" use:inview on:inview_enter={scrollSpy}>
        <h1>Ihr Partner für Putz, Stuck und Dämmung</h1>
        <p>
            Wir stehen in Laichingen und Umgebung für handwerkliche Qualität, kreative Lösungen
            und eine persönliche Beratung rund um die Themen Putz, Stuck und Innenausbau. Unser
            Ziel ist es, traditionelles Handwerk mit modernen Techniken zu verbinden – für
            Ergebnisse, die sowohl optisch überzeugen als auch langlebig sind. Ob Neubau,
            Renovierung oder Sanierung: Wir begleiten Sie von der Planung bis zur Umsetzung
            und setzen Ihre Vorstellungen detailgenau um.
        </p>
        <Splide options={{
          type: 'loop',
          gap: '20px',
          snap: false,
          fixedWidth: '70%',
          mediaQuery: "min",
          breakpoints: {
            1200: {
              gap: '40px',
              fixedWidth: '27%',
            }
          },
          arrows: false,
          pagination: false,
        }}>
            <SplideSlide>
                <Image src="/images/impressionen_1.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_2.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_3.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_4.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_1.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_2.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_3.jpg"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_4.jpg"/>
            </SplideSlide>
        </Splide>

        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
    </section>
    <section id="services" use:inview on:inview_enter={scrollSpy}>
        <h2>Dienstleistungen</h2>
        <div class="service--wrapper">
            <Image src="/images/innenputz.jpg" responsiveSet="3x2"/>
            <div class="service--text">
                <h3>Innenputz</h3>
                <p>Saubere Wände und ein gesundes Raumklima, wir verputzen Innenräume fachgerecht
                    und schaffen die perfekte Grundlage für Farbe oder Tapete. Wir bieten Ihnen
                    verschiedene Putztechniken – von klassisch bis modern – und beraten Sie, welche
                    Lösung am besten zu Ihren Räumen passt.</p>
            </div>
        </div>
        <div class="service--wrapper">
            <Image src="/images/aussenputz.jpg" responsiveSet="3x2"/>
            <div class="service--text">
                <h3>Aussenputz</h3>
                <p>Schutz und Optik in einem: Unser Außenputz bewahrt Ihre Fassade vor Witterung.
                    Mit moderner Wärmedämmung (WDVS) steigern wir zusätzlich die Energieeffizienz
                    Ihres Hauses.</p>
            </div>
        </div>
        <div class="service--wrapper">
            <Image src="/images/trockenbau.jpg" responsiveSet="3x2"/>
            <div class="service--text">
                <h3>Trockenbau</h3>
                <p>Schnell, flexibel, passgenau: Mit Trockenbauwänden, Decken und Verkleidungen gestalten
                    wir Räume nach Ihren Anforderungen und auf Wunsch auch mit integrierter Wärme- und
                    Schalldämmung.</p>
            </div>
        </div>
        <div class="service--wrapper">
            <Image src="/images/stuck.jpg" responsiveSet="3x2"/>
            <div class="service--text">
                <h3>Stuck</h3>
                <p>Mit Stuckarbeiten verleihen wir Fassaden und Innenräumen eine besondere Note.
                    Von klassischen Profilen über Gesimse bis hin zu modernen Gestaltungen – wir
                    fertigen und montieren Stuckelemente passgenau und langlebig.</p>
            </div>
        </div>
        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
    </section>
    <!--<section id="work" use:inview on:inview_enter={scrollSpy}>
        <h2>Arbeiten</h2>
        <Splide options={{
          type: 'loop',
          gap: '20px',
          fixedWidth: '70%',
          mediaQuery: "min",
          breakpoints: {
            1200: {
              gap: '40px',
              fixedWidth: '27%',
            }
          },
          arrows: false,
          pagination: false,
        }}>
            <SplideSlide>
                <Image src="/images/impressionen_1.jpg" caption="Aussenputz"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_2.jpg" caption="Stuckverkleidung"/>
            </SplideSlide>
            <SplideSlide>
                <Image src="/images/impressionen_3.jpg" caption="Effektputz"/>
            </SplideSlide>
        </Splide>

        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
    </section>-->
    <section id="customers" use:inview on:inview_enter={scrollSpy}>
        <h2>Was unsere Kunden sagen</h2>
        <Splide options={{
          type: 'loop',
          gap: '0',
          fixedWidth: '100%',
          arrows: true,
          pagination: true,
        }}>
            <SplideSlide>
                <Quote quote="Absolut begeistert! Die Renovierung unserer Fassade übertrifft alle Erwartungen. Was für eine makellose Ausführung – pure Perfektion von A bis Z! Danke an das Team von AH Stuck und Design."
                       author="Haustechnik Renner GmbH"/>
            </SplideSlide>
        </Splide>
    </section>
    <section id="praktikum">
        <h2>Praktikum <br/>bei AH Stuck</h2>
        <p>
            Du interessierst dich für handwerkliches Arbeiten und möchtest Einblicke in den Stuckateurberuf gewinnen?
            Wir bieten Schülern und Interessierten die Möglichkeit, ein Praktikum in unserem Betrieb zu absolvieren.
            Lerne unsere Arbeit kennen, sammle praktische Erfahrungen und entdecke, wie viel Kreativität und Präzision in unserem Handwerk steckt.
            Wir freuen uns auf deine Bewerbung: <a href="mailto:info@ahstuckdesign.de"><strong>info@ahstuckdesign.de</strong></a>
        </p>
    </section>
    <section id="contact" use:inview on:inview_enter={scrollSpy}>
        <h2>Erreichen Sie uns, <br/>wenn Sie uns brauchen</h2>
        <p>Als Stuckateur mit langjähriger Erfahrung bieten wir Ihnen hochwertige Handwerksarbeit. Wir freuen uns Ihre
            Anfrage.</p>
        <address>
            <div><span>Telefon</span></div>
            <div><a href="tel:+4973338053144">+49 7333 8053144</a></div>
            <div><span>E-Mail</span></div>
            <div><a href="mailto:info@ahstuckdesign.de">info@ahstuckdesign.de</a></div>
            <div><span>Adresse</span></div>
            <div>
                <p>Gottlieb-Daimler-Straße 11<br/>89150 Laichingen</p>
            </div>
        </address>
        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
        <picture class="structure">
            <source src="/images/structure.avif" type="image/avif"/>
            <source src="/images/structure.webp" type="image/webp"/>
            <img src="/images/structure.png">
        </picture>
    </section>
</main>

<style>
  @import '@splidejs/svelte-splide/css';

  section#hero {
    width: 100%;
    height: 100vh;

    margin: 0;

    .logo {
      position: absolute;
      top: var(--gutter-width);
      left: var(--gutter-width);
    }

    video.section--background {
      width: 100%;
      height: 100%;
      object-position: center;
      object-fit: cover;
    }

    #logo-large {
      position: absolute;
      bottom: calc(var(--logo-bottom) * 1.7);
      left: var(--gutter-width);

      max-width: 80vw;

      @media(min-width: 1200px) {
        bottom: calc(var(--logo-bottom));
      }

      path {
        fill: url(#image);
      }
    }
  }

  section#intro {
    h1 {
      grid-column: 1/4;

      @media (min-width: 1200px) {
        grid-column: 2/5;
      }
    }

    p {
      grid-column: 1/4;
      column-count: 2;

      @media (min-width: 1200px) {
        grid-column: 2/6;
      }
    }

    :global(.splide) {
      grid-column: 1/4;
      grid-row: 4;

      @media (min-width: 1200px) {
        grid-column: 1/7;
      }
    }

    .structure {
      position: absolute;
      &:nth-of-type(1) {
        right: -30vw;
        top: 60vh;
        transform: rotate(45deg);
      }

      &:nth-of-type(2) {
        left: -25vw;
        top: 20vh;
        transform: rotate(-45deg);
      }
    }
  }

  section#services {
    h2 {
      grid-column: 1/4;

      @media (min-width: 1200px) {
        grid-column: 1/4;
      }
    }

    .service--wrapper {
      grid-column: 1/4;

      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: var(--gutter-width);

      @media (min-width: 1200px) {
        grid-column: 1/7;

        grid-template-columns: 1fr 1fr;
      }

      .service--text {
        align-content: end;
      }

      &:nth-of-type(even) {
        grid-column: 1/4;

        @media (min-width: 1200px) {
          grid-column: 2/7;
        }

        :global(picture) {
          grid-column: 2/4;
          grid-row: 1;

          @media (min-width: 1200px) {
            grid-column: 2;
          }
        }

        .service--text {
          grid-column: 1/4;
          grid-row: 2;

          text-align: right;

          @media (min-width: 1200px) {
            grid-column: 1;
            grid-row: 1;

            text-align: unset;
          }
        }
      }

      &:nth-of-type(odd) {
        grid-column: 1/4;

        @media (min-width: 1200px) {
          grid-column: 1/6;
        }

        :global(picture) {
          grid-column: 1/3;
          grid-row: 1;

          @media (min-width: 1200px) {
            grid-column: 1;
          }
        }

        .service--text {
          grid-column: 1/4;
          grid-row: 2;

          @media (min-width: 1200px) {
            grid-column: 2;
            grid-row: 1;
          }
        }
      }

      &:nth-of-type(1) {
        grid-row: 3;

        @media (min-width: 1200px) {
          grid-row: 2/11;
        }
      }

      &:nth-of-type(2) {
        grid-row: 5;

        @media (min-width: 1200px) {
          grid-row: 12/21;
        }

        .service--text {
          align-content: center;
        }
      }

      &:nth-of-type(3) {
        grid-row: 7;

        @media (min-width: 1200px) {
          grid-row: 19/28;
        }

        .service--text {
          align-content: center;
        }
      }

      &:nth-of-type(4) {
        grid-row: 9;

        @media (min-width: 1200px) {
          grid-row: 29/38;
        }
      }
    }

    .structure {
      position: absolute;
      &:nth-of-type(1) {
        left: -35vw;
        top: 90vh;
        transform: rotate(-45deg);
      }

      &:nth-of-type(2) {
        right: -25vw;
        bottom: -30vh;
        transform: rotate(45deg);
      }
    }
  }

  section#work {
    h2 {
      grid-column: 1/4;
      grid-row: 1;

      @media (min-width: 1200px) {
        grid-column: 1/4;
      }
    }

    :global(.splide) {
      grid-column: 1/4;
      grid-row: 2;

      @media (min-width: 1200px) {
        grid-column: 1/7;
      }
    }

    .structure {
      position: absolute;
      &:nth-of-type(1) {
        left: -20vw;
        bottom: 30vh;
        transform: rotate(-45deg);
      }
    }
  }

  section#customers {
    h2 {
      grid-column: 1/4;

      @media (min-width: 1200px) {
        grid-column: 1/4;
      }
    }

    :global(.splide) {
      grid-column: 1/4;
      grid-row: 2;

      @media (min-width: 1200px) {
        grid-column: 2/6;
      }

      :global(.splide__track) {
        margin: 0 2em;

        @media (min-width: 1200px) {
          margin: unset;
        }
      }

      :global(.splide__arrows) {


        :global(.splide__arrow) {
          background: none;
          border: none;

          :global(svg) {
            width: 2em;
            height: 2em;
          }
        }

        :global(.splide__arrow--prev) {
          position: absolute;
          top: 50%;
          left: 0;

          transform: translateY(-50%);

          @media (min-width: 1200px) {
            left: -10em;
          }
        }

        :global(.splide__arrow--next) {
          position: absolute;
          top: 50%;
          right: 0;

          transform: translateY(-50%);

          @media (min-width: 1200px) {
            right: -10em;
          }
        }
      }

      :global(.splide__pagination) {
        position: absolute;
        bottom: -2.5em;
        left: 50%;
        transform: translateX(-50%);
        :global(.splide__pagination__page) {
          width: 30px;
          height: 5px;
          border-radius: 5px;

          background: var(--grey-medium);

          transition: all 0.5s;

          &:global(.is-active) {
            background: var(--black);
            border: none;
            transform: none;
          }
        }
      }
    }
  }

  section#praktikum {
    h2 {
      grid-column: 1/5;
      grid-row: 1;
    }
    p {
      grid-column: 1/5;
      grid-row: 2;
      column-count: 2;

      @media (min-width: 1200px) {
        grid-column: 2/6;
        grid-row: 2;
      }
    }
  }

  section#contact {
    margin: calc(var(--gutter-width) * 3.5) 0 0 0;
    padding: 0 var(--gutter-width) calc(var(--gutter-width) * 5.5) var(--gutter-width);

    overflow: hidden;

    @media (min-width: 1200px) {
      margin: calc(var(--gutter-width) * 5.5) 0 0 0;
      padding: 0 var(--gutter-width) calc(var(--gutter-width) * 5.5) var(--gutter-width);
    }

    h2 {
      grid-column: 1/4;
      grid-row: 1;

      @media (min-width: 1200px) {
        grid-column: 1/6;
      }
    }

    p {
      grid-column: 1/4;
      grid-row: 2;

      @media (min-width: 1200px) {
        grid-column: 3/5;
      }
    }

    address {
      grid-column: 1/4;
      grid-row: 3;

      display: grid;
      grid-template-columns: 1fr 2fr;
      grid-gap: calc(var(--gutter-width) / 4);

      font-style: normal;

      @media (min-width: 1200px) {
        grid-column: 3/5;
      }

      p {
        margin: 0;
      }

      :nth-child(even) {
        grid-column: 2;

        text-align: right;

      font-family: 'Be Vietnam Pro SemiBold';
      font-weight: 600;

        @media (min-width: 1200px) {

        }
      }

      :nth-child(odd) {
        grid-column: 1;

        span {
          text-transform: uppercase;
          color: var(--primary);
          font-family: 'Be Vietnam Pro SemiBold';
          font-weight: 600;
        }

        @media (min-width: 1200px) {

        }
      }
    }

    .structure {
      position: absolute;
      &:nth-of-type(1) {
        left: -30vw;
        bottom: -0vh;
        transform: rotate(-45deg);
      }
      &:nth-of-type(2) {
        right: 0vw;
        bottom: -30vh;
        transform: rotate(45deg);
      }
    }
  }

</style>