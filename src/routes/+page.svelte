<script async script lang="ts" defer>
  import { Section, News, HeroHeader, HeroBody } from "flowbite-svelte-blocks";
  import { ArrowRightSolid } from "flowbite-svelte-icons";
  import { Carousel, Indicator, Button } from "flowbite-svelte";
  import Card from "$lib/components/Card.svelte";
  import { db } from "$lib/firebase/firebase.js";
  import { collection, getDocs } from "firebase/firestore";

  let images: { src: string; alt: string; title: string }[] = [];

  // this
  let image = {
    src: "",
    alt: "",
    title: "",
  };

  const addImage = () => {
    images = [...images, image];
  };

  async function fetchData() {
    try {
      const querySnapshot = await getDocs(
        collection(db, "hall_of_fame_images"),
      );
      querySnapshot.forEach((doc) => {
        const src = doc.data().src;
        const alt = doc.data().alt;
        const title = doc.data().title;
        image = { src: src, alt: alt, title: title };
        addImage();

        // console.log(`src: ${src}`);
        // console.log(`alt: ${alt}`);
        // console.log(`title: ${title}`);
      });
    } catch (error) {
      console.log("Couldn't load data");
    }
  }

  fetchData();
</script>

<!-- hero section -->
<div class="mx-4 flex justify-between">
  <div class="mr-auto place-self-center lg:col-span-7">
    <HeroHeader
      h1Class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white"
      pClass="max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400"
    >
      <svelte:fragment slot="h1"
        >Fr. Conceicao Rodrigues College of Engineering</svelte:fragment
      >
      <svelte:fragment slot="paragraph"
        >The College is Affiliated to the University of Mumbai. Approved by
        AICTE, New Delhi. & Offers UG, PG & Ph.D. Programmes in Technology.The
        College strives to a single goal Moulding Engineers into building the
        nation</svelte:fragment
      >
      <a href="/"
        ><Button
          size="xl"
          color="red"
          class="inline-flex items-center justify-center mr-3"
          >About Us<ArrowRightSolid size="md" class="ml-2 -mr-1" /></Button
        >
      </a>
    </HeroHeader>
  </div>
  <div class="hidden align-end lg:mt-0 lg:col-span-5 lg:flex">
    <img
      src="https://fragnel.edu.in/images/2021/10/2-page-1-crce-building.png"
      alt="mockup"
    />
  </div>
</div>

<section class="">
  <div class=" mt-16 mb-8 w-full text-3xl font-bold flex justify-center">
    CRCE HALL OF FAME
  </div>

  <!-- carousel -->
  <div class=" mx-auto max-w-5xl">
    <Carousel
      {images}
      slideDuration={2500}
      duration={5000}
      transition={null}
      let:Controls
      let:Indicators
    >
      <Controls class="text-slate-900" />
      <Indicators let:selected let:index>
        <Indicator
          color="dark"
          class="relative top-5 w-4 h-4 text-transparent border border-white {selected
            ? 'opacity-100'
            : 'opacity-50'}"
        >
          {index}
        </Indicator>
      </Indicators>
    </Carousel>
  </div>
</section>
<hr class="mt-16 w-4/5 m-auto text-slate-900" />
<!-- social media posts -->
<section class="">
  <div class=" mt-16 mb-8 w-full text-3xl font-bold flex justify-center">
    LATEST POST
  </div>
  <div class="flex overflow-hidden">
    <Card />
  </div>
</section>

