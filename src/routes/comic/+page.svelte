<script lang="ts">
  import rid from "../../lib/assets/komik.jpg"
</script>

<main style="background-image: url({rid}); background-color: #0B1108;">

    <!-- tambahin konten biar bisa discroll -->
    <div style="height: 250vh;"></div>

</main>

<style>

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  min-height: 100vh;
  background-image: url("{rid}");
  background-size: cover;
  background-position: center top;
  background-repeat: no-repeat;
  background-attachment: scroll; /* ini kuncinya — background ikut scroll */
  background-color: #ebe3c6; /* nutup area bawah */
}

.content {
  width: 100%;
  position: relative;
  z-index: 1;
  padding: 4rem 2rem;
  text-align: center;
}

@media (max-width: 768px) {
    main {
        
        min-height: 90vh;          
        padding-top: 40vh;       
        background-position: top;
        background-size: contain; 
        background-repeat: no-repeat;
    }

    .btn {
        width: 40vw;              
        font-size: 0.9rem;
        padding: 10px 20px;
    }
}

@media (max-width: 658px) {
    main {
        min-height: 60vh;          /* ganti height -> min-height */
        padding-top: 40vh;         
        background-position: top;  
        background-size: contain; 
        background-repeat: no-repeat;
    }
}

</style>
