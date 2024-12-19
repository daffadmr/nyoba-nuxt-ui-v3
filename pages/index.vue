<template>
  <UModal
    title="Ini Modal"
    v-model:open="modal"
    :close="{
      class: 'rounded-full border border-slate-200',
    }"
  >
    <template #body>
      <Form />
    </template>
  </UModal>
  <USlideover />
  <div class="flex flex-col items-center justify-center h-[90dvh] gap-5">
    <div class="flex gap-5">
      <UButton label="Modal" @click="modal = true" />
      <UButton label="Toast" @click="showToast" />
    </div>
    <div class="bg-slate-100 dark:bg-slate-800 p-2 rounded">
      <UTable sticky :data="data" class="flex-1 max-h-[312px]" />
    </div>
  </div>
</template>

<script setup>
const modal = ref(false);

const toast = useToast();

function showToast() {
  toast.add({
    title: "Success",
    description: "Your action was completed successfully.",
    color: "success",
  });
}

const data = ref([
  {
    id: "4600",
    date: "2024-03-11T15:30:00",
    status: "paid",
    email: "james.anderson@example.com",
    amount: 594,
  },
  {
    id: "4599",
    date: "2024-03-11T10:10:00",
    status: "failed",
    email: "mia.white@example.com",
    amount: 276,
  },
  {
    id: "4598",
    date: "2024-03-11T08:50:00",
    status: "refunded",
    email: "william.brown@example.com",
    amount: 315,
  },
  {
    id: "4597",
    date: "2024-03-10T19:45:00",
    status: "paid",
    email: "emma.davis@example.com",
    amount: 529,
  },
  {
    id: "4596",
    date: "2024-03-10T15:55:00",
    status: "paid",
    email: "ethan.harris@example.com",
    amount: 639,
  },
  {
    id: "4595",
    date: "2024-03-10T15:55:00",
    status: "paid",
    email: "ethan.harris@example.com",
    amount: 639,
  },
  {
    id: "4594",
    date: "2024-03-10T15:55:00",
    status: "paid",
    email: "ethan.harris@example.com",
    amount: 639,
  },
]);
</script>
