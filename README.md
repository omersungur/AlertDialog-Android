Activity Context -> Aktiviteyi ilgilendiren durumlarda kullanılır.
Application Context -> Genel appi ilgilendiren durumlarda kullanılır.

Activity Context'e "this" veya "this@MainActivity" ile ulaşabiliriz.
Application Context'e "applicationContext" ile ulaşabiliriz.

AlertDialog.Builder(this)
.setTitle("are you sure?") // Alert Dialog'un başlığı
.setPositiveButton("Yes"){ dialog, which -> // Buton oluşturma ve tıklanıldığında ne olacağını yazdığımız yer.
    Toast.makeText(applicationContext,"Saved!",Toast.LENGTH_LONG).show() // Toast mesaj.
          }
.setNegativeButton("No") { dialog, which ->
    Toast.makeText(this@MainActivity,"Not Saved!",Toast.LENGTH_LONG).show()
    }.show()
