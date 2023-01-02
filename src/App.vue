<template>
    <nav x-data="{ isOpen: false }" class="relative bg-white dark:bg-gray-800">
        <div class="container px-4 py-6 mx-auto">
            <div class="lg:flex lg:items-center lg:justify-between">
                <div class="flex items-center justify-between">
                    <div class="text-xl font-semibold text-gray-700">
                        <a class="text-2xl font-medium text-sky-500 transition-colors flex items-center duration-300 transform dark:text-sky-400 hover:text-sky-400 dark:hover:text-sky-300" href="#">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.7" stroke="currentColor" class="w-8 h-8">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 7.125C2.25 6.504 2.754 6 3.375 6h6c.621 0 1.125.504 1.125 1.125v3.75c0 .621-.504 1.125-1.125 1.125h-6a1.125 1.125 0 01-1.125-1.125v-3.75zM14.25 8.625c0-.621.504-1.125 1.125-1.125h5.25c.621 0 1.125.504 1.125 1.125v8.25c0 .621-.504 1.125-1.125 1.125h-5.25a1.125 1.125 0 01-1.125-1.125v-8.25zM3.75 16.125c0-.621.504-1.125 1.125-1.125h5.25c.621 0 1.125.504 1.125 1.125v2.25c0 .621-.504 1.125-1.125 1.125h-5.25a1.125 1.125 0 01-1.125-1.125v-2.25z" />
                            </svg>

                            <h3 class="mx-2">Blog</h3>
                        </a>
                    </div>

                    <!-- Mobile menu button -->
                    <div class="flex lg:hidden">
                        <button x-cloak @click="isOpen = !isOpen" type="button" class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
                            <svg x-show="!isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
                            </svg>
                    
                            <svg x-show="isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </button>
                    </div>
                </div>

                <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
                <div x-cloak :class="[isOpen ? 'translate-x-0 opacity-100 ' : 'opacity-0 -translate-x-full']" class="absolute inset-x-0 z-20 w-full px-6 py-4 transition-all duration-300 ease-in-out bg-white dark:bg-gray-800 lg:mt-0 lg:p-0 lg:top-0 lg:relative lg:bg-transparent lg:w-auto lg:opacity-100 lg:translate-x-0 lg:flex lg:items-center">
                    <div class="flex flex-col -mx-6 lg:flex-row lg:items-center">
                        <a href="#" class="px-4 py-1.5 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-lg lg:mt-0 dark:text-gray-200 bg-gray-100 dark:bg-gray-700">Blog</a>
                        <a href="#" class="px-4 py-1.5 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-lg lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Join Slack</a>
                        <a href="#" class="px-4 py-1.5 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-lg lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Browse Topics</a>
                        <a href="#" class="px-4 py-1.5 mx-3 mt-2 text-gray-700 transition-colors duration-300 transform rounded-lg lg:mt-0 dark:text-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700">Random Item</a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <header class=" h-[28rem] bg-gray-50">
        <div class=" container mx-auto px-4 flex h-full py-6 items-center">
            <div class=" max-w-xl">
                <p class=" text-sky-500 uppercase tracking-wider">knowleddge base</p>

                <h2 class=" text-3xl xl:text-4xl font-bold mt-4 text-gray-800 capitalize">All Resurece You Need to grow</h2>

                <p class=" text-gray-500 mt-4 text-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta error odit vel minima optio consequuntur atque omnis, repellendus eos, rerum totam quas vitae voluptatibus, facere distinctio fugit? Nam, iure expedita!</p>
            </div>
        </div>
    </header>

    <section class=" container mx-auto px-4 py-16">
        <div class=" flex items-center justify-between">
            <h2 class=" text-gray-800 font-bold text-3xl">Latest Articles</h2>

            <button class="flex items-center px-4 py-2.5 font-medium tracking-wide text-sky-500 capitalize transition-colors duration-300 transform border border-sky-500 rounded-lg hover:bg-sky-50 focus:outline-none focus:ring focus:ring-sky-300 focus:ring-opacity-80">
                <span class="mx-1">Exploer All</span>

                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 mx-1 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
                </svg>
            </button>
        </div>

        <div class="grid grid-cols-1 gap-8 md:grid-cols-2 mt-12 xl:grid-cols-3">
            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1624996379697-f01d168b1a52?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        What do you want to know about UI
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                John snow
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 1, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1590283603385-17ffb3a7f29f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        All the features you want to know</h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Arthur Melo
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 6, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1597534458220-9fb4969f2df5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        Which services you get from Meraki UI
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Tom Hank
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 19, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class=" container mx-auto px-4 py-10 lg:py-16">
        <div class=" flex items-center justify-between">
            <h2 class=" text-gray-800 font-bold text-3xl">Podcasts</h2>

            <button class="flex items-center px-4 py-2.5 font-medium tracking-wide text-sky-500 capitalize transition-colors duration-300 transform border border-sky-500 rounded-lg hover:bg-sky-50 focus:outline-none focus:ring focus:ring-sky-300 focus:ring-opacity-80">
                <span class="mx-1">Exploer All</span>

                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 mx-1 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
                </svg>
            </button>
        </div>

        <div class="grid grid-cols-1 gap-8 md:grid-cols-2 mt-12 xl:grid-cols-3">
            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcTbDroD8JBly4YN-kttERe-REhf1Ago4jgen2nZFLR0wjm2IKU" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Podcast</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        057: DevTools Mini Series - Interaction
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                John snow
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 1, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Open Episode</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRb1UizkegO75CK7joXI5YU_PyD-PrAKQj2reAOV99r4O5Ic3Y" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Podcast</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        Steal From Other Hobbies
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Jeffrey Way
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 6, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Open Episode</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQe9M4BrVwjAO9HM8h1tNhWJ0iOah_ERztSZKs8D2DrxSexPFs" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Podcast</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        152: Ben Orenstein - How to Stand Out When Applying for a Job at a Small Company
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Adam Wathan
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 19, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Open Episode</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="bg-white dark:bg-gray-900">
        <div class="container px-4 py-10 lg:py-16 mx-auto lg:flex lg:items-center lg:justify-between">
            <h2 class="text-2xl font-semibold tracking-tight text-gray-800 xl:text-3xl dark:text-white">
                Join us and get the update from anywhere
            </h2>

            <div class="mt-8 lg:mt-0">
                <div class="flex flex-col space-y-3 sm:space-y-0 sm:flex-row sm:-mx-2">
                    <input id="email" type="text" class="px-4 py-2 text-gray-700 bg-white border border-gray-200 rounded-md sm:mx-2 dark:bg-gray-900 dark:text-gray-300 dark:border-gray-600 focus:border-sky-400 dark:focus:border-sky-400 focus:ring-sky-300 focus:outline-none focus:ring focus:ring-opacity-40" placeholder="Email Address">

                    <button class="px-4 py-2 text-sm font-medium tracking-wide text-white capitalize transition-colors duration-300 transform bg-sky-500 rounded-md focus:ring focus:ring-sky-300 focus:ring-opacity-80 fo sm:mx-2 hover:bg-sky-400 focus:outline-none focus:bg-sky-400">
                        Get Started
                    </button>
                </div>

                <p class="mt-3 text-sm text-gray-500 dark:text-gray-300">Attention! Offer expires in 30 days. Make sure not to miss this opportunity</p>
            </div>
        </div>
    </section>

    <section class=" container mx-auto px-4 py-10 lg:py-16">
        <div class=" flex items-center justify-between">
            <h2 class=" text-gray-800 font-bold text-3xl">Most Popular</h2>

            <button class="flex items-center px-4 py-2.5 font-medium tracking-wide text-sky-500 capitalize transition-colors duration-300 transform border border-sky-500 rounded-lg hover:bg-sky-50 focus:outline-none focus:ring focus:ring-sky-300 focus:ring-opacity-80">
                <span class="mx-1">Exploer All</span>

                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 mx-1 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
                </svg>
            </button>
        </div>

                <div class="grid grid-cols-1 gap-8 md:grid-cols-2 mt-12 xl:grid-cols-3">
            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1624996379697-f01d168b1a52?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        What do you want to know about UI
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                John snow
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 1, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1590283603385-17ffb3a7f29f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        All the features you want to know</h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Arthur Melo
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 6, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>

                </div>
            </div>

            <div>
                <img class="object-cover object-center w-full h-64 rounded-lg lg:h-80" src="https://images.unsplash.com/photo-1597534458220-9fb4969f2df5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80" alt="">

                <div class="mt-8">
                    <span class="text-sky-500 uppercase tracking-wider">Article</span>

                    <h1 class="mt-4 text-xl font-semibold text-gray-800 dark:text-white truncate">
                        Which services you get from Meraki UI
                    </h1>

                    <p class="mt-2 text-gray-500 dark:text-gray-400">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam est asperiores vel, ab animi
                        recusandae nulla veritatis id tempore sapiente
                    </p>

                    <div class="flex items-center justify-between mt-4">
                        <div>
                            <a href="#" class="text-lg font-medium text-gray-700 dark:text-gray-300 hover:underline hover:text-gray-500">
                                Tom Hank
                            </a>

                            <p class="text-sm text-gray-500 dark:text-gray-400">February 19, 2022</p>
                        </div>

                        <a href="#" class="inline-block text-sky-500 underline hover:text-sky-400">Read more</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer class="bg-white mt-12 dark:bg-gray-900">
        <div class="container px-4 py-12 mx-auto">
            <div class="md:flex md:-mx-3 md:items-center md:justify-between">
                <h1 class="text-3xl font-semibold tracking-tight text-gray-800 md:mx-3 xl:text-4xl dark:text-white">Subscribe our newsletter to get update.</h1>
                
                <div class="mt-6 md:mx-3 shrink-0 md:mt-0 md:w-auto">
                    <a href="#" class="inline-flex items-center justify-center w-full px-4 py-2 text-sm text-white duration-300 bg-sky-500 rounded-lg hover:bg-sky-600 focus:ring focus:ring-sky-300 focus:ring-opacity-80">
                        <span class="mx-2">Sign Up Now</span>

                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6 mx-2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
                        </svg>
                    </a>
                </div>
            </div>
            
            <hr class="my-6 border-gray-200 md:my-10 dark:border-gray-700">

            <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
                <div>
                    <p class="font-semibold text-gray-800 dark:text-white">Quick Link</p>

                    <div class="flex flex-col items-start mt-5 space-y-2">
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Home</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Who We Are</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Our Philosophy</a>
                    </div>
                </div>

                <div>
                    <p class="font-semibold text-gray-800 dark:text-white">Industries</p>

                    <div class="flex flex-col items-start mt-5 space-y-2">
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Retail & E-Commerce</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Information Technology</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Finance & Insurance</a>
                    </div>
                </div>

                <div>
                    <p class="font-semibold text-gray-800 dark:text-white">Services</p>

                    <div class="flex flex-col items-start mt-5 space-y-2">
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Translation</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Proofreading & Editing</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">Content Creation</a>
                    </div>
                </div>

                <div>
                    <p class="font-semibold text-gray-800 dark:text-white">Contact Us</p>

                    <div class="flex flex-col items-start mt-5 space-y-2">
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">+880 768 473 4978</a>
                        <a href="#" class="text-gray-600 transition-colors duration-300 dark:text-gray-300 dark:hover:text-blue-400 hover:underline hover:text-blue-500">info@merakiui.com</a>
                    </div>
                </div>
            </div>
            
            <hr class="my-6 border-gray-200 md:my-10 dark:border-gray-700">
            
            <div class="flex flex-col items-center justify-between sm:flex-row">
                <a class="text-2xl font-medium text-sky-500 transition-colors flex items-center duration-300 transform dark:text-sky-400 hover:text-sky-400 dark:hover:text-sky-300" href="#">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.7" stroke="currentColor" class="w-8 h-8">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 7.125C2.25 6.504 2.754 6 3.375 6h6c.621 0 1.125.504 1.125 1.125v3.75c0 .621-.504 1.125-1.125 1.125h-6a1.125 1.125 0 01-1.125-1.125v-3.75zM14.25 8.625c0-.621.504-1.125 1.125-1.125h5.25c.621 0 1.125.504 1.125 1.125v8.25c0 .621-.504 1.125-1.125 1.125h-5.25a1.125 1.125 0 01-1.125-1.125v-8.25zM3.75 16.125c0-.621.504-1.125 1.125-1.125h5.25c.621 0 1.125.504 1.125 1.125v2.25c0 .621-.504 1.125-1.125 1.125h-5.25a1.125 1.125 0 01-1.125-1.125v-2.25z" />
                    </svg>

                    <h3 class="mx-2">Blog</h3>
                </a>

                <p class="mt-4 text-sm text-gray-500 sm:mt-0 dark:text-gray-300">© Copyright 2021. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {}
</script>
