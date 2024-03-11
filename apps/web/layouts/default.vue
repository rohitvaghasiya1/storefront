<template>
  <UiNavbarTop filled>
    <nav class="hidden md:flex md:flex-row md:flex-nowrap justify-between w-full">
      <!-- Navbar Link -->
      <ul class="flex items-center gap-4">
        <li>
          <NuxtLink to="#" class="text-blue-950 text-base">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="text-blue-950 text-base">Shop</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="text-blue-950 text-base">FAQs</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="text-blue-950 text-base">Contact Us</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="text-blue-950 text-base">Suggestions</NuxtLink>
        </li>
        <li>
          <NuxtLazyHydrate when-visible>
            <SfButton
              class="group relative"
              :tag="NuxtLink"
              :to="paths.cart"
              :aria-label="$t('numberInCart', cartLineItemsCount)"
              variant="tertiary"
              square
            >
              <template #prefix>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="inline-block w-6 h-6"
                  viewBox="0 0 24 24"
                  data-testid="shopping-cart"
                >
                  <path
                    d="M7 22c-.55 0-1.02-.196-1.412-.587A1.926 1.926 0 0 1 5 20c0-.55.196-1.02.588-1.413A1.926 1.926 0 0 1 7 18c.55 0 1.02.196 1.412.587C8.804 18.98 9 19.45 9 20s-.196 1.02-.588 1.413A1.926 1.926 0 0 1 7 22Zm10 0c-.55 0-1.02-.196-1.412-.587A1.926 1.926 0 0 1 15 20c0-.55.196-1.02.588-1.413A1.926 1.926 0 0 1 17 18c.55 0 1.02.196 1.413.587.391.392.587.863.587 1.413s-.196 1.02-.587 1.413A1.926 1.926 0 0 1 17 22ZM6.15 6l2.4 5h7l2.75-5H6.15ZM7 17c-.75 0-1.317-.33-1.7-.988-.383-.658-.4-1.312-.05-1.962L6.6 11.6 3 4H1.975a.927.927 0 0 1-.7-.288A.99.99 0 0 1 1 3c0-.283.096-.52.288-.712A.968.968 0 0 1 2 2h1.625c.183 0 .358.05.525.15a.93.93 0 0 1 .375.425L5.2 4h14.75c.45 0 .758.167.925.5.167.333.158.683-.025 1.05l-3.55 6.4a2.034 2.034 0 0 1-.725.775A1.93 1.93 0 0 1 15.55 13H8.1L7 15h11.025c.283 0 .517.096.7.287.183.192.275.43.275.713s-.096.52-.288.712A.968.968 0 0 1 18 17H7Z"
                  ></path>
                </svg>
                <SfBadge
                  :content="cartLineItemsCount"
                  class="bg-black flex justify-center text-white"
                  data-testid="cart-badge"
                />
              </template>
            </SfButton>
          </NuxtLazyHydrate>
        </li>
      </ul>
      <div class="flex items-center gap-3">
        <div>
          <h4 class="text-blue-950">Sign In</h4>
        </div>
        <div>
          <div>
            <a href="#" class="p-2 w-12 flex items-center justify-center rounded-lg bg-blue-950">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="inline-block w-4 fill-white bg-blue-950"
                viewBox="0 0 24 24"
                data-testid="shopping-cart"
              >
                <path
                  d="M7 22c-.55 0-1.02-.196-1.412-.587A1.926 1.926 0 0 1 5 20c0-.55.196-1.02.588-1.413A1.926 1.926 0 0 1 7 18c.55 0 1.02.196 1.412.587C8.804 18.98 9 19.45 9 20s-.196 1.02-.588 1.413A1.926 1.926 0 0 1 7 22Zm10 0c-.55 0-1.02-.196-1.412-.587A1.926 1.926 0 0 1 15 20c0-.55.196-1.02.588-1.413A1.926 1.926 0 0 1 17 18c.55 0 1.02.196 1.413.587.391.392.587.863.587 1.413s-.196 1.02-.587 1.413A1.926 1.926 0 0 1 17 22ZM6.15 6l2.4 5h7l2.75-5H6.15ZM7 17c-.75 0-1.317-.33-1.7-.988-.383-.658-.4-1.312-.05-1.962L6.6 11.6 3 4H1.975a.927.927 0 0 1-.7-.288A.99.99 0 0 1 1 3c0-.283.096-.52.288-.712A.968.968 0 0 1 2 2h1.625c.183 0 .358.05.525.15a.93.93 0 0 1 .375.425L5.2 4h14.75c.45 0 .758.167.925.5.167.333.158.683-.025 1.05l-3.55 6.4a2.034 2.034 0 0 1-.725.775A1.93 1.93 0 0 1 15.55 13H8.1L7 15h11.025c.283 0 .517.096.7.287.183.192.275.43.275.713s-.096.52-.288.712A.968.968 0 0 1 18 17H7Z"
                ></path>
              </svg>
            </a>
          </div>
        </div>
      </div>
    </nav>
    <SfButton
      variant="tertiary"
      class="relative text-white hover:text-white active:text-white hover:bg-primary-800 active:bg-primary-900 rounded-md md:hidden"
      square
      @click="searchModalOpen"
      :aria-label="$t('openSearchModalButtonLabel')"
    >
      <SfIconSearch />
    </SfButton>
  </UiNavbarTop>
  <NarrowContainer v-if="breadcrumbs">
    <div class="p-4 md:px-0">
      <LazyUiBreadcrumbs :breadcrumbs="breadcrumbs" />
    </div>
  </NarrowContainer>
  <main>
    <slot />
  </main>
  <NuxtLazyHydrate when-idle>
    <UiNavbarBottom />
  </NuxtLazyHydrate>
  <NuxtLazyHydrate when-visible>
    <UiFooter />
  </NuxtLazyHydrate>
  <NuxtLazyHydrate when-idle>
    <SfModal
      v-model="isSearchModalOpen"
      class="w-full h-full z-50"
      tag="section"
      role="dialog"
      aria-labelledby="search-modal-title"
    >
      <header class="mb-4">
        <SfButton square variant="tertiary" class="absolute right-4 top-2" @click="searchModalClose">
          <SfIconClose class="text-neutral-500" />
        </SfButton>
        <h3 id="search-modal-title" class="absolute left-6 top-4 font-bold typography-headline-4 mb-4">
          {{ $t('search') }}
        </h3>
      </header>
      <UiSearch :close="searchModalClose" />
    </SfModal>
  </NuxtLazyHydrate>
