<template>
    <div class="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-xl cursor-pointer duration-100 ease-in">

        <div class="relative">
            <img src="/src/assets/images/card/card-img.png" class="w-full h-48 object-cover" />

            <span class="absolute top-2 left-2 bg-white text-xs px-2 py-1 rounded-full shadow">
                6 days on Houzeo
            </span>

            <button class="absolute top-2 right-2 p-1 rounded-full shadow cursor-pointer">
                <svg xmlns="www.w3.org" width="24" height="24" viewBox="0 0 24 24" fill="#00000080" stroke="white"
                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path
                        d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z">
                    </path>
                </svg>

            </button>
            <button class="absolute hover:animate-ping top-2 right-2 p-1 rounded-full shadow cursor-pointer">
                <svg xmlns="www.w3.org" width="24" height="24" viewBox="0 0 24 24" fill="#00000080" stroke="white"
                    stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path
                        d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z">
                    </path>
                </svg>

            </button>
        </div>


        <div class="p-4">
            <div class="flex justify-between gap-1">
                <div
                    class="flex items-center gap-2 text-sm text-gray-600 border border-gray-300 inline-flex px-2 rounded-full">
                    <span class="w-3 h-3 bg-green-500 rounded-full "></span>
                    <span class="font-semibold">House For Sale</span>
                </div>
                <div class="flex gap-1 items-center">
                    <svg id='Eye_20' width='20' height='20' viewBox='0 0 20 20' xmlns='http://www.w3.org/2000/svg'
                        xmlns:xlink='http://www.w3.org/1999/xlink'>
                        <rect width='20' height='20' stroke='none' fill='#000000' opacity='0' />


                        <g transform="matrix(0.73 0 0 0.73 10 10)">
                            <path
                                style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                                transform=" translate(-12, -12)"
                                d="M 12 4 C 4 4 1 12 1 12 C 1 12 4 20 12 20 C 20 20 23 12 23 12 C 23 12 20 4 12 4 z M 12 6 C 17.276 6 19.944594 10.267094 20.808594 11.996094 C 19.943594 13.713094 17.255 18 12 18 C 6.724 18 4.0554062 13.732906 3.1914062 12.003906 C 4.0574062 10.286906 6.745 6 12 6 z M 12 8 C 9.791 8 8 9.791 8 12 C 8 14.209 9.791 16 12 16 C 14.209 16 16 14.209 16 12 C 16 9.791 14.209 8 12 8 z M 12 10 C 13.105 10 14 10.895 14 12 C 14 13.105 13.105 14 12 14 C 10.895 14 10 13.105 10 12 C 10 10.895 10.895 10 12 10 z"
                                stroke-linecap="round" />
                        </g>
                    </svg>
                    <span>2.3K</span>
                </div>
            </div>

           <div class="flex justify-between items-center gap-1 mt-2 flex-wrap">
             <p class=" text-xl font-semibold text-sky-700">
                $3,349,000
            </p>

            <div class="flex gap-2 text-sm text-gray-600 ">
                <span><span class="text-sky-700 text-lg font-semibold">4</span> Beds</span>
                <span><span class="text-sky-700 text-lg font-semibold">3</span> Baths</span>
                <span><span class="text-sky-700 text-lg font-semibold">998</span> sqft</span>
            </div>
           </div>

            <p class="text-sm text-gray-500 mt-2 text-zinc-600">
                <span class="font-semibold text-black">2856 Meadow Park Ave</span>, Henderson, NV 89052
            </p>

            <p class="text-xs text-gray-400 mt-1">
                MLS® distributed by MLS GRID
            </p>
        </div>
    </div>
</template>
