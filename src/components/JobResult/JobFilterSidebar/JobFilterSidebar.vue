<template>
  <div
    class="flex flex-col p-4 bg-white border-r border-solid border-brand-gray-1 w-96"
  >
    <section class="pb-5">
      <div class="flex flex-row justify-between">
        <h3 class="my-4 text-base font-semibold">What do You want to do</h3>
        <div class="flex items-center text-sm">
          <action-button text="Clear filters" type="secondary" />
        </div>
      </div>

      <accordion header="Degree" />
      <job-filter-sidebar-checkbox-group
        header="Job Types"
        :unique-values="uniqueJobTypes"
        :mutation="ADD_SELECTED_JOB_TYPES"
      />
      <job-filter-sidebar-checkbox-group
        header="Organizations"
        :unique-values="uniqueOrganizations"
        :mutation="ADD_SELECTED_ORGANIZATIONS"
      />
    </section>
  </div>
</template>

<script>
import Accordion from "../../Shared/Accordion.vue";
import ActionButton from "../../Shared/ActionButton.vue";
import JobFilterSidebarCheckboxGroup from "@/components/JobResult/JobFilterSidebar/JobFilterSidebarCheckboxGroup.vue";

import { useUniqueJobTypes, useUniqueOrganizations } from "@/store/composables";
import {
  ADD_SELECTED_JOB_TYPES,
  ADD_SELECTED_ORGANIZATIONS,
} from "@/store/constants";
export default {
  name: "JobFilterSidebar",
  components: {
    ActionButton,
    Accordion,
    JobFilterSidebarCheckboxGroup,
  },
  setup() {
    const uniqueOrganizations = useUniqueOrganizations();
    const uniqueJobTypes = useUniqueJobTypes();
    return {
      uniqueOrganizations,
      uniqueJobTypes,
      ADD_SELECTED_JOB_TYPES,
      ADD_SELECTED_ORGANIZATIONS,
    };
  },
};
</script>

<style></style>
,
