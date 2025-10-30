<script>

    let {
      quote,
      author
    } = $props();
</script>

<div class="quote">
    <p class="lead">{@html quote }</p>
    <span class="author small">{@html author}</span>
</div>

<style>
    .quote {
      position: relative;

      text-align: left;

      .author {

      }
    }
</style>