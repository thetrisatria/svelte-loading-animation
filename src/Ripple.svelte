<script>
  export let size = '64px';
  export let color = '#ff3e00'
</script>

<style>
  .ripple {
    display: inline-flex;
    position: relative;
    width: var(--size);
    height: var(--size)
  }
  .ripple div {
    position: absolute;
    border: calc(var(--size) * .075) solid var(--color);
    opacity: 1;
    border-radius: 50%;
    animation: ripple 1s cubic-bezier(0, 0.2, 0.8, 1) infinite
  }
  .ripple div:nth-child(2) {
    animation-delay: -0.5s;
  }
  @keyframes ripple {
    0% {
      top: calc(var(--size) * .45);
      left: calc(var(--size) * .45);
      width: 0;
      height: 0;
      opacity: 1;
    }
    100% {
      top: 0px;
      left: 0px;
      width: calc(var(--size) * .9);
      height: calc(var(--size) * .9);
      opacity: 0;
    }
  }
</style>

<div class="ripple" style="--size:{size};--color:{color}"><div></div><div></div></div>

