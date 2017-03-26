TUGAS WEBSERVICE


Disusun Oleh :

Nama : Adli Asirof

NPM : 1144069

Kelas : 3B

PROGRAM DIPLOMA IV TEKNIK INFORMATIKA

POLITEKNIK POS INDONESIA

BANDUNG

2017


"<?xml encoding="UTF-8"?>

<!ELEMENT logbarang (barang)+>"
<!ATTLIST logbarang
    xmlns CDATA #FIXED ''>

<!ELEMENT barang (kode?,satuan?,harga,asal,tujuan)>
<!ATTLIST barang
    xmlns CDATA #FIXED ''>

<!ELEMENT kode (#PCDATA)>
<!ATTLIST kode
    xmlns CDATA #FIXED ''>

<!ELEMENT satuan (#PCDATA)>
<!ATTLIST satuan
    xmlns CDATA #FIXED ''>

<!ELEMENT harga (#PCDATA)>
<!ATTLIST harga
    xmlns CDATA #FIXED ''
    cur NMTOKEN #REQUIRED>

<!ELEMENT asal (pt,kodewil)>
<!ATTLIST asal
    xmlns CDATA #FIXED ''>

<!ELEMENT tujuan (pt,kodewil)>
<!ATTLIST tujuan
    xmlns CDATA #FIXED ''>

<!ELEMENT pt (#PCDATA)>
<!ATTLIST pt
    xmlns CDATA #FIXED ''>

<!ELEMENT kodewil (#PCDATA)>
<!ATTLIST kodewil
    xmlns CDATA #FIXED ''>"

Analisis

<?xmlversion="1.0"encoding="UTF-8"?>
Sintak untuk memulai pembuatan sintak xml

<!DOCTYPElogbarangSYSTEM"logbarang.dtd">
Sintak yang menyatakan bahwa dtd dengan logbarang sudah terhubung dengan xmlnya.

<logbarang>
Sintak element logbarang dari xml dengan nama barang.

<barang> <kode>M1112</kode> <satuan>pc</satuan> <hargacur="nmtoken">5000</harga> <asal> <pt>ladyrock</pt> <kodewil>10</kodewil> </asal> <tujuan> <pt>union</pt> <kodewil>1001</kodewil> </tujuan></barang>

Dalam elemen logbarang terdapat elemen barang dengan didalamnya terdapat element kode, satuan, harga, asal, dan tujuan. Dalam elemen harga terdapat atribut cur = "nmtoken". Dalam elemen asal terdapat elemen pt dan kodewil dan dalam elemen tujuan terdapat elemen pt dan kodewil. Dan ditutup dengan elemen penutul barang.

</logbarang>
Penutup elemen logbarang.

Logbarang.dtd

<?xml encoding="UTF-8"?>
Sintak yang digunakan pada awal dtd.

<!ELEMENTlogbarang (barang)+>
Dalam element dtd logbarang terdapat element dengan nama "barang". Terdapat tanda "+" ini menyatakan bahwa data pada element barang harus ada minimal 1 atau lebih.

<!ATTLISTlogbarang xmlns CDATA#FIXED_''_>
Attlist menyatakan nama element dalam xml.

<!ELEMENTbarang (kode?,satuan,harga,asal,tujuan)>
Pada elemen barang didalamnya terdapat element lain yaitu kode, satuan, harga, asal dan tujuan. Tanda "?" menyatakan bahwa elemen yang memiliki tanda tersebut boleh tidak memiliki data atau bisa memiliki data.

<!ELEMENTkode(#PCDATA)><!ATTLISTkode xmlns CDATA#FIXED_''_>
Pada elemen kode berisi data atau value. Dengan nama elemen di xml kode.

<!ELEMENTsatuan(#PCDATA)><!ATTLISTsatuan xmlns CDATA#FIXED_''_>
Pada elemen satuan berisi data atau value. Dengan nama elemen di xml satuan.

<!ELEMENTharga(#PCDATA)><!ATTLISTharga xmlns CDATA#FIXED_''_ cur NMTOKEN#IMPLIED>
Pada elemen harga berisi data atau value. Dengan nama elemen di xml harga dan atribut cur dengan nilai nmtoken.

<!ELEMENTasal (pt,kodewil)><!ATTLISTasal xmlns CDATA#FIXED_''_>
Pada elemen asal didalamnya terdapat elemen pt dan kodewil.

<!ELEMENTtujuan (pt,kodewil)><!ATTLISTtujuan xmlns CDATA#FIXED_''_>
Pada elemen tujuan didalamnya terdapat elemen pt dan kodewil.

<!ELEMENTpt(#PCDATA)><!ATTLISTpt xmlns CDATA#FIXED_''_>
Pada elemen pt berisi data atau value. Dengan nama elemen di xml pt.

<!ELEMENTkodewil(#PCDATA)><!ATTLISTkodewil xmlns CDATA#FIXED_''_>
Pada elemen kodewil berisi data atau value. Dengan nama elemen di xml kodewil.
