<template>
    <div class="flex flex-col gap-2">
      <label for="" class="text-[#334054] font-work-sans text-base font-semibold">{{ label }}</label>
      <textarea
        type="text"
        v-bind="$attrs"
        :value="modelValue"
        @input="$emit('update:modelValue', ($event.target as HTMLInputElement).value)"
        class="flex w-[400px] h-[200px] px-2 py-1 items-center border border-[#d0d5dd] rounded-lg"
      />
    </div>
  </template>

<script lang="ts" setup>
defineProps<{
  label: string;
  modelValue: string;
}>();

const emits = defineEmits(['update:modelValue']);
</script>
