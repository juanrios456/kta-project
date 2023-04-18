<script setup>
import { ref } from 'vue'
import {
  TransitionRoot,
  TransitionChild,
  Dialog,
  DialogPanel,
  DialogTitle,
} from '@headlessui/vue'

const isOpen = ref(false);

function closeModal() {
  isOpen.value = false
}
function openModal() {
  isOpen.value = true
}
</script>

<template>
  <div class=" flex items-center justify-center">
    <button
      type="button"
      @click="openModal"
      class=" footerButton text-[16px] py-[16px] font-[700] px-[32px] text-[#331B3B] bg-[#FBBF24] rounded-lg mt-5"   >
      REQUEST MORE INFORMATION
    </button>
  </div>
  <TransitionRoot appear :show="isOpen" as="template">
    <Dialog as="div" @close="closeModal" class="relative z-10">
      <TransitionChild
        as="template"
        enter="duration-300 ease-out"
        enter-from="opacity-0"
        enter-to="opacity-100"
        leave="duration-200 ease-in"
        leave-from="opacity-100"
        leave-to="opacity-0"
      >
        <div class="fixed inset-0 bg-black bg-opacity-25" />
      </TransitionChild>

      <div class="fixed inset-0 overflow-y-auto">
        <div
          class="flex min-h-full items-center justify-center p-4 text-center"
        >
          <TransitionChild
            as="template"
            enter="duration-300 ease-out"
            enter-from="opacity-0 scale-95"
            enter-to="opacity-100 scale-100"
            leave="duration-200 ease-in"
            leave-from="opacity-100 scale-100"
            leave-to="opacity-0 scale-95"
          >
            <DialogPanel
              class="w-full max-w-[800px] transform overflow-hidden rounded-2xl bg-white p-6 text-left align-middle shadow-xl transition-all"
            >
              <DialogTitle
                as="h3"
                class="font-[700] text-[18px]"
              >
                GET IN TOUCH
              </DialogTitle>
              <div class="mt-2">
                <div class="formTop">
                  <div class="max-[600px]:w-[100%] flex flex-col w-[48%]">
                  <label for="name">Full Name</label><input class=" border-[1px] border-[#331B3B] rounded-lg px-2 py-3" type="text" placeholder="Enter your first and last name"/>
                  </div>
                  <div class="max-[600px]:w-[100%] flex flex-col w-[48%] ">
                  <label for="Email">Email</label><input class=" border-[1px] border-[#331B3B] rounded-lg px-2 py-3" type="text" placeholder="Enter your Email"/>
                  </div>
                </div>
                  <div class="flex flex-col w-[100%]">
                  <label for="message">Message</label><textarea class=" border-[1px] border-[#331B3B] rounded-lg p-2" rows="4" type="text" placeholder="Type in your message"></textarea>
                  </div>
              </div>

              <div class="mt-4">
                <button
                  type="button"
                  class="inline-flex justify-center rounded-lg border border-transparent bg-[#331B3B] px-4 py-2 font-[700] text-[#fff] hover:bg-blue-200 focus:outline-none focus-visible:ring-2 focus-visible:ring-blue-500 focus-visible:ring-offset-2"
                  @click="closeModal"
                >
                Send
                </button>
              </div>
            </DialogPanel>
          </TransitionChild>
        </div>
      </div>
    </Dialog>
  </TransitionRoot>
</template>
<style scoped>
  .formTop{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 2%;
  }
  @media screen and (max-width: 600px) {
    .formTop{
      flex-direction: column;
    }
  }
</style>