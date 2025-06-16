<script>
    import Navbar from '$lib/Navbar.svelte';
    import { onMount } from 'svelte';
    
    let heroSection;
    let isVisible = false;
    
    onMount(() => {
        // Trigger animations after component mounts
        setTimeout(() => {
            isVisible = true;
        }, 100);
    });
</script>

<Navbar />
 
<main>
    <section bind:this={heroSection} class="relative min-h-screen bg-gradient-to-br from-blue-50 via-blue-100 to-blue-200 flex items-center justify-center overflow-hidden">
        <!-- Animated background elements -->
        <div class="absolute inset-0 overflow-hidden">
            <div class="absolute -top-40 -right-40 w-80 h-80 bg-blue-300 rounded-full mix-blend-multiply filter blur-xl opacity-30 animate-pulse"></div>
            <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-blue-400 rounded-full mix-blend-multiply filter blur-xl opacity-30 animate-pulse"></div>
            <div class="absolute top-40 left-40 w-80 h-80 bg-blue-200 rounded-full mix-blend-multiply filter blur-xl opacity-30 animate-pulse"></div>
        </div>
        
        <!-- Geometric pattern overlay -->
        <div class="absolute inset-0 opacity-5">
            <div class="absolute top-20 left-20 w-4 h-4 bg-blue-600 rotate-45"></div>
            <div class="absolute top-40 right-32 w-6 h-6 bg-blue-700 rotate-12"></div>
            <div class="absolute bottom-32 left-16 w-3 h-3 bg-blue-500 rotate-45"></div>
            <div class="absolute bottom-20 right-20 w-5 h-5 bg-blue-600 rotate-12"></div>
        </div>
        
        <!-- Main content -->
        <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
            <div class="text-center">
                <!-- Greeting -->
                <div class="mb-8 {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-8'} transition-all duration-1000 ease-out">
                    <span class="inline-block px-4 py-2 bg-blue-950 text-blue-100 text-sm font-medium rounded-full shadow-lg">
                        👋 Welcome to my portfolio
                    </span>
                </div>
                
                <!-- Main heading -->
                <h1 class="mb-6 {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} transition-all duration-1000 delay-200 ease-out">
                    <span class="block text-4xl sm:text-6xl lg:text-7xl font-bold text-blue-950 leading-tight">
                        Hi, I'm
                        <span class="relative inline-block">
                            <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 via-blue-700 to-blue-800">
                                Your Name
                            </span>
                            <div class="absolute -bottom-2 left-0 right-0 h-1 bg-gradient-to-r from-blue-400 to-blue-600 rounded-full transform scale-x-0 {isVisible ? 'animate-ping' : ''}"></div>
                        </span>
                    </span>
                </h1>
                
                <!-- Subtitle -->
                <p class="mb-8 text-xl sm:text-2xl lg:text-3xl text-blue-800 font-light max-w-4xl mx-auto leading-relaxed {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} transition-all duration-1000 delay-400 ease-out">
                    Creative Developer & Designer crafting digital experiences that inspire and engage
                </p>
                
                <!-- Description -->
                <p class="mb-12 text-lg text-blue-700 max-w-2xl mx-auto leading-relaxed {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} transition-all duration-1000 delay-600 ease-out">
                    Passionate about building beautiful, functional, and user-centered digital solutions. 
                    Let's create something amazing together.
                </p>
                
                <!-- CTA buttons -->
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} transition-all duration-1000 delay-800 ease-out">
                    <button class="group relative px-8 py-4 bg-blue-950 text-blue-100 font-semibold rounded-full shadow-xl hover:shadow-2xl transform hover:scale-105 transition-all duration-300 overflow-hidden">
                        <span class="relative z-10">View My Work</span>
                        <div class="absolute inset-0 bg-gradient-to-r from-blue-800 to-blue-900 transform scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left"></div>
                    </button>
                    
                    <button class="group px-8 py-4 border-2 border-blue-950 text-blue-950 font-semibold rounded-full hover:bg-blue-950 hover:text-blue-100 transition-all duration-300 transform hover:scale-105">
                        <span class="flex items-center gap-2">
                            Get In Touch
                            <svg class="w-4 h-4 transform group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
                            </svg>
                        </span>
                    </button>
                </div>
                
                <!-- Social links -->
                <div class="mt-16 flex justify-center space-x-6 {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-12'} transition-all duration-1000 delay-1000 ease-out">
                    <a href="#" class="group p-3 bg-white bg-opacity-60 backdrop-blur-sm rounded-full shadow-lg hover:shadow-xl transform hover:scale-110 transition-all duration-300">
                        <svg class="w-6 h-6 text-blue-700 group-hover:text-blue-950 transition-colors duration-300" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/>
                        </svg>
                    </a>
                    <a href="#" class="group p-3 bg-white bg-opacity-60 backdrop-blur-sm rounded-full shadow-lg hover:shadow-xl transform hover:scale-110 transition-all duration-300">
                        <svg class="w-6 h-6 text-blue-700 group-hover:text-blue-950 transition-colors duration-300" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                        </svg>
                    </a>
                    <a href="#" class="group p-3 bg-white bg-opacity-60 backdrop-blur-sm rounded-full shadow-lg hover:shadow-xl transform hover:scale-110 transition-all duration-300">
                        <svg class="w-6 h-6 text-blue-700 group-hover:text-blue-950 transition-colors duration-300" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
        
        <!-- Scroll indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 {isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-4'} transition-all duration-1000 delay-1200 ease-out">
            <div class="flex flex-col items-center">
                <span class="text-blue-700 text-sm font-medium mb-2">Scroll to explore</span>
                <div class="w-6 h-10 border-2 border-blue-300 rounded-full flex justify-center">
                    <div class="w-1 h-3 bg-blue-600 rounded-full mt-2 animate-bounce"></div>
                </div>
            </div>
        </div>
    </section>
</main>