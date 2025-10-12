<script lang="ts">
    import Titled from "../lib/assets/real123.png";
    import Real from "../lib/assets/cover.jpeg";
    let title = "Real12 Magazine";
</script>

<main style="background-image: url({Titled});">
  <button class="w-48 h-16 rounded-2xl btn mt-60% hover:scale-105 transition-transform duration-200">here!</button>
    <div class="bg-transparent z-1000">
         
  </div>
</main>



<style>
main {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100vh;           
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    padding-top: 50vh; /* tombol muncul sekitar tengah layar */
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
        width: 40vw;              /* tombol menyesuaikan layar */
        font-size: 0.9rem;
        padding: 10px 20px;
    }

    .pic {
      width: 60vw;
      height: 80vw;
    }
}
</style>
