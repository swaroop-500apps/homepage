
  <template>
<div class="flex items-center gap-x-6 bg-blue-900 px-6 py-2.5 sm:px-3.5 sm:before:flex-1">
      <p class="text-sm leading-6 text-white d-flex inline-block">
      
        <a href="#"
          >  <img class="h-2 w-auto d-flex inline-block mr-2" src="https://hipsocial.com/lib/images/500appsportal/infinity-white.svg?v=1680093951877334605"><strong class="font-semibold">Join the SaaS Revolution by</strong>  <span style="color: #ffdc00;">500apps</span><strong class="font-semibold">50 Apps for</strong><span class="c-pricing-text pricing-id" style="color: #ffdc00;">$14.99 /user</span></a
        >
      </p>
      <div class="flex flex-1 justify-end">
        <button type="button" class="-m-3 p-3 focus-visible:outline-offset-[-4px]">
          <span class="sr-only">Dismiss</span>
          <XMarkIcon class="h-5 w-5 text-white" aria-hidden="true" />
        </button>
      </div>
    </div>
    <div >
     <header class="bg-white">
       <nav class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8" aria-label="Global">
         <div class="flex lg:flex-1">
           <a href="#" class="-m-1.5 p-1.5">
             <span class="sr-only">Your Company</span>
             <img class="h-9 w-auto" src="https://hipsocial.com/images/logo.svg?v=1680093951877334605" alt="" />
           </a>
         </div>
         <div class="flex lg:hidden">
           <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
             <span class="sr-only">Open main menu</span>
             <Bars3Icon class="h-6 w-6" aria-hidden="true" />
           </button>
         </div>
         <PopoverGroup class="hidden lg:flex lg:gap-x-12">
           <Popover class="relative">
             <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-gray-900">
               Features
               <ChevronDownIcon class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
             </PopoverButton>
   
             <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
               <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-screen max-w-md overflow-hidden rounded-3xl bg-white shadow-lg ring-1 ring-gray-900/5">
                 <div class="p-4">
                   <div v-for="item in products" :key="item.name" class="group relative flex items-center gap-x-6 rounded-lg p-4 text-sm leading-6 hover:bg-gray-50">
                     <div class="flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                       <component :is="item.icon" class="h-6 w-6 text-gray-600 group-hover:text-indigo-600" aria-hidden="true" />
                     </div>
                     <div class="flex-auto">
                       <a :href="item.href" class="block font-semibold text-gray-900">
                         {{ item.name }}
                         <span/>
                       </a>
                       <p class="mt-1 text-gray-600">{{ item.description }}</p>
                     </div>
                   </div>
                 </div>
                 <div class="grid grid-cols-2 divide-x divide-gray-900/5 bg-gray-50">
                   <a v-for="item in callsToAction" :key="item.name" :href="item.href" class="flex items-center justify-center gap-x-2.5 p-3 text-sm font-semibold leading-6 text-gray-900 hover:bg-gray-100">
                     <component :is="item.icon" class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
                     {{ item.name }}
                   </a>
                 </div>
               </PopoverPanel>
             </transition>
           </Popover>
   
           <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Pricing</a>
           <Popover class="relative">
             <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-gray-900">
               Resources
               <ChevronDownIcon class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
             </PopoverButton>
   
             <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
               <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-screen max-w-md overflow-hidden rounded-3xl bg-white shadow-lg ring-1 ring-gray-900/5">
                 <div class="p-4">
                   <div v-for="item in products" :key="item.name" class="group relative flex items-center gap-x-6 rounded-lg p-4 text-sm leading-6 hover:bg-gray-50">
                     <div class="flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                       <component :is="item.icon" class="h-6 w-6 text-gray-600 group-hover:text-indigo-600" aria-hidden="true" />
                     </div>
                     <div class="flex-auto">
                       <a :href="item.href" class="block font-semibold text-gray-900">
                         {{ item.name }}
                         <span class="absolute inset-0" />
                       </a>
                       <p class="mt-1 text-gray-600">{{ item.description }}</p>
                     </div>
                   </div>
                 </div>
                 <div class="grid grid-cols-2 divide-x divide-gray-900/5 bg-gray-50">
                   <a v-for="item in callsToAction" :key="item.name" :href="item.href" class="flex items-center justify-center gap-x-2.5 p-3 text-sm font-semibold leading-6 text-gray-900 hover:bg-gray-100">
                     <component :is="item.icon" class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
                     {{ item.name }}
                   </a>
                 </div>
               </PopoverPanel>
             </transition>
           </Popover>
           <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Login</a>
         </PopoverGroup>
         <div class="hidden lg:flex lg:flex-1 lg:justify-end">
            <button type="button" class="rounded-md bg-indigo-500 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Sign Up</button>

         </div>
       </nav>
       <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
         <div class="fixed inset-0 z-10" />
         <DialogPanel class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
           <div class="flex items-center justify-between">
             <a href="#" class="-m-1.5 p-1.5">
               <span class="sr-only">Your Company</span>
               <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" alt="" />
             </a>
             <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
               <span class="sr-only">Close menu</span>
               <XMarkIcon class="h-6 w-6" aria-hidden="true" />
             </button>
           </div>
           <div class="mt-6 flow-root">
             <div class="-my-6 divide-y divide-gray-500/10">
               <div class="space-y-2 py-6">
                 <Disclosure as="div" class="-mx-3" v-slot="{ open }">
                   <DisclosureButton class="flex w-full items-center justify-between rounded-lg py-2 pl-3 pr-3.5 text-base font-semibold leading-7 hover:bg-gray-50">
                     Product
                     <ChevronDownIcon :class="[open ? 'rotate-180' : '', 'h-5 w-5 flex-none']" aria-hidden="true" />
                   </DisclosureButton>
                   <DisclosurePanel class="mt-2 space-y-2">
                     <DisclosureButton v-for="item in [...products, ...callsToAction]" :key="item.name" as="a" :href="item.href" class="block rounded-lg py-2 pl-6 pr-3 text-sm font-semibold leading-7 text-gray-900 hover:bg-gray-50">{{ item.name }}</DisclosureButton>
                   </DisclosurePanel>
                 </Disclosure>
                 <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Features</a>
                 <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Marketplace</a>
                 <a href="#" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Company</a>
               </div>
               <div class="py-6">
                 <a href="#" class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-gray-900 hover:bg-gray-50">Log in</a>
               </div>
             </div>
           </div>
         </DialogPanel>
       </Dialog>
     </header>
    </div>
    
