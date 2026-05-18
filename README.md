# Async Tutorial - Modul 10

## Experiment 1.1: Original timer from the book

Program berhasil dijalankan. Output menunjukkan "howdy!" diikuti jeda 2 detik,
kemudian "done!". Ini membuktikan TimerFuture bekerja secara asynchronous,
thread spawner menunggu 2 detik di background, sementara executor bisa
melakukan hal lain (jika ada task lain).
