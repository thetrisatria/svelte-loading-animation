<script>
  export let size = '64px';
  export let color = '#ff3e00'
</script>

<style>
  .ellipsis {
    display: inline-flex;
    position: relative;
    width: var(--size);
    height: var(--size);
  }
  .ellipsis div {
    position: absolute;
    top: calc(var(--size) * .4125);
    width: calc(var(--size) * .1625);
    height: calc(var(--size) * .1625);
    border-radius: 50%;
    background: var(--color);
    animation-timing-function: cubic-bezier(0, 1, 1, 0);
  }
  .ellipsis div:nth-child(1) {
    left: calc(var(--size) * .1);
    animation: ellipsis1 0.6s infinite;
  }
  .ellipsis div:nth-child(2) {
    left: calc(var(--size) * .1);
    animation: ellipsis2 0.6s infinite;
  }
  .ellipsis div:nth-child(3) {
    left: calc(var(--size) * .4);
    animation: ellipsis2 0.6s infinite;
  }
  .ellipsis div:nth-child(4) {
    left: calc(var(--size) * .7);
    animation: ellipsis3 0.6s infinite;
  }
  @keyframes ellipsis1 {
    0% {
      transform: scale(0);
    }
    100% {
      transform: scale(1);
    }
  }
  @keyframes ellipsis3 {
    0% {
      transform: scale(1);
    }
    100% {
      transform: scale(0);
    }
  }
  @keyframes ellipsis2 {
    0% {
      transform: translate(0, 0);
    }
    100% {
      transform: translate(calc(var(--size) * .3), 0);
    }
  }
</style>

<div class="ellipsis" style="--size:{size};--color:{color}"><div></div><div></div><div></div><div></div></div>