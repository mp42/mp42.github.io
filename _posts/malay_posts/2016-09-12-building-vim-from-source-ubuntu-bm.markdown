---
layout: post
title:  "Membina Vim 8 Daripada Kod Sumber Untuk Ubuntu 16.04"
date:   2016-09-12 22:16:57 -0700
categories: general vim bm
draft: true
---

Baru-baru ini, [Vim 8](https://groups.google.com/forum/#!topic/vim_announce/EKTuhjF3ET0) telah diumumkan. Oleh itu, saya akan ambil peluang ini untuk mengkaji semula bagaimana untuk membina Vim daripada kod sumber! (_Nota: tulisan ini adalah untuk peringatan saya diri sendiri_).

[Panduan ini oleh Valloric](https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source) agak menyeluruh walaupun panduan tersebut berdasarkan versi Vim yang lebih lama. Antara langkah-langkah yang saya telah gunakan (langkah-langkah ini juga mengandungi maklumat daripada panduan Valloric):

1. Memadam versi Vim yang sedia ada (_langkah #2 dalam panduan Valloric_)
2. Memastikan bahawa semua "pre-requisite libraries" (_langkah #1 dalam panduan Valloric_) telah dimuat turun dan "installed".
	* langkah ini amat penting jika kita ingin membina Vim yang menyokong "language" tertentu e.g Python 3, Lua etc.
	  

3. Memuat turun kod sumber dan membinanya
	* Biasanya, saya menggunakan `sudo checkinstall` (`checkinstall` akan mewujudkan satu `.deb` fail yang membolehkan "package manager" kita memadam Vim).
	* Saya telah mengalami masalah membina Vim 8 daripada kod sumber yang menyokong Python 2.5 dan Python 3. Selepas kaji selidik, saya sedar bahawa kita hanya boleh membina Vim dengan sokongan untuk salah satu versi Python sahaja.
4. Tetapkan Vim baru sebagai editor text tetapan asal.
5. Memadam fail kod sumber yang dimuat turun
	* Langkah ini tidak semestinya diikut. Saya sendiri lebih suka tidak menyimpan benda yang tidak diperlukan. Jikalau `sudo checkinstall` digunakan, fail `.deb` yang dihasilkan oleh langkah tersebut akan berada di dalam direktori kod sumber. Jangan lupa memindahkan fail tersebut sekiranya anda ingin menyimpannya. 
