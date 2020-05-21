<template>
  <form class="form-download">
    <div class="form-download__line">
      <input type="text" class="form-download__input" placeholder="Your Name" aria-label="Your Name"  />
    </div>
    <div class="form-download__line">
      <input type="email" class="form-download__input" placeholder="Your Email" aria-label="Your Email" name="email" />
    </div>
    <div class="form-download__line">
      <input type="tel" class="form-download__input" placeholder="Phone" aria-label="Phone"  />
    </div>

    <button type="submit" class="btn form-download__submit">Download eBook Now</button>

    <p class="form-download__info">We don’t share your personal info with anyone. <br />   Check out our Policy for more information.</p>
  </form>
</template>

<script>
export default {
  name: 'form-download'
};
</script>