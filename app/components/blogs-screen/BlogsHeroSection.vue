<script setup>
import { ref, computed } from 'vue';
import Combobox from '@/components/ui/combobox/Combobox.vue';
import ComboboxInput from '@/components/ui/combobox/ComboboxInput.vue';
import ComboboxList from '@/components/ui/combobox/ComboboxList.vue';
import ComboboxItem from '@/components/ui/combobox/ComboboxItem.vue';
import ComboboxEmpty from '@/components/ui/combobox/ComboboxEmpty.vue';

// Example blog items — replace with real data or props as needed
const items = ref([
  { id: 1, label: 'How to maintain oral hygiene' },
  { id: 2, label: 'Tips for first dental visit' },
  { id: 3, label: 'Understanding root canals' },
  { id: 4, label: 'Cosmetic dentistry: what to expect' },
  { id: 5, label: 'Pediatric dental care basics' },
]);

const query = ref('');
const selected = ref(null);

const filtered = computed(() => {
  const q = query.value.trim().toLowerCase();
  if (!q) return items.value;
  return items.value.filter((i) => i.label.toLowerCase().includes(q));
});

function onSelect(value) {
  // `reka-ui` combobox will return the selected value; we store the full item when possible
  const found = items.value.find(
    (i) => String(i.id) === String(value) || i.label === value
  );
  selected.value = found ?? { id: -1, label: String(value) };
}
</script>

<template>
  <div class="items-center text-center py-5 sm:py-4 md:py-5">
    <h1 class="font-semibold text-6xl text-deep-blue mb-5">Blogs</h1>
    <p class="font-regular text-lg text-slate-blue mb-5">
      We use only the best quality materials on the market in order to <br />
      provide the best products to our patients.
    </p>

    <div class="w-full max-w-xs mx-auto">
      <Combobox
        class="w-full outline rounded-sm bg-white"
        @update:value="onSelect"
      >
        <ComboboxInput v-model:value="query" placeholder="Search" />

        <ComboboxList>
          <template v-if="filtered.length">
            <ComboboxItem
              v-for="item in filtered"
              :key="item.id"
              :value="item.id"
            >
              {{ item.label }}
            </ComboboxItem>
          </template>
          <ComboboxEmpty v-else> No results found </ComboboxEmpty>
        </ComboboxList>
      </Combobox>
    </div>

    <p v-if="selected" class="mt-4 text-sm text-muted-foreground">
      Selected: {{ selected.label }}
    </p>
  </div>
</template>
