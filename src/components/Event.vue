<template>
  <main>
    <h1
      class="text-center pb-6 text-3xl md:text-4xl lg:text-5xl font-semibold text-indigo-500 fascinate"
    >
      Servicios
    </h1>
    <p class="text-gray-600 text-center lg:px-24">
      Creamos estrategias tan únicas como tu marca, potenciando tus fortalezas y
      logrando que la audiencia se enamore de ti, enfocados en el crecimiento de
      tu negocio en internet.
    </p>
    <section class="mt-10 md:flex flex-wrap justify-between gap-5">
      <div class="md:w-5/12 mb-8 md:mb-0 grid place-items-center">
        <img src="/event.png" class="w-6/12 md:w-11/12 lg:w-8/12" />
      </div>
      <template v-for="(event, x) in events" :key="x">
        <div class="md:w-5/12 mb-8 md:mb-0">
          <span class="text-xl text-purple-700 font-medium leading-snug">
            <span class="border-b-2 border-purple-700">{{ x + 1 }}.</span>
            {{ event.title }}
          </span>
          <p class="mt-4">{{ event.content }}</p>
        </div>
      </template>
    </section>

    <!-- <section class="mt-12">
			<p class="text-indigo-500 font-semibold text-xl lg:text-2xl md:text-center mb-5">Para narasumber kita &#128075</p>
			<div class="md:flex justify-evenly gap-6">
				<template v-for="(speaker, x) in speakers" :key="x">
					<CardProfile :profile="speaker" />
				</template>
			</div>
		</section> -->
  </main>
</template>

<script setup>
import events from "@/events.js";
import speakers from "@/speakers.js";
import CardProfile from "@/components/CardProfile.vue";
</script>
