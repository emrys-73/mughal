<script>
    import Button from "$lib/components/ui/button/button.svelte";

    const featuredPlates = [
        {
            name: 'Chicken Tikka Masala',
            href: '/menu',
            image: '/food/tikka.webp',
        },
        {
            name: 'Chicken Biryani',
            href: '/menu',
            image: '/food/reis.webp',
        },
        {
            name: 'Grillpfanne',
            href: '/menu',
            image: '/food/grill.webp',
        },
    ]
</script>

<div class="w-full h-full min-h-screen bg-[#0f0b09] flex flex-col">
    <!-- Hero section -->
    <div class="w-full h-full min-h-[90vh] bg-[url('/hero.jpg')] bg-cover">
        <div class="bg-gradient-to-t from-[#0f0b09] to-transparent w-full h-[90vh] z-20 absolute top-0 flex"/>

        <div class="w-full h-full justify-end items-center text-white min-h-[90vh] flex flex-col z-40 pb-40">
            <h1 class="text-white opacity-100 flex z-20 text-3xl md:text-5xl lg:text-7xl font-ny-medium py-2">
                Mughal Hotel Restaurant
            </h1>
            <p class="text-white z-20 tracking-wider font-extralight text-sm md:text-md">
                Indische Spezialitäten
            </p>
        </div>
    </div>    

    <!-- Featured Plates -->
    <div id="menu" class="w-full h-full min-h-screen flex flex-col justify-center items-center gap-12">
        <div class="">
            <h2 class="font-ny-medium text-white text-2xl md:text-4xl">Beliebte Gerichte</h2>
        </div>

        <div class="md:w-3/4 w-full h-full justify-around items-center md:flex-row flex-col flex gap-6 md:gap-0">
            {#each featuredPlates as plate}
                <div class="md:w-1/3 w-5/6 px-4 md:px-0 md:hover:w-2/3 md:mx-4 hover:w-full flex rounded-2xl overflow-hidden h-[60vh] transition-all duration-500 ease-in-out relative">
                    <img src={plate.image} alt={plate.name} class="w-full object-cover rounded-2xl"/>

                    <div class="w-full h-1/2 bg-gradient-to-b from-transparent to-black/70 absolute bottom-0 flex flex-col px-4 justify-end py-4">
                        <p class="text-white text-2xl w-full text-center">{plate.name}</p>
                    </div>
                </div>                
            {/each}
        </div>

        <div class="w-full justify-center items-center flex md:flex-row flex-col gap-4 md:gap-0 min-h-[25vh]">
            <Button href="/MughalMenu.pdf" class="bg-[#800707] text-white px-12 py-1 text-lg rounded-full hover:bg-[#120E0B]  transition-all duration-500 ease-in-out font-light">
                Speisekarte ansehen
            </Button>
        </div>
    </div>

    <!-- Break -->
    <div id="gallerie" class="w-full h-[70vh] flex flex-col relative">
        <img src="/in.webp" alt="face" class="w-full object-cover h-[70vh]">
        <div class="bg-gradient-to-t from-[#0f0b09] to-transparent absolute h-[70vh] w-full top-0 flex justify-center items-end">
            <h2 class="text-white opacity-100 z-20 text-4xl hover:text-5xl transition-all duration-500 ease-in-out font-ny-medium py-20 w-full px-12 hidden">
                <a href="https://www.google.com/maps/place/Hotel+Restaurant+Mughal+-+Indian+Specialties/@48.4935596,12.0377078,17z/data=!3m1!4b1!4m9!3m8!1s0x479e25569f7cc23f:0x28864ec669194d7e!5m2!4m1!1i2!8m2!3d48.4935596!4d12.0402827!16s%2Fg%2F11vq9mw_dl?entry=ttu" class="underline">
                    Hofmark 1, 84174 Eching
                </a>
            </h2>
        </div>
        
    </div>

    <!-- Gallery -->
    <div class="w-full min-h-[100vh] flex flex-col py-20 justify-center items-center gap-16">
        <div class="">
            <h2 class="font-ny-medium text-white text-4xl">Galerie</h2>
        </div>
        <!-- General container -->
        <div class="w-full h-full flex flex-col justify-center items-center gap-4 md:gap-12">

            <div class="md:w-5/6 w-full px-4 md:px-0 flex flex-row md:gap-8 gap-4 h-full justify-center items-center">
                <div class="w-1/2 h-[50vh] hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/bokeh.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-1/2 h-[50vh] hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/reiszoom.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
            </div>

            <div class="md:w-5/6 w-full px-4 md:px-0 flex flex-col md:flex-row md:gap-8 gap-4 h-full justify-center items-center">
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/naan.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/beer.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/lasi.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
            </div>

            <div class="md:w-5/6 w-full px-4 md:px-0 flex flex-row md:gap-8 gap-4 h-full justify-center items-center">
                <div class="w-1/2 h-[50vh] hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/bar.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-1/2 h-[50vh] hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/bird.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
            </div>

            <div class="md:w-5/6 w-full px-4 md:px-0 flex flex-col md:flex-row md:gap-8 gap-4 h-full justify-center items-center">
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/tikkaclose.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/me.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
                <div class="w-full md:w-1/3 md:h-[60vh] h-[25vh] hover:h-[35vh] md:hover:h-[60vh] md:hover:w-2/3 overflow-hidden rounded-2xl flex transition-all duration-500 ease-in-out">
                    <img src="/food/grillchicken.jpg" alt="pic" class="w-full h-full object-cover">
                </div>
            </div>

        </div>
    </div>

    <!-- Contact -->
    <div id="contact" class="w-full min-h-[100vh] flex flex-col md:px-12 justify-center items-center gap-8">

        <div class="w-full h-full text-center flex-row hidden">
            <h2 class="text-white z-20 text-4xl transition-all duration-500 ease-in-out font-ny-medium w-full px-12 flex justify-start">
                Hofmark 1, 84174 Eching
            </h2>
            <h2 class="text-white opacity-100 z-20 text-4xl hover:text-5xl transition-all duration-500 ease-in-out font-ny-medium w-full px-12 flex justify-end">
                <a href="https://www.google.com/maps/place/Hotel+Restaurant+Mughal+-+Indian+Specialties/@48.4935596,12.0377078,17z/data=!3m1!4b1!4m9!3m8!1s0x479e25569f7cc23f:0x28864ec669194d7e!5m2!4m1!1i2!8m2!3d48.4935596!4d12.0402827!16s%2Fg%2F11vq9mw_dl?entry=ttu" class="underline">
                    Hofmark 1, 84174 Eching
                </a>
            </h2>
        </div>
        
        <div class="flex w-full h-full md:flex-row flex-col gap-6">
            <div class="w-full h-full justify-end items-center flex flex-col">
                    <div class="text-white font-light md:h-[70vh] text-right py-6 text-md md:text-xl justify-between flex flex-col">
                        <div class="flex flex-col gap-8">
                            <div>
                                <h2 class="text-white opacity-90 hover:opacity-100 z-20 text-2xl md:text-4xl transition-all duration-500 ease-in-out font-ny-medium w-full flex justify-end">
                                    <a href="https://www.google.com/maps/place/Hotel+Restaurant+Mughal+-+Indian+Specialties/@48.4935596,12.0377078,17z/data=!3m1!4b1!4m9!3m8!1s0x479e25569f7cc23f:0x28864ec669194d7e!5m2!4m1!1i2!8m2!3d48.4935596!4d12.0402827!16s%2Fg%2F11vq9mw_dl?entry=ttu" class="underline">
                                        Hofmark 1, 84174 Eching
                                    </a>
                                </h2>
                            </div>
                            <div>
                                <b>Montag bis Freitag</b>
                                <br>
                                11:00 - 15:00 und 17:00 - 23:00 Uhr
                                <br>
                                <b>Samstag, Sonntag und Feiertage</b>
                                <br>
                                12:00 - 23:00 Uhr
                            </div>
                        </div>
    
                        <div class="py-4 md:py-0 flex flex-col gap-4 justify-center items-center">
                            <Button href="tel:(+49)087095698648" class="bg-[#800707] text-white px-12 py-1 text-lg rounded-full hover:bg-[#120E0B]  transition-all duration-500 ease-in-out font-light">
                                Direkt anrufen
                            </Button>
                            <a href="https://www.lieferando.de/speisekarte/restaurant-mughal?&adj_tracker=tn818ro&adj_campaign=17679818623&k1111=k1111&campaignname=CM_S_G_DEU_DE_%5BRES%5D_%5BENGM%5D_OD_Eching_9048295" class="text-white text-sm transition-all duration-300 ease-in-out hover:opacity-100 opacity-80">
                                <span class="">
                                    oder bei Lieferando bestellen
                                </span>
                            </a>
                        </div>
                    </div>
            </div>
            <div class="w-full h-full rounded-2xl justify-center items-center flex px-4 md:px-0">
                <iframe title="Maps" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2644.0694844465643!2d12.037707777274536!3d48.49355957128507!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x479e25569f7cc23f%3A0x28864ec669194d7e!2sHotel%20Restaurant%20Mughal%20-%20Indian%20Specialties!5e0!3m2!1sen!2sde!4v1721199782735!5m2!1sen!2sde" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"
                    class="md:w-[60vw] w-full md:h-[70vh] h-[55vh] rounded-2xl"
                ></iframe>
            </div>
        </div>
    </div>

    <!-- 087095689648 -->
    <!-- Hotel reservation -->
    <div class="w-full h-[80vh] flex flex-row justify-center items-center relative">
        <img src="/face.webp" alt="face" class="w-full h-full object-cover opacity-100">
        <div class="w-full h-full bg-gradient-to-b from-black/30 to-black/100 absolute top-0 z-20 justify-center items-center py-32 flex flex-col gap-4">
            <h2 class="text-white font-ny-medium text-2xl md:text-4xl">
                Auf der Suche nach einer Unterkunft?
            </h2>
            <span class="text-white hidden">
                Inklusive Frühstück
            </span>

            <Button href="https://direct-book.com/properties/mughalhotel-restaurant?locale=de&items%5B0%5D%5Badults%5D=2&items%5B0%5D%5Bchildren%5D=0&items%5B0%5D%5Binfants%5D=0&currency=EUR&checkInDate=2024-07-17&checkOutDate=2024-07-18&trackPage=no&selected=0" class="bg-[#800707] text-white px-12 py-1 text-lg rounded-full hover:bg-[#120E0B]  transition-all duration-500 ease-in-out font-light">
                Jetzt buchen
            </Button>
            <div class="flex flex-row gap-6 justify-center items-center py-2">
                <a href="https://www.instagram.com/mughal.hotelrestaurant/" class="w-8 h-8 hover:w-10 hover:h-10 flex transition-all duration-300 ease-in-out " >
                    <img src="/ig_white.webp" alt="ig" >
                </a>
                <a href="https://www.facebook.com/people/Hotel-Restaurant-Mughal/61569387713603/" class="w-8 h-8 hover:w-10 hover:h-10 flex transition-all duration-300 ease-in-out " >
                    <img src="/fb_white.webp" alt="fb">
                </a>
            </div>
        </div>
    </div>
</div>