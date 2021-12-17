---
title: Copy To Clipboard dengan Javascript
date: 2021-12-17T12:40:52.375Z
description: Copy To Clipboard dengan Javascript semudah membalik telapak tangan
  cukup satu fungsi
---
Halo guys, pernah ngga sih ngalamin kalo buat aplikasi ketika copy text harus ada dalam input (bisa textarea, text field dll) ? Ngeselin kan? Nah cara itu udah kuno banget, ada cara yang lebih gampang yaitu dengan melakukan manipulasi DOM (Document Object Model), singkatnya kita simpan text dari elemen yang ingin kita salin lalu membuat input field sementara untuk menaruh text tersebut sebelum melakukan eksekusi **document.execCommand()** karena secara default fungsi itu akan bekerja ketika ada input field yang terfokus. Oke langsung ke langkah pertama. Disini nantinya aku pakai jQuery sebagai trigger listener buat button, but it works fine with native too

###### Buat pembungkus fungsinya fulu

```js
function copyToClipboard(text) {
    var textarea = document.createElement('textarea'); // Membuat element bayangan
    textarea.textContent = text.trim(); // mengisi textarea dari text yang di trim
    document.body.appendChild(textarea); // tambahkan elemen bayangan ke body

    var selection = document.getSelection(); // melakukan seleksi
    var range = document.createRange(); // ambil jarak
    range.selectNode(textarea); // Tentukan elemen mana yang mau diselect
    selection.removeAllRanges(); // Hapus semua jarak
    selection.addRange(range); // Masukkan elemen yang terselect tadi
    document.execCommand('copy') // Nah trigger copy
    selection.removeAllRanges(); // Bersihkan seleksi

    document.body.removeChild(textarea); // Hapus elemen bayangan tadi
    alert("Success")
}
```

Setelah membuat fungsi diatas, langkah selanjutnya adalah melakukan trigger untuk call fungsi tersebut. Simpel sih kalau di jquery aku pake fungsi dibawah ini
```js
$(document).on('click','.to-clipboard', function () {
    copyToClipboard($(this).html().trim());
});
```

Taddaaa.... Simpel kan? Gitu aja ya blog kali ini, mengatasi gabut