# Muhammad-Riski-Fadillah
def jawab_pertanyaan(pertanyaan: str) -> str:
    # Mengubah input menjadi huruf kecil agar pencarian kata kunci lebih akurat
    t = pertanyaan.lower()
    
    # Respon awal jika input kosong atau sapaan umum
    if t == "" or t == "halo" or t == "hi":
        return (
            "Halo calon pengusaha sukses! Saya adalah asisten AI mentor bisnis Anda.\n"
            "Pertanyaan yang bisa kamu coba:\n"
            "- Strategi bisnis awal\n"
            "- Cara mencari modal\n"
            "- Mentalitas pengusaha\n"
            "- Manajemen waktu\n"
            "- Tips menghadapi kegagalan"
        )

    # Logika berdasarkan kata kunci Strategi Bisnis
    if "strategi" in t or "bisnis" in t:
        return (
            "Strategi bisnis terbaik dimulai dengan riset pasar yang mendalam. "
            "Fokuslah pada penyelesaian masalah (problem solving) pelanggan Anda. "
            "Mulailah dari skala kecil atau MVP (Minimum Viable Product), "
            "kumpulkan masukan, lalu kembangkan secara bertahap."
        )
    
    # Logika berdasarkan kata kunci Modal
    elif "modal" in t or "dana" in t:
        return (
            "Modal bukan hanya soal uang. Kamu bisa mulai dengan bootstrapping (dana pribadi), "
            "mencari partner strategis, atau melalui pendanaan investor jika model bisnis sudah terbukti. "
            "Yang terpenting adalah pengelolaan arus kas (cash flow) yang disiplin."
        )
    
    # Logika berdasarkan kata kunci Mentalitas
    elif "mental" in t or "gagal" in t:
        return (
            "Seorang pengusaha sukses melihat kegagalan sebagai batu loncatan. "
            "Jangan takut gagal, tapi takutlah jika tidak belajar dari kesalahan tersebut. "
            "Miliki resiliensi tinggi dan jangan pernah berhenti berinovasi."
        )
    
    # Logika berdasarkan kata kunci Waktu
    elif "waktu" in t or "produktivitas" in t:
        return (
            "Gunakan hukum Pareto (80/20). Fokuskan 80% energi Anda pada 20% aktivitas "
            "yang memberikan dampak paling besar bagi pertumbuhan bisnis Anda. "
            "Delegasikan tugas rutin agar Anda bisa fokus pada visi besar bisnis."
        )

    # Respon jika kata kunci tidak ditemukan
    else:
        return (
            "Maaf, saya belum memahami pertanyaan itu. "
            "Coba tanya tentang 'strategi', 'modal', 'mentalitas', atau 'manajemen waktu'."
        )

# Bagian untuk menjalankan Chatbot di Terminal/VS Code
if __name__ == "__main__":
    print("--- CHATBOT MENTOR PENGUSAHA SUKSES ---")
    print(jawab_pertanyaan("")) # Menampilkan instruksi awal
    
    while True:
        print("\n> ", end="")
        user_input = input()
        
        # Perintah untuk keluar dari program
        if user_input.lower() in ["exit", "keluar", "stop", "clear"]:
            print("Sampai jumpa di puncak kesuksesan!")
            break
            
        respon = jawab_pertanyaan(user_input)
        print(respon)


--- CHATBOT MENTOR PENGUSAHA SUKSES ---
Halo calon pengusaha sukses! Saya adalah asisten AI mentor bisnis Anda.
Pertanyaan yang bisa kamu coba:
- Strategi bisnis awal
- Cara mencari modal
- Mentalitas pengusaha
- Manajemen waktu
- Tips menghadapi kegagalan

> cara mencari modal
Modal bukan hanya soal uang. Kamu bisa mulai dengan bootstrapping (dana pribadi), mencari partner strategis, atau melalui pendanaan investor jika model bisnis sudah terbukti. Yang terpenting adalah pengelolaan arus kas (cash flow) yang disiplin.

> apa strategi bisnisnya?
Strategi bisnis terbaik dimulai dengan riset pasar yang mendalam. Fokuslah pada penyelesaian masalah (problem solving) pelanggan Anda. Mulailah dari skala kecil atau MVP (Minimum Viable Product), kumpulkan masukan, lalu kembangkan secara bertahap.

> mental pengusaha
Seorang pengusaha sukses melihat kegagalan sebagai batu loncatan. Jangan takut gagal, tapi takutlah jika tidak belajar dari kesalahan tersebut. Miliki resiliensi tinggi dan jangan pernah berhenti berinovasi.

> keluar
Sampai jumpa di puncak kesuksesan!
