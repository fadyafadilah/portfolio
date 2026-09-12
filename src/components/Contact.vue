<script setup lang="ts">
import { personalInfo } from '../data/portfolio';
</script>
<template>
    <section id="contact" class="border-b border-line">
        <div class="mx-auto max-w-[1440px] px-5 md:px-8 lg:px-12">
            <div class="grid min-h-[70vh] grid-cols-12">
                <div class="col-span-12 border-b border-line py-8 md:col-span-2 md:border-b-0 md:border-r"><span
                        class="text-[10px] uppercase tracking-[0.2em] text-industrial">05</span></div>
                <div class="col-span-12 flex flex-col justify-between md:col-span-10">
                    <div class="border-b border-line p-6 md:p-12 lg:p-16">
                        <p class="text-[10px] uppercase tracking-[0.2em] text-muted">Contact / Collaboration</p>
                        <h2 class="mt-10 max-w-5xl text-[clamp(3.5rem,9vw,9rem)] leading-[0.8] tracking-editorial">
                            LET'S<br /><span class="ml-[10vw]">TALK<span class="text-industrial">.</span></span></h2>
                    </div>
                    <div class="grid grid-cols-12">
                        <div
                            class="col-span-12 border-b border-line p-6 md:col-span-7 md:border-b-0 md:border-r md:p-12">
                            <p class="max-w-lg text-sm leading-7 text-muted">Have a project, idea, or opportunity? Feel
                                free to reach out. I am interested in working on digital products, websites, interfaces,
                                and technology-driven projects.</p>
                        </div>
                        <div class="col-span-12 md:col-span-5"><a :href="`mailto:${personalInfo.email}`"
                                class="group flex items-center justify-between border-b border-line p-6 transition-colors hover:bg-ink hover:text-white md:p-8">
                                <div><span
                                        class="block text-[9px] uppercase tracking-[0.18em] text-muted group-hover:text-white/50">Email</span><span
                                        class="mt-2 block text-sm">{{ personalInfo.email }}</span></div><span>↗</span>
                            </a><a href="https://github.com/fadyafadilah" target="_blank" rel="noopener noreferrer"
                                class="group flex items-center justify-between border-b border-line p-6 transition-colors hover:bg-ink hover:text-white md:p-8">
                                <div><span
                                        class="block text-[9px] uppercase tracking-[0.18em] text-muted group-hover:text-white/50">GitHub</span><span
                                        class="mt-2 block text-sm">github.com/fadyafadilah</span></div><span>↗</span>
                            </a><a href="https://www.linkedin.com/" target="_blank" rel="noopener noreferrer"
                                class="group flex items-center justify-between p-6 transition-colors hover:bg-ink hover:text-white md:p-8">
                                <div><span
                                        class="block text-[9px] uppercase tracking-[0.18em] text-muted group-hover:text-white/50">LinkedIn</span><span
                                        class="mt-2 block text-sm">LinkedIn Profile</span></div><span>↗</span>
                            </a></div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
