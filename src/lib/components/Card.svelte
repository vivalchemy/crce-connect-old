<script>
  import { Card, Button } from "flowbite-svelte";
  import { ArrowRightOutline } from "flowbite-svelte-icons";

  let hCard = false;
</script>

<div>
  <Card
    img="https://fragnel.edu.in/images/2021/10/2-page-1-crce-building.png"
    href="/"
    horizontal
    reverse={hCard}
    class="mb-4 mx-4"
  >
    <h5
      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
    >
      Noteworthy technology acquisitions 2021
    </h5>
    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
      Here are the biggest enterprise technology acquisitions of 2021 so far, in
      reverse chronological order.
    </p>
  </Card>
</div>
