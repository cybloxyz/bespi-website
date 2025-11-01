<script lang="ts">
    import { goto } from '$app/navigation';

    function Riddle() {
      goto('/riddle');
    }
    function Games() {
      goto('/games');
    }
    function Create() {
      goto('/create');
    }
    function Our() {
      goto('/extra');
    }
    function Comic() {
      goto('/comic');
    }
    import Titled from "../lib/assets/real123.webp";
	
</script>

<main style="background-image: url({Titled}); background-color: #ebe3c6;">
  <div class="bg-red-900 h-text w-text mt-56 py-2 px-2 mx-4 lg:py-8 md:py-8 sm:py-8 lg:px-24 md:px-24 sm:px-14 rounded-full">
    <h1 class="lg:text-3xl md:text-2xl sm:text-lg text-xs font-bold text-center text-white drop-shadow-2xl">ANSWER FOR REAL 12 BRAIN CHALLENGES!</h1>
  </div>
  <div class="flex gap-4 items-center flex-wrap justify-center mt-8">
    <button class="w-48 h-16 rounded-2xl btn hover:scale-105 transition-transform duration-200" onclick={Riddle}>Riddle</button>
    <button class="w-48 h-16 rounded-2xl btn hover:scale-105 transition-transform duration-200" onclick={Games}>Games</button>
   
    <button class="w-48 h-16 rounded-2xl btn hover:scale-105 transition-transform duration-200" onclick={Comic}>Comic!</button>
  </div>
  <h1 class="text-center mt-6 lg:text-xl md:text-lg sm:text-sm text-xs">click each button to check your answer!</h1>
  <button class="mt-8 w-96 h-16 rounded-2xl btn hover:scale-105 transition-transform duration-200">extra part!</button>
</main>

<style>
main {
    display: flex;
    justify-content: center; /* vertikal */
    align-items: center;     /* horizontal */
    flex-direction: column;
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-color: #ebe3c6; /* menutupi sisa area */
    padding-top: 0; /* hapus padding besar */
}


main::after {
    content: "";
    display: block;
    width: 100%;
    height: 100vh; /* atau height lebih besar sesuai kebutuhan */
    background-color: #ebe3c6;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1; /* biar di belakang konten */
}


/* tombol */
.btn {
    padding: 12px 24px;
    font-size: 1rem;
    font-weight: bold;
    color: white;
    background-color: #942323;
    border: none;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.3);
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

.btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 14px 20px rgba(0, 0, 0, 0.35);
}


@keyframes wiggle {
  0% { transform: rotate(0deg); }
  25% { transform: rotate(5deg); }
  50% { transform: rotate(-5deg); }
  75% { transform: rotate(5deg); }
  100% { transform: rotate(0deg); }
}

.wiggle:hover {
  animation: wiggle 0.5s ease-in-out infinite;
}


/* ----------------- RESPONSIVE UNTUK HP ----------------- */
@media (max-width: 768px) {
    main {
        height: 70vh;            /* lebih pendek di HP */
        padding-top: 40vh;       /* tombol muncul lebih pas */
        background-position: top; /* fokus gambar di atas */
    }

    .btn {
        width: 40vw;              /* tombol menyesuaikan layar */
        font-size: 0.9rem;
        padding: 10px 20px;
    }
}

@media (max-width: 658px) {
    main {
        height: 40vh;            /* lebih pendek di HP */
        padding-top: 40vh;       /* tombol muncul lebih pas */
        background-position: top; /* fokus gambar di atas */
    }

    .btn {
        width: 50vw;              /* tombol menyesuaikan layar */
        font-size: 0.9rem;
        padding: 10px 20px;
    }

    .pic {
      width: 60vw;
      height: 80vw;
    }
}
</style>
