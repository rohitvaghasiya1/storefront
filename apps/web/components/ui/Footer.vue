<template>
  <footer class="pt-10 bg-neutral-100 mb-[58px] md:mb-0" data-testid="footer">
    <div class="flex justify-center px-4 md:px-6 pb-10 max-w-screen-3xl mx-auto" data-testid="section-top">
      <div class="w-1/4">
        <div class="ml-4 text-lg font-bold leading-7 text-blue-950 font-body">
          {{ $t(`usefulLinks.label`) }}
        </div>
        <ul>
          <SfListItem
            v-for="{ key, link } in usefulLinks"
            :key="key"
            class="!bg-transparent typography-text-sm font-body p-0 gap-0"
          >
            <SfLink
              :tag="NuxtLink"
              class="no-underline text-blue-950 hover:underline font-medium"
              variant="secondary"
              :to="link"
            >
              {{ $t(`usefulLinks.subcategories.${key}`) }}
            </SfLink>
          </SfListItem>
        </ul>
      </div>
      <div class="w-2/4">
        <div class="ml-4 text-lg font-bold leading-7 text-blue-950 font-body">{{ $t(`aboutUs.label`) }}</div>
        <ul>
          <li
            class="inline-flex items-center w-full hover:bg-neutral-100 active:bg-neutral-200 cursor-pointer focus-visible:outline focus-visible:outline-offset focus-visible:relative focus-visible:z-10 px-4 py-2 !bg-transparent typography-text-sm font-body"
          >
            <p class="no-underline text-blue-950 font-medium">{{ $t(`aboutUs.subText.title`) }}</p>
          </li>
          <li
            class="inline-flex items-center w-full hover:bg-neutral-100 active:bg-neutral-200 cursor-pointer focus-visible:outline focus-visible:outline-offset focus-visible:relative focus-visible:z-10 px-4 py-2 !bg-transparent typography-text-sm font-body"
          >
            <p class="no-underline text-blue-950 font-medium">
              {{ $t(`aboutUs.subText.subtitle`) }}
              <span class="font-bold">{{ $t(`aboutUs.subText.sub-subtitle`) }}</span>
            </p>
          </li>
        </ul>
      </div>
      <div class="w-1/4">
        <div class="ml-4 text-lg font-bold leading-7 text-blue-950 font-body">Connect with Us</div>
        <ul>
          <li
            class="inline-flex items-center w-full hover:bg-neutral-100 active:bg-neutral-200 cursor-pointer focus-visible:outline focus-visible:outline-offset focus-visible:relative focus-visible:z-10 px-4 py-2 !bg-transparent typography-text-sm font-body"
          >
            <NuxtLink to="#" class="no-underline text-blue-950 font-medium flex gap-2 items-center">
              <svg
                width="14px"
                height="14px"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                stroke="#00005F"
              >
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <path
                    d="M2.2928 21.292L2.28337 21.3026C1.97175 21.6227 1.91001 22.1115 2.1337 22.4995C2.35966 22.8914 2.82058 23.0828 3.25769 22.9662L9.05302 21.4208C10.1339 21.7963 11.2942 22 12.5 22C18.299 22 23 17.299 23 11.5C23 5.70101 18.299 1 12.5 1C6.70103 1 2.00002 5.70101 2.00002 11.5C2.00002 13.6029 2.61921 15.5638 3.6852 17.2072C3.65453 17.5251 3.60229 17.8896 3.51944 18.3039C3.28993 19.4515 2.95112 20.2289 2.68837 20.7019C2.55663 20.939 2.44292 21.1015 2.36973 21.1972C2.3331 21.2451 2.30653 21.2764 2.2928 21.292Z"
                    fill="#00005F"
                  ></path>
                </g>
              </svg>
              Contact Us</NuxtLink
            >
          </li>
          <li
            class="inline-flex items-center w-full hover:bg-neutral-100 active:bg-neutral-200 cursor-pointer focus-visible:outline focus-visible:outline-offset focus-visible:relative focus-visible:z-10 px-4 py-2 !bg-transparent typography-text-sm font-body"
          >
            <NuxtLink
              to="mailto:custserv@lipic.com"
              class="no-underline text-blue-950 font-medium flex gap-2 items-center"
            >
              <svg
                fill="#00005F"
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                width="14px"
                height="14px"
                viewBox="0 0 512 512"
                xml:space="preserve"
              >
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <g id="7935ec95c421cee6d86eb22ecd12600d">
                    <path
                      style="display: inline"
                      d="M170.591,239.406L1.584,429.263c-0.433-1.911-1.084-3.759-1.084-5.852V88.589 c0-2.541,0.71-4.837,1.356-7.144L170.591,239.406z M493.987,65.524c-1.238-0.277-2.424-0.876-3.79-0.876H21.819 c-1.297,0-2.456,0.599-3.769,0.876l237.961,222.734L493.987,65.524z M262.808,313.021c-1.954,1.869-4.372,2.777-6.797,2.777 c-2.419,0-4.842-0.908-6.775-2.777l-62.21-58.217L16.656,446.145c1.698,0.523,3.364,1.207,5.163,1.207h468.378 c1.89,0,3.534-0.684,5.243-1.207L325.082,254.804L262.808,313.021z M341.494,239.406l168.98,189.836 c0.459-1.911,1.025-3.759,1.025-5.831V88.589c0-2.499-0.62-4.837-1.26-7.133L341.494,239.406z"
                    ></path>
                  </g>
                </g>
              </svg>
              custserv@lipic.com</NuxtLink
            >
          </li>
          <li
            class="inline-flex items-center w-full hover:bg-neutral-100 active:bg-neutral-200 cursor-pointer focus-visible:outline focus-visible:outline-offset focus-visible:relative focus-visible:z-10 px-4 py-2 !bg-transparent typography-text-sm font-body"
          >
            <NuxtLink to="tel:314-775-2500" class="no-underline text-blue-950 font-medium flex gap-2 items-center">
              <svg
                width="14px"
                height="14px"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                stroke="#00005F"
              >
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <path
                    d="M16.5562 12.9062L16.1007 13.359C16.1007 13.359 15.0181 14.4355 12.0631 11.4972C9.10812 8.55901 10.1907 7.48257 10.1907 7.48257L10.4775 7.19738C11.1841 6.49484 11.2507 5.36691 10.6342 4.54348L9.37326 2.85908C8.61028 1.83992 7.13596 1.70529 6.26145 2.57483L4.69185 4.13552C4.25823 4.56668 3.96765 5.12559 4.00289 5.74561C4.09304 7.33182 4.81071 10.7447 8.81536 14.7266C13.0621 18.9492 17.0468 19.117 18.6763 18.9651C19.1917 18.9171 19.6399 18.6546 20.0011 18.2954L21.4217 16.883C22.3806 15.9295 22.1102 14.2949 20.8833 13.628L18.9728 12.5894C18.1672 12.1515 17.1858 12.2801 16.5562 12.9062Z"
                    fill="#00005F"
                  ></path>
                </g>
              </svg>
              314-775-2500</NuxtLink
            >
          </li>
        </ul>
      </div>
    </div>
    <div class="mx-auto bg-gray-200 py-4">
      <div class="max-w-screen-3xl mx-auto px-10">
        <p class="text-sm font-semibold text-gray-400">Copyright © ALDI Merchandise Store</p>
      </div>
    </div>
    <hr />
  </footer>
</template>

<script setup lang="ts">
import { SfLink, SfListItem } from '@storefront-ui/vue';
import { usefulLinks } from '~/mocks';

const NuxtLink = resolveComponent('NuxtLink');
</script>
