<script setup lang="ts">
    import { experiences } from '../data/portfolio';
</script>
<template>
    <section id="experience" class="border-b border-line">
        <div class="mx-auto grid max-w-[1440px] grid-cols-12 px-5 md:px-8 lg:px-12">
            <div class="col-span-12 border-b border-line py-8 lg:col-span-3 lg:border-b-0 lg:border-r">
                <div class="flex items-center gap-4"><span
                        class="text-[10px] uppercase tracking-[0.2em] text-industrial">04</span><span
                        class="text-[10px] uppercase tracking-[0.2em] text-muted">Experience</span></div>
            </div>
            <div class="col-span-12 lg:col-span-9">
                <div v-for="exp in experiences" :key="exp.company"
                    class="grid grid-cols-12 border-b border-line last:border-b-0">
                    <div class="col-span-3 border-r border-line p-6 md:p-10"><span
                            class="text-[10px] uppercase tracking-[0.15em] text-muted">{{ exp.period }}</span></div>
                    <div class="col-span-9 p-6 md:p-10">
                        <h3 class="text-2xl tracking-editorial md:text-4xl">{{ exp.role }}</h3>
                        <p class="mt-2 text-xs uppercase tracking-[0.12em] text-industrial">{{ exp.company }}</p>
                        <p class="mt-6 max-w-xl text-sm leading-7 text-muted">{{ exp.description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
