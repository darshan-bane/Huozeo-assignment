<template>
    <div class="w-full bg-white px-4 py-3 rounded-b-xl shadow-md md:rounded-none sticky top-16 bg-white z-10">
        <div class="w-full">
            <!-- DESKTOP -->
            <div class="hidden md:flex items-center gap-3 flex-wrap ">
                <div class="relative flex items-center flex-1 min-w-[200px] bg-sky-700/10 rounded-full">
                    <input type="text" placeholder="Search Place"
                        class="w-full border-2 border-black rounded-full pl-4 pr-10 py-2 text-sm focus:outline-none focus:border-sky-700" />
                    <button class="absolute right-1.5 bg-sky-700 p-1 rounded-full">
                        <svg xmlns="www.w3.org" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="white"
                            stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <circle cx="11" cy="11" r="8"></circle>
                            <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                        </svg>
                    </button>
                </div>

                <div
                    class=" relative cursor-pointer">
                    <button @click="toggleDropdown('For Sale')"
                         class="hover:text-sky-700 flex items-center gap-1 cursor-pointer border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700">For Sale
                        <svg v-if="activeDropdown === 'For Sale'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'For Sale'"
                        class="absolute top-11 left-0 transition w-full z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p class="hover:text-sky-700"> For Sale 1</p>
                        <p class="hover:text-sky-700"> For Sale 2</p>
                        <p class="hover:text-sky-700"> For Sale 3</p>
                    </div>
                </div>

                <div
                    class=" relative cursor-pointer">
                    <button @click="toggleDropdown('Price')"
                        c class="hover:text-sky-700 flex items-center gap-1 cursor-pointer border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700">Price
                        <svg v-if="activeDropdown === 'Price'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'Price'"
                        class="absolute top-11 left-0 transition z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p class="hover:text-sky-700"> Price 1</p>
                        <p class="hover:text-sky-700"> Price 2</p>
                        <p class="hover:text-sky-700"> Price 3</p>
                    </div>
                </div>

                <div
                    class=" relative cursor-pointer">
                    <button @click="toggleDropdown('Beds & Baths')"
                        class="hover:text-sky-700 flex items-center gap-1 cursor-pointer border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700">Beds & Baths
                        <svg v-if="activeDropdown === 'Beds & Baths'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'Beds & Baths'"
                        class="absolute top-11 left-0 transition w-full z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p class="hover:text-sky-700"> Beds & Baths 1</p>
                        <p class="hover:text-sky-700"> Beds & Baths 2</p>
                        <p class="hover:text-sky-700"> Beds & Baths 3</p>
                    </div>
                </div>

                <div class=" relative cursor-pointer">
                    <button @click="toggleDropdown('Property Type')"
                        class="hover:text-sky-700 flex items-center gap-1 cursor-pointer border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700">Property
                        Type
                        <svg v-if="activeDropdown === 'Property Type'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'Property Type'"
                        class="absolute top-11 left-0 transition w-full z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p class="hover:text-sky-700"> Property Type 1</p>
                        <p class="hover:text-sky-700"> Property Type 2</p>
                        <p class="hover:text-sky-700"> Property Type 3</p>
                    </div>
                </div>

                <button
                    class="flex items-center gap-2 border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700 cursor-pointer hover:text-sky-700">
                    <svg id='adjustments-horizontal_20' width='20' height='20' viewBox='0 0 20 20'
                        xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                        <rect width='20' height='20' stroke='none' fill='#000000' opacity='0' />

                        <g transform="matrix(0.83 0 0 0.83 10 10)">
                            <g style="">
                                <g transform="matrix(1 0 0 1 0 0)">
                                    <path
                                        style="stroke: none; stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        transform=" translate(-12, -12)" d="M 0 0 L 24 0 L 24 24 L 0 24 z"
                                        stroke-linecap="round" />
                                </g>
                                <g transform="matrix(1 0 0 1 2 -6)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -4 -6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-4" y1="0" x2="4" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 6 -6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-2" y1="0" x2="2" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 -4 0)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -7 0)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-1" y1="0" x2="1" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 3 0)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-5" y1="0" x2="5" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 5 6)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -2.5 6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-5.5" y1="0" x2="5.5" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 7.5 6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-0.5" y1="0" x2="0.5" y2="0" />
                                </g>
                            </g>
                        </g>
                    </svg> Filters
                </button>

                <button
                    class="flex items-center gap-2 border border-gray-400 rounded-full px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700 cursor-pointer hover:text-sky-700">
                    <svg id='Pencil_20' width='20' height='20' viewBox='0 0 20 20' xmlns='http://www.w3.org/2000/svg'
                        xmlns:xlink='http://www.w3.org/1999/xlink'>
                        <rect width='20' height='20' stroke='none' fill='#000000' opacity='0' />

                        <g transform="matrix(1.3 0 0 1.3 10 10)">
                            <path
                                style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                transform=" translate(-7.85, -8.15)"
                                d="M 12 2.003906 C 11.488281 2.003906 10.972656 2.195313 10.585938 2.585938 L 10.582031 2.585938 L 3.0625 10.234375 L 1.710938 14.292969 L 5.765625 12.9375 L 5.851563 12.855469 L 13.414063 5.414063 C 14.191406 4.636719 14.191406 3.363281 13.414063 2.585938 C 13.027344 2.199219 12.511719 2.003906 12 2.003906 Z M 12 3 C 12.253906 3 12.507813 3.09375 12.707031 3.292969 C 13.101563 3.6875 13.101563 4.3125 12.707031 4.707031 L 11.917969 5.484375 C 11.808594 5.214844 11.632813 4.925781 11.355469 4.648438 C 11.074219 4.367188 10.785156 4.195313 10.515625 4.085938 L 11.296875 3.289063 C 11.492188 3.097656 11.746094 2.996094 12 3 Z M 9.855469 4.929688 C 10.039063 4.945313 10.308594 5.015625 10.644531 5.351563 C 10.984375 5.691406 11.054688 5.960938 11.074219 6.144531 C 11.085938 6.285156 11.066406 6.304688 11.058594 6.328125 L 5.890625 11.410156 C 5.78125 11.164063 5.609375 10.902344 5.351563 10.644531 C 5.097656 10.390625 4.835938 10.21875 4.585938 10.109375 L 9.671875 4.945313 C 9.695313 4.933594 9.714844 4.917969 9.855469 4.929688 Z M 3.898438 10.9375 C 4.054688 10.949219 4.304688 11.011719 4.648438 11.355469 C 4.988281 11.695313 5.050781 11.945313 5.0625 12.097656 C 5.0625 12.117188 5.058594 12.105469 5.0625 12.121094 L 4.109375 12.4375 C 4.03125 12.339844 3.949219 12.242188 3.851563 12.144531 C 3.757813 12.050781 3.660156 11.96875 3.5625 11.894531 L 3.882813 10.9375 C 3.894531 10.941406 3.882813 10.9375 3.898438 10.9375 Z"
                                stroke-linecap="round" />
                        </g>
                    </svg> Saved
                </button>
            </div>

            <!-- MOBILE -->
            <div class="flex md:hidden items-center gap-2">
                <div class="relative flex items-center w-full bg-sky-700/10 rounded-full">
                    <input type="text" placeholder="Search Place"
                        class="w-full border-2 focus:border-sky-700 rounded-full pl-4 pr-10 py-2 text-sm focus:outline-none" />
                    <button class="absolute right-1.5 bg-sky-700 p-1 rounded-full">
                        <svg xmlns="www.w3.org" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="white"
                            stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <circle cx="11" cy="11" r="8"></circle>
                            <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                        </svg>
                    </button>
                </div>


                <button class="border-2 rounded-full border-sky-700 p-2 relative">
                    <svg id='adjustments-horizontal_20' width='20' height='20' viewBox='0 0 20 20'
                        xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                        <rect width='20' height='20' stroke='none' fill='#000000' opacity='0' />

                        <g transform="matrix(0.83 0 0 0.83 10 10)">
                            <g style="">
                                <g transform="matrix(1 0 0 1 0 0)">
                                    <path
                                        style="stroke: none; stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        transform=" translate(-12, -12)" d="M 0 0 L 24 0 L 24 24 L 0 24 z"
                                        stroke-linecap="round" />
                                </g>
                                <g transform="matrix(1 0 0 1 2 -6)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -4 -6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-4" y1="0" x2="4" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 6 -6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-2" y1="0" x2="2" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 -4 0)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -7 0)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-1" y1="0" x2="1" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 3 0)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-5" y1="0" x2="5" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 5 6)">
                                    <circle
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        cx="0" cy="0" r="2" />
                                </g>
                                <g transform="matrix(1 0 0 1 -2.5 6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-5.5" y1="0" x2="5.5" y2="0" />
                                </g>
                                <g transform="matrix(1 0 0 1 7.5 6)">
                                    <line
                                        style="stroke: rgb(33,33,33); stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; stroke-miterlimit: 4; fill: none; fill-rule: nonzero; opacity: 1;"
                                        x1="-0.5" y1="0" x2="0.5" y2="0" />
                                </g>
                            </g>
                        </g>
                    </svg>
                    <span class="absolute -top-1 -right-1 bg-sky-700 text-white text-xs rounded-full px-1">
                        2
                    </span>
                </button>
            </div>

            <div class="flex md:hidden gap-2 mt-3">
                <div
                    class=" relative  border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700 cursor-pointer">
                    <button @click="toggleDropdown('For Sale')"
                        class="hover:text-sky-700 flex items-center gap-1 cursor-pointer">For Sale
                        <svg v-if="activeDropdown === 'For Sale'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'For Sale'"
                        class="absolute top-11 left-0 transition w-full z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p> For Sale 1</p>
                        <p> For Sale 2</p>
                        <p> For Sale 3</p>
                    </div>
                </div>

                <div
                    class=" relative border border-gray-400 rounded-md px-4 py-2 text-sm hover:bg-sky-700/5 hover:border-sky-700 cursor-pointer">
                    <button @click="toggleDropdown('Price')"
                        class="hover:text-sky-700 flex items-center gap-1 cursor-pointer">Price
                        <svg v-if="activeDropdown === 'Price'" class="ml-5" id='Arrow_Button_Up_2_24' width='10'
                            height='10' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg'
                            xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12, -11.98)"
                                    d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                        <svg v-else id='Arrow_Button_Down_2_24' class="ml-5" width='10' height='10' viewBox='0 0 24 24'
                            xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
                            <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
                            <g transform="matrix(0.85 0 0 0.85 12 12)">
                                <path
                                    style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                    transform=" translate(-12.01, -12.02)"
                                    d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                                    stroke-linecap="round" />
                            </g>
                        </svg>
                    </button>
                    <div v-show="activeDropdown === 'Price'"
                        class="absolute top-11 left-0 transition z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
                        <p> Price 1</p>
                        <p> Price 2</p>
                        <p> Price 3</p>
                    </div>
                </div>
                <button class="ml-auto bg-sky-700 text-white px-4 py-2 rounded-full text-sm">
                    Save Search
                </button>
            </div>

        </div>
    </div>
</template>

<script setup>


import { ref } from 'vue'

const activeDropdown = ref(null)

const toggleDropdown = (name) => {
    activeDropdown.value =
        activeDropdown.value === name ? null : name
}
</script>
