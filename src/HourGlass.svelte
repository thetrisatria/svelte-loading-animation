<script>
  export let size = '64px';
  export let color = '#ff3e00'
</script>

<style>
  .hourglass {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    height: var(--size);
    width: var(--size);
  }
  .hourglass div {
    height: calc(var(--size) * .625);
    width: calc(var(--size) * .625);
    animation: hourglass 5s cubic-bezier(.8,0,.2,1) infinite; 
  }
  .hourglass div div:nth-child(1) {
    animation: top 5s linear infinite;
    border-top: calc(var(--size) * .3125) solid var(--color);
    border-right: calc(var(--size) * .3125) solid transparent;
    border-left: calc(var(--size) * .3125) solid transparent;
    height: 0px;
    width: 1px;
    transform-origin: 50% 100%;
  }
  .hourglass div div:nth-child(2) {
    animation: bottom 5s linear infinite;
    border-right: calc(var(--size) * .3125) solid transparent;
    border-bottom: calc(var(--size) * .3125) solid var(--color);
    border-left: calc(var(--size) * .3125) solid transparent;
    height: 0px;
    width: 1px;
    transform: scale(0);
    transform-origin: 50% 100%;
  }
  .hourglass div div:nth-child(3) {
    animation: sand 5s linear infinite;
    border-left: 1px dotted var(--color);
    height: 0px;
    width: 0px;
    position: absolute;
    top: calc(var(--size) * .3125);
    left: calc(var(--size) * .3125);
  }

  @keyframes hourglass {
    90% { transform: rotate(0deg); }
    100% { transform: rotate(180deg); }
  }
  @keyframes top {
    90% { transform: scale(0); }
    100% { transform: scale(0);}
  }
  @keyframes bottom {
    10% { transform: scale(0); }
    90% { transform: scale(1); }
    100% { transform: scale(1); }
  }
  @keyframes sand {
    10% { height: calc(var(--size) * .3125); }
    100% { height: calc(var(--size) * .3125); }
  }
</style>

<div class="hourglass" style="--color:{color};--size:{size}"><div><div></div><div></div><div></div></div></div>