<template>
    <section id="achievements" class="text-white select-none relative z-10 pt-20">
        <h2 class="text-4xl font-bold mb-4 px-4 xl:pl-16">My <span class="text-transparent bg-clip-text bg-gradient-to-r from-[var(--color-primary)] to-[var(--color-secondary)]">Achievements</span></h2>
        <div class="grid grid-cols-1 md:grid-cols-2 sm:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4 gap-8 items-center py-8 px-4 xl:gap-8 sm:py-16 xl:px-16 relative z-10">
            <div v-for="card in cards" data-aos="flip-down">
                <div class="w-full h-75 px-4 py-4 bg-[#111a3e]/80 hover:bg-[#152049] hover:scale-108 transition-all cursor-pointer rounded-2xl flex flex-col items-center justify-center text-center">
                    <div class="h-20 flex justify-center items-center text-[4rem]">
                        <p v-if="card.id==1">🏅</p>
                        <p v-else-if="card.id==2">🥇</p>
                        <p v-else-if="card.id==3 || card.id==4">🥈</p>
                        <p v-else-if="card.id==5"><img src="https://upload.wikimedia.org/wikipedia/commons/1/19/LeetCode_logo_black.png" class="h-[4.5rem]" alt=""></p>
                        <p v-else-if="card.id==6"><img src="https://upload.wikimedia.org/wikipedia/commons/4/43/GeeksforGeeks.svg" class="h-[3rem]" alt=""></p>
                    </div>
                    <p class=" text-transparent bg-clip-text bg-gradient-to-br from-[var(--color-primary)] to-[var(--color-secondary)] text-[1.6rem] font-bold" >{{ card.rank }}</p>
                    <p class="text-[1.15rem] font-semibold">{{ card.event }}</p>
                    <p class="text-[1rem] opacity-80">{{ card.location }}</p>
                    <p>{{ card.link }}</p>
                </div>
            </div>
        </div>  
    </section>
</template>
<script>
    export default{
        data(){
            return{
                cards:[
                    {   
                        id:1,
                        rank:'General Merit Rank: 6',
                        event:'WBJECA, 2024',
                        location:'West Bengal Joint Entrance Examination Board',
                        link:null,
                    },
                    {   
                        id:2,
                        rank:'Winner',
                        event:"Sherlocked, Srijan 2025",
                        location:'Faculty of Engineering and Technology, Jadavpur University',
                        team:{
                            'Bijit Mondal':'link',
                            'Rohan Chakraborty':'link'
                        },
                        link:null,
                    },
                    {
                        id:3,
                        rank:'First Runner-Up',
                        event:'Error 404, Envision 2025',
                        location:'Ramakrishna Mission Residential College (Autonomous)',
                        link:null,
                    },
                    {
                        id:4,
                        rank:'First Runner-Up',
                        event:'The Turing Show, Perceptron 2025',
                        location:'Ramakrishna Mission Vivekananda Educational and Research Institute',
                        link:null,
                    },
                    {
                        id:5,
                        rank:'400+ Problem Solved',
                        event:'LeetCode',
                        location:'Contest Rating: 1600 in 16 contests and POTD Streak: 300+ days',
                        link:null,
                    },
                    {
                        id:6,
                        rank:'300+ Problem Solved',
                        event:'GeeksForGeeks',
                        location:'Contest Rating: 1420 in 5 contests and POTD Streak: 130+ days',
                        link:null,
                    },
                    
                ]
            }
        },
        methods:{
            
        },
    }
</script>
<style scoped>
    
</style>