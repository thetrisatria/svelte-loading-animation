<script>
  export let size = '64px';
  export let color = '#ff3e00'
</script>

<style>
.coin {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: var(--size);
  height: var(--size);
  transform: translateZ(calc(var(--size) * .0125));
}
.coin div {
  width: calc(var(--size) * .8);
  height: calc(var(--size) * .8);
  margin: calc(var(--size) * .05);
  border-radius: 50%;
  animation: flipping 2.4s cubic-bezier(0, 0.2, 0.8, 1) infinite;
  background: var(--color)
}

@keyframes flipping {
  0%, 100% {
    animation-timing-function: cubic-bezier(0.5, 0, 1, 0.5);
  }
  0% {
    transform: rotateY(0deg);
  }
  50% {
    transform: rotateY(1800deg);
    animation-timing-function: cubic-bezier(0, 0.5, 0.5, 1);
  }
  100% {
    transform: rotateY(3600deg);
  }
}
</style>

<div class="coin" style="--size:{size};--color:{color}"><div></div></div>