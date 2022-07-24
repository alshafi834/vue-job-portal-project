<template>
  <accordion header="Organizations">
    <div class="mt-5">
      <fieldset>
        <ul class="flex flex-row flex-wrap">
          <li class="w-1/2 h-8">
            <input id="VueTube" type="checkbox" class="mr-3" />
            <label for="V ueTube">VueTube </label>
          </li>
          <li class="w-1/2 h-8">
            <input id="Between vue and me" type="checkbox" class="mr-3" />
            <label for="Between vue and me">Between vue </label>
          </li>
          <li class="w-1/2 h-8">
            <input id="Et vue brute" type="checkbox" class="mr-3" />
            <label for="Et vue brute">Et Vue </label>
          </li>
          <li class="w-1/2 h-8">
            <input id="Vue half man" type="checkbox" class="mr-3" />
            <label for="Vue half man">Vue half man </label>
          </li>
        </ul>
      </fieldset>
    </div>
  </accordion>
</template>

<script>
import Accordion from "../../Shared/Accordion.vue";
export default {
  name: "JobFilterSidebarOrganizations",
  components: {
    Accordion,
  },
};
</script>

<style></style>
