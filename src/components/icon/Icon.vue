<template>
  <component
    class="svg-icon"
    :class="styles"
    :is="component"
    :width="size"
    :height="size"
  ></component>
</template>

<script setup lang="ts">
import { computed, defineProps } from "vue";
import AddIcon from "./icons/AddIcon.vue";
import ArchiveIcon from "./icons/ArchiveIcon.vue";
import CaretDownIcon from "./icons/CaretDownIcon.vue";
import CheckIcon from "./icons/CheckIcon.vue";
import CheckboxOffIcon from "./icons/CheckboxOffIcon.vue";
import CheckboxOnIcon from "./icons/CheckboxOnIcon.vue";
import CheckCircleIcon from "./icons/CheckCircleIcon.vue";
import ChevronDownIcon from "./icons/ChevronDownIcon.vue";
import ChevronRightIcon from "./icons/ChevronRightIcon.vue";
import ChevronUpIcon from "./icons/ChevronUpIcon.vue";
import CloseIcon from "./icons/CloseIcon.vue";
import DateIcon from "./icons/DateIcon.vue";
import DocIcon from "./icons/DocIcon.vue";
import EditIcon from "./icons/EditIcon.vue";
import ErrorCircleIcon from "./icons/ErrorCircleIcon.vue";
import FileIcon from "./icons/FileIcon.vue";
import HomeIcon from "./icons/HomeIcon.vue";
import InfoIcon from "./icons/InfoIcon.vue";
import PlusCircleIcon from "./icons/PlusCircleIcon.vue";
import PowerIcon from "./icons/PowerIcon.vue";
import SearchIcon from "./icons/SearchIcon.vue";
import TimeIcon from "./icons/TimeIcon.vue";
import TrashIcon from "./icons/TrashIcon.vue";
import UserIcon from "./icons/UserIcon.vue";

const props = defineProps({
  icon: String,
  // sm, md, lg, xl, xxl
  size: {
    type: String,
    default: "md",
  },
  color: {
    type: String,
    default: "common",
  },
});

const component = computed(() => {
  switch (props.icon) {
    case "add":
      return AddIcon;
    case "archive":
      return ArchiveIcon;
    case "caret_down":
      return CaretDownIcon;
    case "check":
      return CheckIcon;
    case "checkbox_off":
      return CheckboxOffIcon;
    case "checkbox_on":
      return CheckboxOnIcon;
    case "check_circle":
      return CheckCircleIcon;
    case "chevron_down":
      return ChevronDownIcon;
    case "chevron_right":
      return ChevronRightIcon;
    case "chevron_up":
      return ChevronUpIcon;
    case "close":
      return CloseIcon;
    case "date":
      return DateIcon;
    case "doc":
      return DocIcon;
    case "edit":
      return EditIcon;
    case "error_circle":
      return ErrorCircleIcon;
    case "file":
      return FileIcon;
    case "home":
      return HomeIcon;
    case "info":
      return InfoIcon;
    case "plus_circle":
      return PlusCircleIcon;
    case "power":
      return PowerIcon;
    case "search":
      return SearchIcon;
    case "time":
      return TimeIcon;
    case "trash":
      return TrashIcon;
    case "user":
      return UserIcon;
    default:
      return null;
  }
});

const size = computed(() => {
  switch (props.size) {
    case "xs":
      return 10;
    case "sm":
      return 12;
    case "md":
      return 14;
    case "lg":
      return 16;
    case "xl":
      return 18;
    case "xxl":
      return 21;
    default:
      return 14;
  }
});

const styles = computed(() => {
  return { ["svg-icon-" + props.color]: true };
});
</script>

<style scoped lang="scss">
.svg-icon {
  display: inline-block;
}

.svg-icon-primary ::v-deep([data-role="main"]) {
  fill: #0f62fe;
}

.svg-icon-common ::v-deep([data-role="main"]) {
  fill: #333333;
}

.svg-icon-white ::v-deep([data-role="main"]) {
  fill: #ffffff;
}

.svg-icon-98 ::v-deep([data-role="main"]) {
  fill: #989898;
}

.svg-icon-c2 ::v-deep([data-role="main"]) {
  fill: #c2c2c2;
}
</style>
