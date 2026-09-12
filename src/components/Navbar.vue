<script setup lang="ts">    
import { ref } from 'vue'; const mobileMenu = ref(false); const navigation = [{ label: 'About', href: '#about' }, { label: 'Works', href: '#works' }, { label: 'Experience', href: '#experience' }, { label: 'Contact', href: '#contact' }];
</script>
<template>
    <header class="fixed left-0 top-0 z-50 w-full border-b border-line bg-paper/95 backdrop-blur">
        <div class="mx-auto grid max-w-[1440px] grid-cols-12 items-center px-5 md:px-8 lg:px-12"><a href="#home"
                class="col-span-8 py-5 text-sm font-semibold tracking-tight md:col-span-3">FADYA<span
                    class="text-industrial">.</span></a>
            <nav class="col-span-6 hidden justify-center md:flex">
                <ul class="flex items-center gap-8">
                    <li v-for="item in navigation" :key="item.label"><a :href="item.href"
                            class="text-[11px] uppercase tracking-[0.14em] text-muted transition-colors hover:text-industrial">{{
                            item.label }}</a>
                    </li>
                </ul>
            </nav>
            <div class="col-span-4 hidden justify-end md:flex lg:col-span-3">
                <div class="flex items-center gap-2"><span class="h-2 w-2 rounded-full bg-industrial"></span><span
                        class="text-[10px] uppercase tracking-[0.12em] text-muted">Available for work</span></div>
            </div><button class="col-span-4 flex justify-end md:hidden" @click="mobileMenu = !mobileMenu"><span
                    class="text-xs uppercase tracking-[0.15em]">{{ mobileMenu ? 'Close' : 'Menu' }}</span></button>
        </div>
        <div v-if="mobileMenu" class="border-t border-line bg-paper md:hidden">
            <nav class="px-5 py-6">
                <ul class="space-y-5">
                    <li v-for="item in navigation" :key="item.label"><a :href="item.href"
                            class="block text-2xl tracking-editorial" @click="mobileMenu = false">{{ item.label }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>
