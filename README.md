# Tutorial 4 - Game Development

Nama: Fikri Risyad Indratno<br>
NPM: 2206031170

## Latihan Mandiri: Membuat Level Baru Dengan Tile Map & Obstacle Berbeda

Saya memulai dengan membuat *scene* baru bernama `Level2.tscn`, lalu memasukkan `Player.tscn` sebagai *child*, serta membuat `TileMapLayer` baru. Kemudian, pada `TileMapLayer` tersebut, saya membuat `TileSet` baru dengan ukuran 128x128 pixel dan menambahkan elemen baru pada *Physics Layers*. Saya menggunakan `assets/kenney_platformerpack/Spritesheets/spritesheet_gr_sand.png` sebagai `TileSet` dan menggambar bentuk kolisi untuk setiap tipe *tile*. Setelah itu, saya mulai membuat level dengan memasukkan tile ke dalam *scene*.

Selanjutnya, saya membuat *area* menang seperti pada `Level1.tscn`, yaitu dengan menggunakan `Sprite2D` dan memasukkan roket rektorat. Lalu, saya menambahkan *scene* `AreaTrigger.tscn` yang sudah di buat pada tutorial sebagai *child* dari `Sprite2D` ini, serta memastikan signal `body_entered` terhubung dengan method `_on_body_entered` pada *script*. `AreaTrigger.tscn` saya gunakan kembali untuk membuat *area* kalah, yaitu jurang, dan memastikan signal juga terhubung dengan benar.

Kemudian, saya membuat *scene* baru bernama `FallingSlime.tscn` yang merupakan `RigidBody2D` dan menambahkan `Sprite2D` dengan *texture* `assets/kenney_platformerpack/PNG/Enemies/slimeBlock.png` sebagai *child*, serta sebuah `CollisionShape2D` dengan ukuran yang sesuai dengan `Sprite2D` sebelumnya sebagai *child*. *Scene* ini juga diberikan *script* yang serupa dengan *script* `FallingFish.gd`. Terakhir, saya membuat `Node2D` sebagai *child* dari `Level2.tscn` sebagai spawner dan meletakkannya di tengah-tengah level. *Spawner* diberikan *script* yang serupa dengan *spawner* pada `Level1.tscn`.