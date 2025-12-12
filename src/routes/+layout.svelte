<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<!-- Primary Meta Tags -->
	<title>AH Stuck & Design - Ihr Partner für Putz, Stuck und Dämmung</title>
	<meta name="title" content="AH Stuck & Design - Ihr Partner für Putz, Stuck und Dämmung in Laichingen" />
	<meta name="description" content="Stuckateur in Laichingen - Wir bieten handwerkliche Qualität für Putz, Stuck und Innenausbau. Neubau, Renovierung und Sanierung mit modernen Techniken und traditionellem Handwerk." />
	<meta name="keywords" content="Stuckateur, Putz, Stuck, Laichingen, Innenputz, Aussenputz, Trockenbau, Dämmung, Innenausbau, Renovierung, Sanierung, Haßler-Schwenk-Weiss" />
	<meta name="author" content="Haßler-Schwenk-Weiss GbR" />
	<meta name="robots" content="index, follow" />
	<meta name="language" content="DE" />
	<meta name="revisit-after" content="7 days" />

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://ahstuckdesign.de/" />
	<meta property="og:title" content="AH Stuck & Design - Ihr Partner für Putz, Stuck und Dämmung" />
	<meta property="og:description" content="Handwerkliche Qualität und kreative Lösungen für Putz, Stuck und Innenausbau. Neubau, Renovierung oder Sanierung - Ihr Stuckateur in Laichingen." />
	<meta property="og:image" content="https://ahstuckdesign.de/logo_claim.svg" />
	<meta property="og:locale" content="de_DE" />
	<meta property="og:site_name" content="AH Stuck & Design" />

	<!-- Business Contact Information (Schema.org) -->
	<meta property="business:contact_data:street_address" content="Gottlieb-Daimler-Straße 11" />
	<meta property="business:contact_data:locality" content="Laichingen" />
	<meta property="business:contact_data:postal_code" content="89150" />
	<meta property="business:contact_data:country_name" content="Germany" />
	<meta property="business:contact_data:email" content="info@ahstuckdesign.de" />
	<meta property="business:contact_data:phone_number" content="+49 7333 8053144" />

	<!-- Favicon -->
	<link rel="icon" href={favicon} />
	<link rel="canonical" href="https://ahstuckdesign.de/" />
</svelte:head>

<header>
    <a href="#intro" class="is-active"><span>Willkommen</span><div></div></a>
    <a href="#services"><span>Dienstleistungen</span><div></div></a>
    <a href="#work"><span>Arbeiten</span><div></div></a>
    <a href="#customers"><span>Kunden</span><div></div></a>
    <a href="#contact"><span>Kontakt</span><div></div></a>
</header>

{@render children?.()}

<footer class="small">
    <span>© 2025 Haßler-Schwenk-Weiss GbR</span>
    <a href="/impressum">Impressum & Datenschutz</a>
</footer>

