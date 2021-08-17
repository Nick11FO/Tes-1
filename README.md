# Take Home Test

Kasus sehari-hari: 

Ada sekelompok anak yang sedang bermain puzzle. Mereka harus cepat-cepatan menempatkan puzzle binatang sesuai dengan huruf depan binatang tersebut. Contohnya adalah Tupai, berarti mencari bagian T pada puzzle tersebut. Yang paling cepat dapat menempatkan puzzle tersebut ke bagiannya dengan benar, dialah yang menang.

Algoritma:

Approach pertama [linear search O(n)] -> </br>
Cari dari awal puzzle. A->B->C->D sampai S->T. (Anggap setiap proses pencarian tiap bagian diselesaikan dengan waktu 1 detik. Bagian A memakan 1 detik). Berarti butuh 20 detik untuk algoritma ini untuk menemukan bagian T dalam puzzle tersebut. A->B->C->D->E->F->G->H->I->J->K->L->M->N->O->P->Q->R->S->T. Setelah menemukan bagian T pada puzzle, tempatkan Tupai pada bagian T puzzle tersebut. 

Approach ketiga [binear search O(log n)] -> </br>
Langsung mencari ke tengah-tengah alphabet yaitu M (dari 26 huruf alphabet dibagi 2 = 13). Lalu mencari tahu apakah T sesudah atau sebelum huruf M. Karena T adalah sesudah M maka dicari lagi bagian tengah dari huruf alphabet ke 13(M) dan 26(Z), yaitu T (26-13 = 13/2 = 6,5; Genapkan jadi 7. 13+7=20. Huruf ke 20). Lalu ketemulah huruf T. Anggap jika setiap proses pencarian diperlukan 1 detik, maka hanya diperlukan 2 detik. M->T. Setelah menemukan bagian T pada puzzle, tempatkan Tupai pada bagian T puzzle tersebut.

Pseudocode:

Approach pertama [linear search O(n)] -> 

1&nbsp;&nbsp;&nbsp;  Pick up puzzle </br>
2&nbsp;&nbsp;&nbsp;  Open first puzzle piece </br>
3&nbsp;&nbsp;&nbsp;  Look at puzzle piece </br>
4&nbsp;&nbsp;&nbsp;  If T is on the puzzle piece </br> 
5&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Put the animal </br> 
6&nbsp;&nbsp;&nbsp;  Else if T is not on the puzzle piece </br>
7&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Open next puzzle piece </br>
8&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Go back to line 4 </br>
9&nbsp;&nbsp;&nbsp;  Else </br>
10&nbsp;             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Quit

Approach ketiga [binear search O(log n)] ->

1&nbsp;&nbsp;&nbsp;  Pick up puzzle </br>
2&nbsp;&nbsp;&nbsp;  Open to the middle of puzzle piece </br>
3&nbsp;&nbsp;&nbsp;  Look at puzzle piece </br>
4&nbsp;&nbsp;&nbsp;  If T is on the puzzle piece </br>
5&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Put the animal </br>
6&nbsp;&nbsp;&nbsp;  Else if T is earlier in puzzle piece  </br>
7&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Open to middle left half of puzzle piece </br>
8&nbsp;&nbsp;&nbsp;  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Go back to line 3 </br>
9&nbsp;&nbsp;&nbsp;  Else if T is later in puzzle piece  </br>
10&nbsp;             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Open to the middle of right half puzzle piece </br>
11&nbsp;             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Go back to line 3 </br>
12&nbsp;             Else </br>
13&nbsp;             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Quit </br>

Kesimpulan:

Linear search adalah metode pencarian yang lebih sederhana dengan hanya mengurutkan satu per satu dari awal hinga akhir daripada binear search namun jauh lebih lama. Sedangkan Binear search adalah metode pencarian yang lebih kompleks daripada linear search namun jauh lebih cepat. 
