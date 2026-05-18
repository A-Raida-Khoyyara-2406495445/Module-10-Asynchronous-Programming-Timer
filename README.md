# Async Tutorial - Modul 10

## Experiment 1.1: Original timer from the book

Program berhasil dijalankan. Output menunjukkan "howdy!" diikuti jeda 2 detik,
kemudian "done!". Ini membuktikan TimerFuture bekerja secara asynchronous,
thread spawner menunggu 2 detik di background, sementara executor bisa
melakukan hal lain (jika ada task lain).



## Experiment 1.2: Understanding How It Works
### Screenshot

![Experiment 1.2 Result](assets/images/experiment12.jpg)


### Urutan Output:
```zsh
Raida's Computer: hey! hey!
Raida's Computer: howdy!
Raida's Computer: done!
```

### Penjelasan:
`"hey hey!"` muncul sebelum `"howdy!"` meskipun ditulis setelah `spawn`
Ini karena `spawn` hanya mendaftarkan task ke queue, tidak langsung menjalankannya
Task baru dieksekusi ketika `executor.run()` dipanggil
`println!("hey hey!")` adalah kode synchronous yang langsung dijalankan