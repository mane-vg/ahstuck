<script>
    let {
      src,
      sources,
      alt,
      caption,
      responsiveSet,
    } = $props();


    let imageWidth;

    function buildSrcset() {
      let _srcset = '';
      if(sources && sources.length > 0) {
        sources.forEach((source, index0) => {
          if(index0 === sources.length - 1) {
            _srcset += source[1] + ' ' + source[0] + 'w';
          } else {
            _srcset += source[1] + ' ' + source[0] + 'w, ';
          }
        });
      }
      return _srcset;
    }
</script>

{#if caption && caption.length > 0}
    <figure>
        <picture bind:clientWidth={imageWidth}>
            <!--{#if responsiveSet == '3x2'}-->
            <!--    <source srcset={src.split('.')[0] + '_1950.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="1950" height="1300">-->
            <!--    <source srcset={src.split('.')[0] + '_1135.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="1135" height="757">-->
            <!--    <source srcset={src.split('.')[0] + '_790.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="790" height="527">-->
            <!--    <source srcset={src.split('.')[0] + '_615.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="615" height="410">-->
            <!--    <source srcset={src.split('.')[0] + '_475.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="475" height="317">-->
            <!--{:else if responsiveSet == '3x4'}-->
            <!--    <source srcset={src.split('.')[0] + '_975.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="975" height="1300">-->
            <!--    <source srcset={src.split('.')[0] + '_568.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="568" height="757">-->
            <!--    <source srcset={src.split('.')[0] + '_395.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="395" height="527">-->
            <!--    <source srcset={src.split('.')[0] + '_308.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="308" height="410">-->
            <!--    <source srcset={src.split('.')[0] + '_238.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="238" height="317">-->
            <!--{:else if responsiveSet == '16x9'}-->
            <!--    <source srcset={src.split('.')[0] + '_3840.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="3840" height="2160">-->
            <!--    <source srcset={src.split('.')[0] + '_1920.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="1920" height="1920">-->
            <!--    <source srcset={src.split('.')[0] + '_1366.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="1366" height="1024">-->
            <!--    <source srcset={src.split('.')[0] + '_1024.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="1024" height="576">-->
            <!--    <source srcset={src.split('.')[0] + '_475.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="475" height="267">-->
            <!--{/if}-->
            <img src={src} srcset={buildSrcset()} alt={alt}>
        </picture>
        <figcaption>
            {@html caption}
        </figcaption>
    </figure>
{:else}
    <picture>
        <!--{#if responsiveSet == '3x2'}-->
        <!--    <source srcset={src.split('.')[0] + '_1950.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="1950" height="1300">-->
        <!--    <source srcset={src.split('.')[0] + '_1135.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="1135" height="757">-->
        <!--    <source srcset={src.split('.')[0] + '_790.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="790" height="527">-->
        <!--    <source srcset={src.split('.')[0] + '_615.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="615" height="410">-->
        <!--    <source srcset={src.split('.')[0] + '_475.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="475" height="317">-->
        <!--{:else if responsiveSet == '3x4'}-->
        <!--    <source srcset={src.split('.')[0] + '_975.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="975" height="1300">-->
        <!--    <source srcset={src.split('.')[0] + '_568.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="568" height="757">-->
        <!--    <source srcset={src.split('.')[0] + '_395.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="395" height="527">-->
        <!--    <source srcset={src.split('.')[0] + '_308.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="308" height="410">-->
        <!--    <source srcset={src.split('.')[0] + '_238.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="238" height="317">-->
        <!--{:else if responsiveSet == '16x9'}-->
        <!--    <source srcset={src.split('.')[0] + '_3840.jpg 1x'} media="all and (min-width: 1920px)" type="image/jpeg" width="3840" height="2160">-->
        <!--    <source srcset={src.split('.')[0] + '_1920.jpg 1x'} media="all and (min-width: 1200px)" type="image/jpeg" width="1920" height="1920">-->
        <!--    <source srcset={src.split('.')[0] + '_1366.jpg 1x'} media="all and (min-width: 992px)" type="image/jpeg" width="1366" height="1024">-->
        <!--    <source srcset={src.split('.')[0] + '_1024.jpg 1x'} media="all and (min-width: 768px)" type="image/jpeg" width="1024" height="576">-->
        <!--    <source srcset={src.split('.')[0] + '_475.jpg 1x'} media="all and (max-width: 475px)" type="image/jpeg" width="475" height="267">-->
        <!--{/if}-->
        <img src={src} srcset={buildSrcset()} alt={alt}>
    </picture>
{/if}

<style>
  figure {
    position: relative;

    display: flex;
    flex-direction: column;

    margin: 0;

    figcaption {
      position: absolute;
      top: calc(var(--gutter-width) / 2);
      left: calc(var(--gutter-width) / 2);

      padding: calc(var(--gutter-width) / 4) calc(var(--gutter-width) / 2);
      background: var(--primary);
      border-radius: calc(var(--gutter-width));

      color: white;
      font-size: var(--font-size-small);
      text-transform: uppercase;
    }
  }

  picture {
    display: block;
    width: 100%;
    height: auto;

    img {
      display: block;
      width: 100%;
      height: auto;
      object-fit: cover;
    }
  }
</style>