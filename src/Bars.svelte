<script>
  export let size = '64px';
  export let color = '#ff3e00'
</script>

<style>
  .bars {
    display: inline-flex;
    position: relative;
    width: var(--size);
    height: var(--size);
  }
  .bars div {
    display: inline-flex;
    position: absolute;
    left: calc(var(--size) * .1);
    width: calc(var(--size) * .2);
    background: var(--color);
    animation: bars 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
  }
  .bars div:nth-child(1) {
    left: calc(var(--size) * .1);
    animation-delay: -0.24s;
  }
  .bars div:nth-child(2) {
    left: calc(var(--size) * .4);
    animation-delay: -0.12s;
  }
  .bars div:nth-child(3) {
    left: calc(var(--size) * .7);
    animation-delay: 0;
  }
  @keyframes bars {
    0% {
      top: calc(var(--size) * .1);
      height: calc(var(--size) * .8);
    }
    50%, 100% {
      top: calc(var(--size) * .3);
      height: calc(var(--size) * .4);
    }
  }
</style>

<div class="bars" style="--color:{color};--size:{size}"><div></div><div></div><div></div></div>