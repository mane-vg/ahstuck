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
      align-self: center;
      vertical-align: middle;
      justify-self: center;

      .author {

      }
    }
</style>