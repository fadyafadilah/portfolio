<script setup lang="ts">
import heroImage from '../images/Hero.jpg';
</script>
<template>
    <section id="home" class="relative min-h-screen border-b border-line pt-24">
        <div class="mx-auto grid min-h-[calc(100vh-6rem)] max-w-[1440px] grid-cols-12 px-5 md:px-8 lg:px-12">
            <div class="col-span-1 hidden border-r border-line pt-10 lg:block"><span
                    class="text-[10px] uppercase tracking-[0.2em] text-muted">01</span></div>
            <div class="col-span-12 lg:col-span-11">
                <div class="grid grid-cols-12 border-b border-line">
                    <div class="col-span-12 py-8 md:col-span-7 lg:py-12">
                        <p class="mb-6 text-[10px] uppercase tracking-[0.2em] text-industrial">Portfolio / 2026</p>
                        <h1
                            class="max-w-5xl text-[clamp(4rem,10vw,10rem)] font-medium leading-[0.82] tracking-editorial">
                            FADYA<br /><span class="ml-[8vw]">FADILAH<span class="text-industrial">.</span></span></h1>
                    </div>
                    <div class="col-span-12 flex items-end border-l border-line p-6 md:col-span-5 md:p-8 lg:p-12">
                        <div class="max-w-sm">
                            <p class="mb-4 text-[10px] uppercase tracking-[0.18em] text-muted">Profile</p>
                            <p class="text-lg leading-relaxed tracking-tight md:text-xl">Fresh Graduate <span class="text-industrial">Full Stack Developer</span></p>
                        </div>
                    </div>
                </div>
                <div class="grid grid-cols-12 border-b border-line">
                    <div class="col-span-12 overflow-hidden md:col-span-9"><img
                            :src="heroImage"
                            alt="Workspace"
                            class="h-[55vh] w-full object-cover grayscale transition duration-700 hover:grayscale-0 md:h-[65vh]" />
                    </div>
                    <div
                        class="col-span-12 flex flex-col justify-between border-l border-line p-6 md:col-span-3 md:p-8">
                        <span class="text-[10px] uppercase tracking-[0.2em] text-muted">Based in</span>
                        <div>
                            <p class="text-3xl tracking-editorial">Indonesia</p>
                            <p class="mt-3 text-xs leading-relaxed text-muted">Building modern web applications for businesses and individuals. With focus on creating efficient and user-friendly solutions.</p>
                        </div><a href="#works" class="text-[10px] uppercase tracking-[0.18em] text-industrial">Explore
                            selected works ↓</a>
                    </div>
                </div>
                <div class="grid grid-cols-2 md:grid-cols-4">
                    <div class="border-r border-line p-5">
                        <p class="text-[9px] uppercase tracking-[0.16em] text-muted">Education</p>
                        <p class="mt-2 text-xs">Informatics Engineering Nusa Putra University</p>
                    </div>
                    <div class="border-r border-line p-5">
                        <p class="text-[9px] uppercase tracking-[0.16em] text-muted">Focus Learning</p>
                        <p class="mt-2 text-xs">Software Development</p>
                    </div>
                    <div class="border-r border-line p-5">
                        <p class="text-[9px] uppercase tracking-[0.16em] text-muted">Programming Languages</p>
                        <p class="mt-2 text-xs">JavaScript · Python · PHP</p>
                    </div>
                    <div class="p-5">
                        <p class="text-[9px] uppercase tracking-[0.16em] text-muted">Status</p>
                        <p class="mt-2 text-xs text-industrial">Open to opportunities</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>