<style>
  /* be-vietnam-pro-regular - latin_latin-ext */
  @font-face {
    font-display: swap; /* Check https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display for other options. */
    font-family: 'Be Vietnam Pro Regular';
    font-style: normal;
    font-weight: 400;
    src: url('/fonts/be-vietnam-pro-v12-latin_latin-ext-regular.woff2') format('woff2'); /* Chrome 36+, Opera 23+, Firefox 39+, Safari 12+, iOS 10+ */
  }
  /* be-vietnam-pro-500 - latin_latin-ext */
  @font-face {
    font-display: swap; /* Check https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display for other options. */
    font-family: 'Be Vietnam Pro Medium';
    font-style: normal;
    font-weight: 500;
    src: url('/fonts/be-vietnam-pro-v12-latin_latin-ext-500.woff2') format('woff2'); /* Chrome 36+, Opera 23+, Firefox 39+, Safari 12+, iOS 10+ */
  }
  /* be-vietnam-pro-600 - latin_latin-ext */
  @font-face {
    font-display: swap; /* Check https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display for other options. */
    font-family: 'Be Vietnam Pro SemiBold';
    font-style: normal;
    font-weight: 600;
    src: url('/fonts/be-vietnam-pro-v12-latin_latin-ext-600.woff2') format('woff2'); /* Chrome 36+, Opera 23+, Firefox 39+, Safari 12+, iOS 10+ */
  }
  /* be-vietnam-pro-900 - latin_latin-ext */
  @font-face {
    font-display: swap; /* Check https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-display for other options. */
    font-family: 'Be Vietnam Pro ExtraBold';
    font-style: normal;
    font-weight: 900;
    src: url('/fonts/be-vietnam-pro-v12-latin_latin-ext-900.woff2') format('woff2'); /* Chrome 36+, Opera 23+, Firefox 39+, Safari 12+, iOS 10+ */
  }

    :root {
      --black: #000000;
      --white: #FFFFFF;
      --primary: #BC422C;
      --secondary: #2A5E81;
      --grey-light: #E9E9E9;
      --grey-medium: #D5D5D5;
      --grey-dark: #6F6F6F;

      --font-family-base: 'Be Vietnam Pro Regular';
      --font-family-medium: 'Be Vietnam Pro Medium';
      --font-family-semibold: 'Be Vietnam Pro SemiBold';
      --font-family-bold: 'Be Vietnam Pro ExtraBold';
      --font-size-base: 4vw;
      --font-size-small: calc(0.875 * var(--font-size-base));
      --font-size-lead: calc(1.325 * var(--font-size-base));
      --font-size-h1: calc(3.11 * var(--font-size-base));
      --font-size-h2: calc(1.94 * var(--font-size-base));
      --font-size-h3: calc(1.38 * var(--font-size-base));

      --gutter-width: 20px;

      --transition-duration: 0.25s;

      @media(min-width: 1200px) {
        --font-size-base: 1.25vw;

        --font-size-small: calc(0.875 * var(--font-size-base));
        --font-size-lead: calc(1.325 * var(--font-size-base));
        --font-size-h1: calc(3.11 * var(--font-size-base));
        --font-size-h2: calc(4.16 * var(--font-size-base));
        --font-size-h3: calc(1.39 * var(--font-size-base));

        --gutter-width: 30px;
      }

      @media(min-width: 1925px) {
        --font-size-base: 0.8vw;
      }
    }

  header {
    position: fixed;
    top: 50%;
    right: var(--gutter-width);

    transform: translateY(-50%);

    display: flex;
    flex-direction: column;
    grid-gap: 10px;

    mix-blend-mode: difference;

    text-align: right;

    z-index: 10;

    a {
      position: relative;
      text-decoration: none;

      transition: all 0.5s;
      span {
        color: transparent;
        margin-right: 1em;

        transition: all 0.5s;

        @media(max-width: 1199px) {
          color: transparent;
        }
      }

      div {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        background-color: var(--white);
        width: 5px;
        height: 100%;
        border-radius: 5px;

        opacity: 0.25;
        transition: all 0.5s;
      }

      &.is-active, &:hover {
        span {
          color: var(--white);

          @media(max-width: 1199px) {
            color: transparent;
          }
        }

        div {
          opacity: 1;
        }
      }
    }
  }

  :global(html) {
    scroll-behavior: smooth;
    overflow-x: hidden;
  }

  :global(body) {
    scroll-behavior: smooth;
    margin: 0;

    background-color: var(--grey-light);

    font-family: 'Be Vietnam Pro Regular';
    font-weight: normal;
    font-size: var(--font-size-base);
    line-height: 150%;
    overflow-x: hidden;
  }

    :global(section) {
      position: relative;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: var(--gutter-width);

      margin: calc(var(--gutter-width) * 3.5) var(--gutter-width);

      @media (min-width: 1200px) {
        grid-template-columns: repeat(6, 1fr);

        margin: calc(var(--gutter-width) * 5.5) var(--gutter-width);
      }
    }

    :global(.section--background) {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 20%;
      left: 0;

      background: linear-gradient(180deg, rgba(0, 0, 0, 0.00) 0%, #000 100%);

      z-index: -1;

      :global(img) {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;

        opacity: 0.8;
      }
    }

    :global(h1) {
      font-size: var(--font-size-h1);
      font-family: var(--font-family-semibold);
      font-weight: 500;
      font-style: normal;
      line-height: 1em;
      text-transform: uppercase;
      color: inherit;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(h2) {
      font-size: var(--font-size-h2);
      font-family: var(--font-family-semibold);
      font-weight: 400;
      font-style: normal;
      line-height: 1em;
      color: inherit;
      text-transform: uppercase;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(h3) {
      font-size: var(--font-size-h3);
      font-family: var(--font-family-medium);
      font-weight: 400;
      font-style: normal;
      color: var(--primary);
      text-transform: uppercase;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(h4) {
      font-size: var(--font-size-h4);
      font-weight: 300;
      font-style: normal;
      color: inherit;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(h5) {
      font-size: var(--font-size-h5);
      font-weight: 300;
      font-style: normal;
      color: inherit;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(h6) {
      font-size: var(--font-size-h6);
      font-weight: 500;
      font-style: normal;
      color: inherit;
      margin-top: 0;
      margin-bottom: 1em;
    }

    :global(.lead) {
      font-size: var(--font-size-lead);
    }

  :global(.small) {
    font-size: var(--font-size-small);
  }

  :global(strong) {
    font-family: 'Be Vietnam Pro SemiBold';
  }

  :global(a) {
    color: var(--black);
    text-decoration: underline;

    transition: all 0.5s;

    &:hover {
      text-decoration: none;
    }
  }

  :global(.structure) {
    opacity: 0.1;
    background-blend-mode: hard-light;
    z-index: -1;
  }

  footer {
    display: flex;
    flex-direction: column;
    grid-gap: var(--gutter-width);
    margin: var(--gutter-width);

    @media (min-width: 1200px) {
      flex-direction: row;
      grid-gap: calc(var(--gutter-width) * 2);
    }
  }
</style>