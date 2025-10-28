// =======================================================
// script.js
// Logika Sederhana untuk Website Portofolio Rifki
// =======================================================

document.addEventListener('DOMContentLoaded', () => {
    // 1. Logika Smooth Scrolling
    // Membuat guliran antar section lebih halus di browser yang tidak mendukung CSS smooth-scroll

    const navLinks = document.querySelectorAll('nav ul li a');

    navLinks.forEach(link => {
        link.addEventListener('click', function(e) {
            // Hentikan perilaku default (melompat tiba-tiba)
            e.preventDefault(); 
            
            // Ambil ID tujuan dari atribut href (e.g., '#about', '#projects')
            const targetId = this.getAttribute('href'); 
            
            // Cari elemen dengan ID tersebut
            const targetSection = document.querySelector(targetId);

            if (targetSection) {
                // Gunakan API 'scrollIntoView' untuk animasi gulir yang mulus
                targetSection.scrollIntoView({
                    behavior: 'smooth' // Ini yang membuat guliran halus
                });
            }
        });
    });

    // 2. Fungsi Contoh (Siap untuk Pengembangan Lanjutan)
    // Di masa depan, kamu bisa menambahkan fitur lain di sini, 
    // misalnya: toggle dark mode, filter proyek, atau animasi saat scroll.
    
    console.log("Website Portofolio Rifki Hadi Saputra siap dimuat!");
    
});