</template>

<script setup lang="ts">
import {
  SfBadge,
  SfButton,
  SfIconExpandMore,
  SfIconShoppingCart,
  SfIconClose,
  SfIconSearch,
  SfIconPerson,
  SfDropdown,
  SfListItem,
  SfModal,
  useDisclosure,
} from '@storefront-ui/vue';
import { DefaultLayoutProps } from '~/layouts/types';

defineProps<DefaultLayoutProps>();

const { isOpen: isAccountDropdownOpen, toggle: accountDropdownToggle } = useDisclosure();
const { isOpen: isSearchModalOpen, open: searchModalOpen, close: searchModalClose } = useDisclosure();
const { fetchCart, data: cart } = useCart();
const { fetchCustomer, data: account } = useCustomer();

fetchCart();
fetchCustomer();
usePageTitle();

const cartLineItemsCount = computed(
  () => cart.value?.lineItems.reduce((total, { quantity }) => total + quantity, 0) ?? 0,
);

const accountDropdown = [
  {
    label: 'account.heading',
    link: paths.account,
  },
  {
    label: 'account.ordersAndReturns.section.myOrders',
    link: paths.accountMyOrders,
  },
  {
    label: 'account.ordersAndReturns.section.returns',
    link: paths.accountReturns,
  },
  {
    label: 'account.logout',
    link: '/',
  },
];
const NuxtLink = resolveComponent('NuxtLink');
</script>
