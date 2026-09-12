<script setup lang="ts">
    import { ref } from 'vue'; import { projects, type Project } from '../data/portfolio'; 
    const selectedProject = ref<Project | null>(null);
</script>
<template>
    <section id="works" class="border-b border-line">
        <div class="mx-auto max-w-[1440px] px-5 md:px-8 lg:px-12">
            <div class="grid grid-cols-12 border-b border-line">
                <div class="col-span-12 py-8 md:col-span-8 md:py-12">
                    <div class="flex items-center gap-4"><span
                            class="text-[10px] uppercase tracking-[0.2em] text-industrial">03</span><span
                            class="text-[10px] uppercase tracking-[0.2em] text-muted">Selected works</span></div>
                    <h2 class="mt-8 max-w-4xl text-[clamp(3rem,7vw,7rem)] leading-[0.85] tracking-editorial">
                        SELECTED<br /><span class="ml-[10vw]">WORKS<span class="text-industrial">.</span></span></h2>
                </div>
                <div class="col-span-12 flex items-end border-l border-line p-6 md:col-span-4 md:p-10">
                    <p class="max-w-xs text-sm leading-6 text-muted">A selection of digital products, interfaces,
                        websites and systems developed through design and technology.</p>
                </div>
            </div>
            <article v-for="project in projects" :key="project.id" class="group grid grid-cols-12 border-b border-line">
                <div class="col-span-2 hidden border-r border-line py-8 md:block"><span
                        class="text-[10px] uppercase tracking-[0.2em] text-muted">{{ project.number }}</span></div>
                <div class="col-span-12 overflow-hidden md:col-span-7"><button class="block h-full w-full text-left"
                        @click="selectedProject = project"><img :src="project.image" :alt="project.title"
                            class="h-[55vw] max-h-[620px] w-full object-cover grayscale transition duration-700 group-hover:scale-[1.025] group-hover:grayscale-0 md:h-[38vw]" /></button>
                </div>
                <div
                    class="col-span-12 flex flex-col justify-between border-l border-line p-6 md:col-span-3 md:p-8 lg:p-10">
                    <div>
                        <div class="mb-10 flex items-center justify-between"><span
                                class="text-[9px] uppercase tracking-[0.18em] text-industrial">{{ project.category }}</span><span
                                class="text-[9px] text-muted">{{ project.year }}</span></div>
                        <h3 class="text-3xl leading-none tracking-editorial md:text-4xl">{{ project.title }}</h3>
                        <p class="mt-6 text-xs leading-6 text-muted">{{ project.description }}</p>
                    </div>
                    <div class="mt-12">
                        <div class="mb-5 flex flex-wrap gap-2"><span v-for="tech in project.technologies" :key="tech"
                                class="border border-line px-2 py-1 text-[9px] uppercase tracking-[0.08em]">{{ tech }}</span>
                        </div><button class="text-[10px] uppercase tracking-[0.15em] hover:text-industrial"
                            @click="selectedProject = project">View project →</button>
                    </div>
                </div>
            </article>
            <div class="grid grid-cols-12">
                <div class="col-span-12 py-8 md:col-span-8">
                    <p class="text-xs text-muted">More projects available on request.</p>
                </div>
                <div class="col-span-12 border-l border-line p-8 md:col-span-4"><a href="#contact"
                        class="text-xs uppercase tracking-[0.15em] text-industrial">Discuss a project →</a></div>
            </div>
        </div>
        <Teleport to="body">
            <div v-if="selectedProject" class="fixed inset-0 z-[100] overflow-y-auto bg-black/60 p-4 md:p-10"
                @click.self="selectedProject = null">
                <div class="mx-auto max-w-5xl bg-paper">
                    <div class="flex items-center justify-between border-b border-line p-5 md:p-7">
                        <div><span
                                class="text-[9px] uppercase tracking-[0.2em] text-industrial">{{ selectedProject.category }}</span>
                            <h3 class="mt-2 text-2xl tracking-editorial">{{ selectedProject.title }}</h3>
                        </div><button class="text-[10px] uppercase tracking-[0.15em]"
                            @click="selectedProject = null">Close ×</button>
                    </div><img :src="selectedProject.image" :alt="selectedProject.title"
                        class="max-h-[70vh] w-full object-cover" />
                    <div class="grid grid-cols-12">
                        <div
                            class="col-span-12 border-b border-line p-6 md:col-span-8 md:border-b-0 md:border-r md:p-10">
                            <p class="text-sm leading-7 text-muted">{{ selectedProject.description }}</p>
                        </div>
                        <div class="col-span-12 p-6 md:col-span-4 md:p-10">
                            <p class="text-[9px] uppercase tracking-[0.18em] text-muted">Technologies</p>
                            <div class="mt-5 space-y-2">
                                <p v-for="tech in selectedProject.technologies" :key="tech" class="text-xs">{{ tech }}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </Teleport>
    </section>
</template>
