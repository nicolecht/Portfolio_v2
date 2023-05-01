<template>
  <section>
    <h4>Zoom In</h4>
    <div class="border border-success p-5">
      <div class="card card-body bg-success w-50 mx-auto zoom-in" ref="element">
        <h1 class="text-center">Test Message</h1>
      </div>
    </div>
  </section>
</template>

<style>
.zoom-in:hover {
  animation: zoom-in 2s ease;
  cursor: pointer;
}

@keyframes zoom-in {
  0% {
    transform: scale(1, 1);
  }

  100% {
    transform: scale(1.2, 1.2);
  }
}
</style>