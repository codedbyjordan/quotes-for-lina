<script lang="ts">
  import { reveal } from "svelte-reveal";

  const quotes = [
    "You have the most beautiful personality.",
    "You make me the happiest person alive.",
    "The shape of your eyes is so pretty.",
    "Thank you for being you.",
    "Please don't ever change for anyone.",
    "I'm always thinking of you.",
    "What's on your mind?",
    "I'll be here you for always.",
    "It's squidy!!!",
    "Websta...",
    "Get it mac, mac, mac, mac, mac, mac, mac",
    "Too many bottles of this wine we can't pronounce.",
    "Mwah!!!",
    "*thinking face*",
    "RAHHHHH...just kidding...",
    "Oh boy...",
    "Rolls royce",
    "Monty and Squidy and Froggy and Jimbo and Jigglypuff and Scrubby",
    "That's literally Kirby...",
    "Play chocolate!!!",
    "I loves you mostest.",
    "Me when I outta",
    "Who's Dick Cheney?",
    "AirPods with a folder.",
    "Without being attracted to any of them",
    "Bitch my name is Johnny",
    "It's all peaches and cream"
  ];

  const rollQuote = () => {
    return quotes[Math.ceil(Math.random() * quotes.length - 1)]
  }

  let quote = rollQuote();
  while(quote === localStorage.getItem('quote')) quote = rollQuote();
  localStorage.setItem('quote', quote);
</script>

<main
  class="w-full h-screen flex justify-center items-center font-hurricane flex-col bg-black text-center"
>
  <h2 class="text-white text-3xl md:text-4xl">Dear Lina,</h2>
  <h1
    class="text-[#d4af37] text-4xl md:text-6xl"
    use:reveal={{ duration: 1250 }}
  >
    {quote}
  </h1>
</main>
