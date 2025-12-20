<template>
  <UDropdownMenu
    v-slot="{ open }"
    :modal="false"
    :items="[{
      label: 'eban-ui',
      to: '/',
      color: 'primary',
      checked: true,
      type: 'checkbox'
    }, {
      label: 'Nuxt UI docs',
      to: 'https://ui.nuxt.com/docs/getting-started/installation/nuxt',
      target: '_blank'
    }, {
      label: 'Component gallery',
      to: 'https://ui.nuxt.com/components/button',
      target: '_blank'
    }, {
      label: 'GitHub',
      to: 'https://github.com/eban/eban-ui',
      target: '_blank'
    }]"
    :content="{ align: 'start' }"
    :ui="{ content: 'min-w-fit' }"
    size="xs"
  >
    <UButton
      label="eban-ui"
      variant="subtle"
      trailing-icon="ph:caret-down-bold"
      size="xs"
      class="-mb-[6px] font-semibold rounded-full truncate"
      :class="[open && 'bg-primary/15']"
      :ui="{
        trailingIcon: ['transition-transform duration-200', open ? 'rotate-180' : undefined].filter(Boolean).join(' ')
      }"
    />
  </UDropdownMenu>
</template>
