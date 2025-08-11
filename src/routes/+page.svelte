<script>
  import { onMount } from 'svelte';
  import { Button } from "$lib/components/ui/button";

  let visible = false;

  onMount(() => {
    visible = true;
  });
</script>

<div class="flex flex-col items-center justify-center p-4 text-slate-900 min-h-[calc(100vh-4rem)]">
  <div class="container mx-auto flex max-w-3xl flex-col items-center justify-center space-y-8 text-center transition-all duration-700 ease-in-out {visible ? 'opacity-100' : 'opacity-0 translate-y-4'}">
    <!-- Logo/Icon -->
    <div class="mb-2">
      <img src="/favicon.png" alt="WiseOwl Tutoring Logo" width="120" height="120" class="mx-auto" />
    </div>

    <!-- Title with subtle animation -->
    <h1 class="text-5xl font-extrabold tracking-tight leading-tight sm:text-6xl md:text-7xl">
      <span class="inline-block animate-fade-in-up opacity-0 text-slate-900" style="animation-delay: 200ms; animation-fill-mode: forwards;">Welcome to</span>
      <br />
      <span class="inline-block animate-fade-in-up bg-gradient-to-r from-purple-700 to-purple-400 bg-clip-text text-transparent opacity-0 pb-2" style="animation-delay: 400ms; animation-fill-mode: forwards;">
        WiseOwl Tutoring
      </span>
    </h1>

    <!-- Subtitle -->
    <p class="max-w-lg text-xl font-medium text-slate-900 animate-fade-in-up opacity-0" style="animation-delay: 600ms; animation-fill-mode: forwards;">
      Empowering students to achieve academic excellence through personalized learning experiences
    </p>

    <!-- Get Started Button -->
    <div class="pt-6 animate-fade-in-up opacity-0" style="animation-delay: 800ms; animation-fill-mode: forwards;">
      <Button variant="default" size="lg" class="px-10 h-14 text-lg font-medium">
        Get Started
      </Button>
    </div>
  </div>
</div>

<style>
  /* Custom animations */
  @keyframes fade-in-up {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .animate-fade-in-up {
    animation: fade-in-up 0.6s ease-out forwards;
  }
</style>