<div>

  <div class="bg-white py-24 sm:py-32 ">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:mx-0 d-flex inline-block">
        <h1 class="mt-2 text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl ">
Social Media Management Tool
</h1>
<p class="text-base font-semibold leading-9 text-indigo-700">Join the SaaS Revolution -
50 Apps for ₹999</p>
<div>
   
<div class="d-flex align-items-baseline mb-2">
<div class="badge badge-rounded-circle bg-primary mr-2">
<i class="fe fe-check"></i>
</div>
<p class="mb-0">
Access all of your social media platforms from one place - Facebook, Twitter, LinkedIn, Instagram
</p>
</div>
<div class="d-flex align-items-baseline mb-2">
<div class="badge badge-rounded-circle bg-primary mr-2">
<i class="fe fe-check"></i>
</div>
<p class="mb-0">
    Schedule posts with approvals workflow, content calendar, and bulk scheduling tools
</p>
</div>
<div class="d-flex align-items-baseline mb-2">
<div class="badge badge-rounded-circle bg-primary mr-2">
<i class="fe fe-check"></i>
</div>
<p class="mb-0">

    Engage your audience with creative media content using Giphy animations and Pixabay images
</p>
</div>
<div class="d-flex align-items-baseline mb-2">
<div class="badge badge-rounded-circle bg-primary mr-2">
<i class="fe fe-check"></i>
</div>
<p class="mb-0">
    Create posts by scraping content and graphics from your website and blog
</p>
</div>
<div class="d-flex align-items-baseline mb-5">
<div class="badge badge-rounded-circle bg-primary mr-2">
<i class="fe fe-check"></i>
</div>
<p class="mb-0">
    Use AI to write new posts, engage with customers on your social platforms, and get insights into your customers' needs
</p>
</div>
<div class="d-flex inline-block align-items-right mb-2">
    <button type="button" class="rounded-md bg-indigo-800 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"><span>Sign Up</span><small class="trail-text2 d-block">14-day Trial</small>
    </button>
    <p class="d-flex inline-block ml-2">or</p>
    <div class="align-items-center d-flex inline-block">
       <div class="d-flex inline-block ml-2"><img class="h-7 w-7" src="https://hipsocial.com/lib/images/sso-icons/google.svg?v=1680093951877334605"> </div>
       <div class="d-flex inline-block ml-2"><img class="h-7 w-7" src="https://hipsocial.com/lib/images/sso-icons/linkedin.svg?v=1680093951877334605"></div>
       <div class="d-flex inline-block ml-2"><img class="h-7 w-7" src="https://hipsocial.com/lib/images/sso-icons/microsoft.svg?v=1680093951877334605"></div>
       <div class="d-flex inline-block ml-2"><img class="h-7 w-7" src="https://hipsocial.com/lib/images/sso-icons/facebook.svg?v=1680093951877334605"></div>
</div>
<p >No credit card required</p>
</div>
</div>
      </div>
      <div class="d-flex inline-block">
    <object data="https://hipsocial.com/images/social-media-management.svg?v=1680093951877334605" ></object> 
</div>
    </div>
  </div>


</div>




  </template>


<script setup>
import { ref } from 'vue'
import {
  Dialog,
  DialogPanel,
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
} from '@headlessui/vue'
import {
  ArrowPathIcon,
  Bars3Icon,
  ChartPieIcon,
  CursorArrowRaysIcon,
  FingerPrintIcon,
  SquaresPlusIcon,
  XMarkIcon,
} from '@heroicons/vue/24/outline'
import { ChevronDownIcon, PhoneIcon, PlayCircleIcon } from '@heroicons/vue/20/solid'

const products = [
  { name: 'Analytics', description: 'Get a better understanding of your traffic', href: '#', icon: ChartPieIcon },
  { name: 'Engagement', description: 'Speak directly to your customers', href: '#', icon: CursorArrowRaysIcon },
  { name: 'Security', description: 'Your customers’ data will be safe and secure', href: '#', icon: FingerPrintIcon },
  { name: 'Integrations', description: 'Connect with third-party tools', href: '#', icon: SquaresPlusIcon },
  { name: 'Automations', description: 'Build strategic funnels that will convert', href: '#', icon: ArrowPathIcon },
]
const callsToAction = [
  { name: 'Watch demo', href: '#', icon: PlayCircleIcon },
  { name: 'Contact sales', href: '#', icon: PhoneIcon },
]

const mobileMenuOpen = ref(false)
</script>

